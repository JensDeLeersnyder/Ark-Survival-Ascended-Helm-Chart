# ARK: Survival Ascended - Helm Chart
This repository provides a Helm chart to easily deploy an **ARK: Survival Ascended** server on Kubernetes.

## Prerequisites
- A Kubernetes cluster
- Helm installed on your machine
- Access to persistent storage (for server files)

# Setup

### 1. Create a Directory for Server Files
Ensure that you have a folder to store server data. Use the following commands to create and set permissions for the folder:
``` bash
mkdir -p /mnt/local-volumes/asa
chown -R steam:steam /mnt/local-volumes/asa
```

### 2. Helm deployment
``` bash
 helm repo add jensdl https://jensdeleersnyderpxl.github.io/Ark-Survival-Ascended-Helm-Chart/

 helm install myark-ascended-server jensdl/ark-survival-ascended
```

### 3. Configuration
You can customize your deployment by modifying the values.yaml file. The default values.yaml can be found here: [values.yaml](https://github.com/JensDeLeersnyderPXL/Ark-Survival-Ascended-Helm-Chart/blob/main/charts/kube-ark-survival-ascended/values.yaml)

You can use your custom values by using the following command: 
``` bash
helm install myark-ascended-server -n asa-helm --create-namespace jensdl/ark-survival-ascended -f values.yaml
```

#### Additional Environment Variables

This Helm chart uses the azixus/ark-ascended-docker Docker image. You can find additional configuration options for the Docker image by visiting their GitHub repository: [azixus/ARK_Ascended_Docker](https://github.com/azixus/ARK_Ascended_Docker)