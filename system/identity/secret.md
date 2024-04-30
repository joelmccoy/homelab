# Create the secrets necessary for the identity apps 

Use the tpl files and replace values
```
cp kratos_secrets.tpl.env kratos_secrets.env
cp postgres_secrets.tpl.env postgres_secrets.env
```

Create the sealed secrets
```bash
# Kratos
k create secret generic kratos-secret -n identity --from-env-file=kratos_secrets.env  --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/kratos-secret.yaml

# Postgres
k create secret generic postgres-secret -n identity --from-env-file=postgres_secrets.env  --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/postgres-secret.yaml
```
