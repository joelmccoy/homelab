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

> [!WARNING]
> The secrets may need to have helm hooks added in manually to ensure they are created first.  This is because the database migrations is a prehook in the chart.  If you regenerate the secrets, you will need to manually add these hooks back in: `helm.sh/hook-weight: "0"` `helm.sh/hook: "pre-install, pre-upgrade"`
