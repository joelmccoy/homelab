# :sunglasses: Lab Joel :sunglasses:

This repo configures my Kubernetes HomeLab.  I use this for learning but also to host some functional services on my home network.

All apps are deployed/configured via GitOps using ArgoCD.

## :computer: Hardware

<deatails>
  <summary>Hardware Specs</summary>
  3x Nodes:
  - **Model**: Lenovo Thinkcentre M900 Tiny
  - **CPU**: Intel i5-6500T
  - **RAM**: 32GB DDR4
  - **Storage**: 256GB SSDs
  - **OS**: Debian 12
</details>

## :rocket: Installed Apps
TODO

## :gear: Bootstrapping Steps

Deploy ArgoCD to the Kubernetes Cluster

```bash
cd system & make bootstrap
```
*Note: ArgoCD needs setup first so all other apps and tools can be deployed*

## :heavy_check_mark: TODO 
TODO
