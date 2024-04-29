# :sunglasses: Lab Joel :sunglasses:

This repo configures my Kubernetes HomeLab.  I use this for learning but also to host some functional services on my home network.

All apps are deployed/configured via GitOps using ArgoCD.

## :computer: Hardware

The cluster is running HA k3s with all nodes being both a master and a worker node.

:green_circle: 3x Nodes :green_circle:

* **Model**: Lenovo Thinkcentre M900 Tiny
* **CPU**: Intel i5-6500T
* **RAM**: 32GB DDR4
* **Storage**: 256GB SSDs
* **OS**: Debian 12

## :rocket: Installed Apps & Tools

### Apps
End User Applications
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

### System
Applications/services core to the cluster
<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
        <th>Public?</th>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/argocd.svg"></td>
        <td><a href="https://argo-cd.readthedocs.io/en/stable/">ArgoCD</a></td>
        <td>Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/cert-manager.svg"></td>
        <td><a href="https://cert-manager.io/">cert-manager</a></td>
        <td>X.509 certificate management for Kubernetes.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/grafana.svg"></td>
        <td><a href="https://grafana.com/">Grafana</a></td>
        <td>The open observability platform.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/longhorn.svg"></td>
        <td><a href="https://longhorn.io/">Longhorn</a></td>
        <td>Cloud native distributed block storage for Kubernetes.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg"></td>
        <td><a href="https://prometheus.io/">Prometheus</a></td>
        <td>An open-source monitoring system with a dimensional data model, flexible query language, efficient time series database and modern alerting approach.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/traefik.svg"></td>
        <td><a href="https://traefik.io/traefik/">Traefik</a></td>
        <td>Used as the Kubernetes ingress controller/reverse proxy.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/github.svg"></td>
        <td><a href="https://github.com/bitnami-labs/sealed-secrets">Sealed Secrets</a></td>
        <td>A Kubernetes controller and tool for one-way encrypted Secrets.</td>
        <td>:x:</td>
    </tr>
</table>

### Tools
Tools used for managing the cluster

<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
        <th>Public?</th>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/ansible.svg"></td>
        <td><a href="https://www.ansible.com/">Ansible</a></td>
        <td>An automation platform for bootstrapping the physical nodes.</td>
        <td>:x:</td>
    </tr>
    <tr>
        <td><img width="32" src="https://icon.icepanel.io/Technology/svg/K3s.svg"></td>
        <td><a href="https://k3s.io/">k3s</a></td>
        <td>A lightweight Kubernetes distribution.</td>
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

- [ ] Setup federated identity for apps
- [ ] Setup cloudflare tunnel for public access

