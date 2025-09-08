# ML Services Overview - Learning Notes

## Overview
This lesson provides an overview of **ML Services** within Oracle Cloud Infrastructure.  
It explains the relationship between data, AI services, and machine learning services.  
The primary focus is on **OCI Data Science** as part of machine learning services.  

## Key Concepts
- **Data as the foundation**: AI and ML work on and require data.  
- **Application layer**: Refers to ways AI is consumed, such as applications, business processes, or analytics systems.  
- **Two groups between application and data layer**:  
  - AI Services (covered in a previous lesson)  
  - Machine Learning Services (focus of this lesson)  
- **OCI Data Science**: A cloud service supporting data scientists through the full ML lifecycle, with Python and open-source support.  
- **Core Principles of OCI Data Science**:  
  - Accelerated  
  - Collaborative  
  - Enterprise Grade  

## Detailed Notes
- **OCI Data Science** serves data scientists throughout the full machine learning lifecycle, with Python and open-source support.  
- Features include:  
  - Model catalog  
  - Projects  
  - JupyterLab Notebook  
  - Model deployment  
  - Model training  
  - Model management  
  - Model explanation  
  - Open-source libraries  
  - AutoML  

### Core Principles of OCI Data Science
1. **Accelerated**  
   - Helps accelerate the work of individual data scientists.  
   - Provides open-source libraries and access to compute power without infrastructure management.  
   - Includes Oracle’s own library to streamline work.  

2. **Collaborative**  
   - Improves team productivity by sharing assets and reducing duplicative work.  
   - Supports reproducibility and auditability of models for collaboration and risk management.  

3. **Enterprise Grade**  
   - Integrated with OCI security and access protocols.  
   - Underlying infrastructure is fully managed.  
   - Handles maintenance, patching, and upgrades, allowing users to focus on solving business problems.  

### Usage of OCI Data Science
- **What it is**: Cloud service to rapidly build, train, deploy, and manage ML models.  
- **Whom it serves**: Data scientists and teams.  
- **Where it is used**: In JupyterLab Notebook interface with Python.  
- **How it is used**:  
  - Models are preserved in the Model Catalog.  
  - Models are deployed on managed infrastructure.  

### Product Terminology
- **Projects**  
  - Containers for organizing and documenting data science assets (notebook sessions, models).  
  - Represent collaborative workspaces.  
  - No limits on the number of projects in a tenancy.  

- **Notebook Sessions**  
  - JupyterLab environments with preinstalled open-source libraries.  
  - Interactive coding environment for building and training models.  
  - Runs on managed infrastructure with selectable CPU/GPU, compute shape, and storage.  

- **Conda Environment**  
  - Open-source environment and package management system created for Python.  
  - Used to install, run, and update packages and dependencies.  
  - Supports creating, saving, loading, and switching between environments.  

- **Accelerated Data Science (ADS) SDK**  
  - Oracle’s Python library included in OCI Data Science.  
  - Automates/simplifies workflow steps: connecting to data, exploring, visualizing, training (AutoML), evaluating, and explaining models.  
  - Provides interface to access Data Science service, Model Catalog, and OCI services (e.g., Object Storage).  

- **Models**  
  - Mathematical representations of data and business processes.  
  - Created in notebooks and projects.  

- **Model Catalog**  
  - Centralized repository to store, track, share, and manage models.  
  - Stores metadata (provenance, Git info, scripts, notebooks).  
  - Models can be shared across teams and reloaded into notebook sessions.  

- **Model Deployments**  
  - Deploy models from Model Catalog as HTTP endpoints on managed infrastructure.  
  - Operationalizes models as web applications or APIs.  
  - Enables real-time predictions.  

- **Jobs**  
  - Enable defining and running repeatable ML tasks on managed infrastructure.  

## Important Terms
- **OCI Data Science**: Cloud service for ML lifecycle with Python and open-source support.  
- **Projects**: Collaborative containers for organizing assets.  
- **Notebook Sessions**: JupyterLab environments for building/training models.  
- **Conda Environment**: Package/environment management system for Python.  
- **Accelerated Data Science (ADS) SDK**: Python library automating ML workflows.  
- **Models**: Mathematical representation of data and processes.  
- **Model Catalog**: Centralized repository for storing and managing models.  
- **Model Deployments**: HTTP endpoints for operationalizing models.  
- **Jobs**: Managed repeatable ML tasks.  

## Summary
- **ML Services** in OCI build on data as their foundation.  
- Applications consume AI through AI services and ML services.  
- **OCI Data Science** supports data scientists and teams across the ML lifecycle with Python and open-source tools.  
- Core principles: **Accelerated**, **Collaborative**, and **Enterprise Grade**.  
- Provides features such as projects, notebooks, Conda environments, ADS SDK, model catalog, deployments, and jobs.  
- Fully managed infrastructure allows users to focus on solving business problems with data science.  
