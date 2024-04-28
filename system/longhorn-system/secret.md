# Add Longhorn Backup Secret to Backup to AWS S3

TODO: Make this a sealed secret and check into git.

Follow Instructions to create user and permissions [here](https://longhorn.io/docs/1.6.1/snapshots-and-backups/backup-and-restore/set-backup-target/).
```bash
kubectl create secret generic s3-backup-secret \
    --from-literal=AWS_ACCESS_KEY_ID=<your-aws-access-key-id> \
    --from-literal=AWS_SECRET_ACCESS_KEY=<your-aws-secret-access-key> \
    -n longhorn-system
```
