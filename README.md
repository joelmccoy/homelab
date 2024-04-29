# :sunglasses: Lab Joel :sunglasses:

This repo configures my Kubernetes HomeLab.  I use this for learning but also to host some functional services on my home network.

All apps are deployed/configured via GitOps using ArgoCD.

## :computer: Hardware

The cluster is running HA k3s with all nodes being both a master and a worker node.

3x Nodes:

* **Model**: Lenovo Thinkcentre M900 Tiny
* **CPU**: Intel i5-6500T
* **RAM**: 32GB DDR4
* **Storage**: 256GB SSDs
* **OS**: Debian 12

## :rocket: Installed Apps & Tools

### Apps
<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
        <th>Public?</th>
    </tr>
    <tr>
        <td><img width="32" src="https://simpleicons.org/icons/homeassistant.svg"></td>
        <td><a href="https://www.home-assistant.io/">Home Assistant</a></td>
        <td>Smart home integrations and automations.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://simpleicons.org/icons/github.svg"></td>
        <td><a href="https://github.com/gethomepage/homepage">Home Page</a></td>
        <td>Home landing page for all apps and services.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/teslamate.svg"></td>
        <td><a href="https://github.com/teslamate-org/teslamate">TeslaMate</a></td>
        <td>A powerful, self-hosted data logger for your Tesla.</td>
        <td>:x:</td>
    </tr>
</table>


## :gear: Bootstrapping Steps

Deploy ArgoCD to the Kubernetes Cluster

```bash
cd system & make bootstrap
```
*Note: ArgoCD needs setup first so all other apps and tools can be deployed*

## :heavy_check_mark: TODO 
TODO
