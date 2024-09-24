# helm chart for ark-surviva-ascended

# setup

## Create folder to store server files
``` bash
mkdir -p /mnt/local-volumes/asa
```
## Helm deployment
```
 helm repo add jensdl https://jensdeleersnyderpxl.github.io/Ark-Survival-Ascended-Helm-Chart/
 helm install myark-ascended-server kube-ark-survival-ascended/jensdl
```
the values file can be found here --> [values.yaml](https://github.com/JensDeLeersnyderPXL/Ark-Survival-Ascended-Helm-Chart/blob/main/charts/kube-ark-survival-ascended/values.yaml)