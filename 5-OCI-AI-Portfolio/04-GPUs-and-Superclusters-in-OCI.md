# RDMA Supercluster - Learning Notes

## Overview
This session from the *First Principles* series explores the architectural aspects of **Remote DMA (RDMA)** technology in Oracle Cloud Infrastructure (OCI). It covers the history of RDMA adoption, its role in enabling high-performance workloads, the evolution into **RDMA Superclusters**, and the detailed design choices that make these clusters scalable, low-latency, and lossless.

## Key Concepts
- **RDMA (Remote DMA):** Enables data transfer between machines bypassing the CPU, allowing low latency, high bandwidth communication.
- **Use Cases:** Foundational for OCI database services (ExaCS, Autonomous DB), HPC workloads, and GPU workloads.
- **Rocky (RDMA over Converged Ethernet):** Strategic adoption enabling RDMA functionality over Ethernet fabrics.
- **Supercluster:** Large-scale GPU-enabled RDMA network designed to support tens of thousands of GPUs.
- **Clo Network Design:** Three-tier architecture used in the Supercluster to provide scalable nonblocking interconnects.
- **Lossless Networking:** Networking approach ensuring no packet drops, enabled by buffers and congestion notification systems.
- **Placement Mechanism:** Control plane strategy for optimizing workload deployment within blocks to balance latency and throughput.
- **Network Locality Hints:** Mechanism providing workload topology guidance to reduce latency and avoid collisions.

## Detailed Notes

### RDMA in OCI
- RDMA has been central to OCI services from the beginning.
- Allows **data transfer without CPU interference**, supporting:
  - **Extremely low latency**
  - **High bandwidth**
  - **Minimal CPU overhead**
- Critical building block for:
  - **Database services (ExaCS, Autonomous DB)**
  - **HPC workloads**
  - **GPU workloads**

### Transition to Rocky
- OCI made a **strategic bet on Rocky (RDMA over Converged Ethernet)**.
- Current HPC, GPU, and database workloads leverage Rocky on OCI’s Ethernet fabric.

### Demand for Large-Scale GPU Workloads
- Partnership with NVIDIA emphasized growing demand for **large GPU clusters**.
- Customer requirements include:
  - **Thousands to tens of thousands of GPUs**
  - Operating within a **single RDMA network (Supercluster)**

### RDMA Supercluster
- Built to support extremely large GPU workloads.
- Each GPU node:
  - 8 × NVIDIA A100 GPUs interconnected via **NVLinks**
  - Connects to the fabric at **1.6 Tbps (1,600 Gbps)**  
    → **200 Gbps per GPU**
- Fabric provides **nonblocking interconnects** for GPUs.

### Supercluster Fabric Design
- Comprised of **blocks** connected via a **three-tier Clo network**.
- Supports scaling to **tens of thousands of GPUs**, with potential beyond **100,000 GPUs**.

#### Latency Management
- **Latency within a block:** ~6.5 µs round trip.
- **Worst-case latency across Supercluster:** ~20 µs round trip.
- Managed through:
  - **QOS-enabled networking**
  - Adequate **switch and silicon buffering**
  - Buffer allocation tuned for GPU workloads

#### Lossless Networking
- Ensures **packets are not dropped**.
- Employs **intelligent congestion notification**.
- Buffers tuned for higher-latency scenarios.

### Balancing Scale and Latency
- Not all workloads require tens of thousands of GPUs.
- Placement strategy:
  - **Small workloads (e.g., ~1000 GPUs, HPC, DB)** → deployed within a **single block** for lower latency.
  - **Large workloads** → may span multiple blocks but still optimized via **network locality hints**.

### Network Locality Hints
- Provide **placement transparency** to customers.
- Help structure workloads to maximize local traffic:
  - **85% traffic remains local within a block**
  - Some traffic crosses blocks with ~20 µs latency
- Benefits:
  - Average latency is reduced
  - **Half of traffic < 6.5 µs** (local to top-of-rack switch)
  - Reduced **flow collisions**, improving throughput

### Side Benefits
- Lower latency and reduced collisions → **higher throughput** for workloads.
- Especially beneficial for large-scale GPU training workloads.

## Important Terms
- **RDMA (Remote Direct Memory Access):** Data transfer bypassing CPU for low latency, high bandwidth communication.
- **Rocky (RDMA over Converged Ethernet):** RDMA capability over Ethernet networks.
- **Supercluster:** Extremely large RDMA-enabled GPU cluster.
- **NVLinks:** NVIDIA interconnect technology for GPUs within a node.
- **Clo Network:** Multi-tiered nonblocking network design.
- **Lossless Networking:** Ensures no packet loss using buffering and congestion controls.
- **Placement:** Strategy to deploy workloads in optimal locations within the cluster to minimize latency.
- **Network Locality Hints:** Information guiding workload placement to keep traffic local and reduce latency.

## Summary
- RDMA is a **core technology** for OCI, enabling **low-latency, high-bandwidth** communication without CPU overhead.  
- OCI’s **Supercluster** architecture supports **tens of thousands of GPUs** with **lossless three-tier Clo networking**.  
- **Latency management, placement mechanisms, and network locality hints** ensure workloads are optimized for both **scale and performance**.  
- Customers benefit from **lower latency, reduced flow collisions, and higher throughput**, making the Supercluster suitable for massive GPU, HPC, and database workloads.
