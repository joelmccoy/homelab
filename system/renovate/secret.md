# Create the Sealed Secret

Use the tpl file secrets.env and replace values
```bash
cp secrets.env.tpl secrets.env
```

Create the sealed secret
```bash
k create secret generic -n renovate --from-env-file=secrets.env renovate-secret --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```
