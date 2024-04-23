# homelab
My Kubernetes Homelab Setup

## Bootstrapping Steps

Deploy ArgoCD to the Kubernetes Cluster

```bash
cd system & make bootstrap
```
*Note: ArgoCD needs setup first so all other apps and tools can be deployed*

Add Cloudflare API Token needed by cert-manager

```bash
kubectl -n cert-manager create secret generic cloudflare-api-token --from-literal api-token=<API_KEY_GOES_HERE>
```
