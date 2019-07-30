# Ansible Role - Microk8s

Ansible role to install Microk8s (defaults to version "1.13/stable"). Includes option to install the Kubernetes dashboard.

Microk8s (https://microk8s.io/) is a lightweight, development/test only Kubernetes installation. Do not run in production; in particular, the Kubernetes API is not secure.

## Configure Versions

Use the following variables to customise the versions installed:

```
microk8s_version: "1.13/stable"
```

## Persistent Storage

Microk8s supports the hostpath-provisioner and is enabled by default. This means that Kubernetes pods need only specify the storage class "microk8s-hostpath" and MicroK8s will take care of provisioning (hostpath) persistent volumes. These volumes will reside in the directory "/var/snap/microk8s/common/default-storage".