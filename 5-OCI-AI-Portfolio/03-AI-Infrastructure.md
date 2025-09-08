# GPU in AI Infrastructure - Learning Notes

## Overview
This lesson explains the role of the **Graphics Processing Unit (GPU)** in AI infrastructure.  
It covers why GPUs are required for AI and machine learning workloads, their architecture, how modern GPUs accelerate deep learning, and the evolution of NVIDIA GPUs.  
The session also introduces how **OCI AI infrastructure** leverages GPUs for training and deployment of large language models (LLMs).  

## Key Concepts
- **GPU**: Specialized hardware optimized for repetitive and parallel computations.  
- **Parallel Computing**: Thousands of lightweight GPU cores work simultaneously on data.  
- **Throughput Advantage**: GPUs process many inference tasks in parallel, useful for batch processing or serving multiple requests.  
- **Deep Learning Frameworks**: Modern GPUs are optimized for TensorFlow, PyTorch, and ONNX Runtime.  
- **NVIDIA GPU Evolution**: Progression from A100 (2020) to H100 (2022), H200 (2024), and Blackwell (2025).  
- **OCI GPU Offerings**: OCI compute supports a wide range of GPUs including H100N, L40, H200, B200, and GB200.  
- **OCI AI Quick Actions**: Simplify deployment, fine-tuning, and inference for popular LLMs using GPU-powered infrastructure.  

## Detailed Notes
### What is a GPU and Why it is Required
- GPUs are essential for **machine learning and AI workloads** due to the large amount of repetitive calculations needed for model training and inference.  
- **Parallel computing** allows GPUs to run many processes at the same time.  
- Thousands of lightweight cores handle data in parallel, enabling processing of very large datasets at high speed.  
- GPUs can handle many inference tasks simultaneously, giving much higher throughput than CPUs.  
- Particularly useful for batch processing or serving multiple requests.  

### Optimization for Deep Learning
- Modern GPUs are optimized for frameworks like **TensorFlow**, **PyTorch**, and **ONNX Runtime**.  
- These frameworks leverage GPU-specific libraries to accelerate computations.  

### NVIDIA GPU Evolution
- **A100 (2020, Ampere architecture)**  
  - Uses tensor cores, crucial for accelerating deep learning workloads.  
  - Tensor cores perform multiple fused multiply-accumulate operations in a single clock cycle.  

- **H100 (2022, Hopper architecture)**  
  - Introduced a dedicated transformer engine to optimize transformer model performance.  

- **H200 (2024)**  
  - Similar to H100 but with more memory.  

- **Blackwell Architecture (2025)**  
  - Designed to accelerate large-scale AI models.  
  - Aligned with growing focus on **LLMs**.  

- **NVIDIA Grace CPU**  
  - Breakthrough processor for modern data centers running AI Cloud and HPC applications.  

- **NVIDIA GB200 (2025)**  
  - Grace Blackwell and L4 superchip.  
  - Unlocks performance through unification of Blackwell GPU with two base CPUs.  

### OCI GPU Compute Offerings
- OCI broadens its GPU compute lineup to support small, medium, and large use cases.  
- Current availability: **10,800 H100N**, **L40 GPU**.  
- Upcoming (2025): **H200**, **B200**, **GB200 superchips**.  
- Also offering **superclusters** built on these GPUs.  

### Performance Improvements
- Beginning with **H200**, performance is **4X** compared to H100 superclusters.  
- With **B200** and **GB200**, performance reaches **APEX** compared to H100 for AI workloads.  

### Using OCI AI Infrastructure
- Through **OCI Data Science**, GPUs can be used for training and deploying LLMs.  
- Options include:  
  - **Direct deployment** of popular LLMs to VM or bare metal instances with GPUs via AI Quick Actions.  
  - **Fine-tuning** base models and deploying custom models for inference via AI Quick Actions.  
- Current support: Registering any model supported by:  
  - Virtual LLM  
  - Next generation inference  
  - Text-embedding inference containers  

## Important Terms
- **GPU**: Graphics Processing Unit, specialized hardware for parallel computations.  
- **Parallel Computing**: Simultaneous processing using thousands of lightweight cores.  
- **Inference**: Model predictions, often run in parallel on GPUs.  
- **Tensor Cores**: Hardware components in NVIDIA GPUs for accelerating deep learning.  
- **Ampere Architecture**: Architecture of A100 GPUs.  
- **Hopper Architecture**: Architecture of H100 GPUs with transformer engine.  
- **Blackwell Architecture**: Architecture designed for large-scale AI models (2025).  
- **NVIDIA Grace CPU**: Processor for AI Cloud and HPC applications.  
- **NVIDIA GB200**: Grace Blackwell + L4 superchip (2025).  
- **OCI GPU Compute**: Oracle Cloud Infrastructure GPU offerings (H100N, L40, H200, B200, GB200).  
- **Superclusters**: Large-scale GPU clusters in OCI with high performance.  
- **OCI Data Science AI Quick Actions**: Tools for deploying, fine-tuning, and inferring models on GPU-powered infrastructure.  

## Summary
- GPUs are vital for AI and ML due to their ability to handle repetitive, large-scale calculations in parallel.  
- Modern GPUs, with tensor cores and transformer engines, are optimized for deep learning workloads.  
- NVIDIA’s evolution: **A100 → H100 → H200 → Blackwell**, along with Grace CPU and GB200 superchips, continuously improves performance for AI.  
- **OCI GPU Compute** provides access to the latest GPUs, with upcoming H200, B200, and GB200 superclusters promising massive performance gains.  
- **OCI Data Science AI Quick Actions** simplify deploying, fine-tuning, and running inference on LLMs using GPU infrastructure.  
