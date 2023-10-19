
# Example Deployment Utils

## Description

This repository contains a Helm chart used for deploying a set of example services. It is designed to demonstrate the Helm architecture and acts as a template for similar deployments.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Kubernetes cluster (Minikube, kind, etc.)
- Helm, version 3.0+

### Installation

1. Clone the repository to your local machine:

```bash
git clone https://github.com/omermishania/example-deployment-utils.git
```

2. Navigate to the project directory:

```bash
cd example-deployment-utils
```

3. Update Git Submodules:

```bash
git submodule update --init --recursive --remote --force
```

4. Install the Helm chart:

```bash
helm install [RELEASE_NAME] deployment
```

Replace `[RELEASE_NAME]` with your desired release name.


## Structure

The project has the following structure:

- `deployment/`: Contains the Helm chart for the services.
  - `charts/`: Includes any subcharts upon which the main chart depends.
  - `templates/`: Contains Symlinks to Git Submodules.
  - `Chart.yaml`: A YAML file containing information about the chart.
  - `values.yaml`: The default configuration values for this chart.

- `.github/`: Contains GitHub workflow definitions.
  - `workflows/`: Contains the Helm chart CI/CD workflow.
