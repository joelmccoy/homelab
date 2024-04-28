# Create the Tesla Sealed Secret

Create secrets.env (Will not be checked into git)
```
ENCRYPTION_KEY="REPLACE_WITH_RANDOM_STRING"
DATABASE_NAME="teslamate"
DATABASE_HOST="postgres-v15-rw.teslamate.svc.cluster.local"
DATABASE_PASS="REPLACE_WITH_DATABASE_PASS"
DATABASE_USER="teslamate"
POSTGRES_DB="teslamate"
POSTGRES_PASS="REPLACE_WITH_DATABASE_PASS"
POSTGRES_USER="teslamate"
```

Create the sealed secret
```bash
k create secret generic -n teslamate --from-env-file=secrets.env teslamate-secret --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```

