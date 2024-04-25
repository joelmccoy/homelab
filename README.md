# homelab
My Kubernetes Homelab Setup

## Bootstrapping Steps

TODO: Move these instructions to another document.

Deploy ArgoCD to the Kubernetes Cluster

```bash
cd system & make bootstrap
```
*Note: ArgoCD needs setup first so all other apps and tools can be deployed*

### Add Cloudflare API Token needed by cert-manager

```bash
kubectl -n cert-manager create secret generic cloudflare-api-token --from-literal api-token=<API_KEY_GOES_HERE>
```

### Add Longhorn Backup Secret to Backup to AWS S3

Follow Instructions to create user and permissions [here](https://longhorn.io/docs/1.6.1/snapshots-and-backups/backup-and-restore/set-backup-target/).
```bash
kubectl create secret generic s3-backup-secret \
    --from-literal=AWS_ACCESS_KEY_ID=<your-aws-access-key-id> \
    --from-literal=AWS_SECRET_ACCESS_KEY=<your-aws-secret-access-key> \
    -n longhorn-system
```
