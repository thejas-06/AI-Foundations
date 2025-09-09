# OCI Data Science Service Demo - Learning Notes

## Overview
This lesson demonstrates a hands-on demo of **OCI Data Science Service**, replicating a previously shown machine learning demo in the Oracle Data Science environment. The session walks through creating projects, notebook sessions, Conda environments, and building, training, and deploying a machine learning model using **Random Forest Classifier** with the **Iris dataset**.

## Key Concepts
- **OCI Data Science Service**: A fully managed platform for data science teams to build, train, deploy, and manage ML models.
- **Projects and Notebook Sessions**: Core workspace units in the service where resources like compute shapes, storage, and environments are configured.
- **Conda Environments**: Prepackaged environments with libraries suited for different ML/AI use cases.
- **ADS Library**: A library that simplifies model preparation, deployment, and lifecycle tasks in OCI.
- **Model Workflow Steps**: Includes `initiate`, `prepare`, `verify`, `save`, `deploy`, and `predict`.

## Detailed Notes
### Getting Started
- The demo replicates a machine learning example in the **OCI Data Science service**.
- Sign up for an **Oracle account** to use the service.
- The setup of policies and workspaces is not covered (recommended to take the OCI Data Science Professional course for that).

### Service Overview
- **Data Science** is available in the **Machine Learning stack** under **Analytics and AI**.
- Provides a managed platform with Python and open-source tools for building and deploying ML models.

### Creating a Project
1. From the Data Science service page, click **Create Project**.
2. Select compartment, enter project name and description.
3. Click **Create** to initialize the project.
4. After creation, the active project shows notebook sessions with details such as state, compute, shape, network, and endpoint.

### Notebook Sessions
- To create a notebook session:
  1. Click **Create Notebook Session**.
  2. Select compartment and provide session name (or let system generate one).
  3. Choose **Compute Shape** (with options like AMD, Intel, etc., along with CPU and memory).
  4. Define **block storage, networking resources, and endpoint type**.
  5. Click **Create**.
- Active notebook sessions display additional metrics and details.
- Launching an active session opens the **Jupyter environment**.

### Jupyter Environment
- Begin with a **new launcher** tab, which provides kernels and resources.
- Create a **Conda environment**:
  - Open **Environment Explorer**.
  - Browse multiple Conda environments, view their descriptions, included libraries, and installation steps.
  - Copy installation command and run it in the terminal.
  - After refresh, the new kernel appears in the launcher.

### Conda Environments in Use
- Example: **general ML, machine learning with Python 3.8**.
- Select or switch Conda environments directly in Jupyter.

### Model Development Workflow
- Import required libraries.
- Load the **Iris dataset**.
- Split into:
  - **Features** (X)
  - **Target variable** (y)
- Further split into **training** and **testing** sets.
- Train a **Random Forest Classifier**.
- Create a **model object** and call `.prepare()` to generate artifacts.
- Use **ADS library** for model preparation, deployment artifacts, and extra steps.

### Model Lifecycle
- **`summary_status`**: Returns a pandas dataframe showing:
  - Available methods.
  - Method descriptions.
  - Status of each step (initiate, prepare, verify, save, deploy, predict).
  - Required actions, if any.
- Completed steps in demo: **initiate** and **prepare**.
- **`verify`**: Simulates model deployment and performs predictions on test data (e.g., first 10 rows).
- **`save`**: Saves the model artifact to the model catalog.
- **`deploy`**: Deploys model to REST endpoint.
- **`predict`**: Invokes deployed endpoint for predictions.

### Demo Scope
- Completed steps: **initiate**, **prepare**, **verify**, and **save**.
- Deployment (`deploy`) and prediction (`predict`) steps are outlined but not executed in this demo.
- The created model (e.g., sklearn model) is visible under **Models** in the notebook session.

## Important Terms
- **OCI Data Science Service**: Oracle’s managed ML platform.
- **Compartment**: Logical entity for organizing cloud resources.
- **Notebook Session**: Interactive development environment within a project.
- **Compute Shape**: Virtual machine type (e.g., AMD, Intel) with configurable CPU and memory.
- **Conda Environment**: Predefined environment with specific ML libraries.
- **ADS Library**: Oracle’s Accelerated Data Science library.
- **Random Forest Classifier**: Machine learning model used in the demo.
- **Model Catalog**: Repository where model artifacts are saved.
- **REST Endpoint**: Deployment endpoint for serving model predictions.

## Summary
The demo showcases the complete workflow of using **OCI Data Science Service**:
- Creating projects and notebook sessions.
- Setting up **Conda environments**.
- Loading and preprocessing the **Iris dataset**.
- Training a **Random Forest Classifier**.
- Using the **ADS library** to prepare, verify, save, and manage the model lifecycle.
- While the full deployment and prediction steps were not executed, the demo provides clear instructions for completing them independently.
