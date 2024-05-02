# Create Sealed Secrets

Use the tpl file secrets.env and replace values
```
cp secrets.env.tpl secrets.env
```

Create the sealed secret
```bash
k create secret generic -n monitoring --from-env-file=secrets.env auth-generic-oauth-secret --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```
