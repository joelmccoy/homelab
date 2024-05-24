# Create the Tesla Sealed Secret

Use the tpl file secrets.env and replace values
```
cp secrets.env.tpl secrets.env
```

Create the sealed secret
```bash
k create secret generic -n teslamate --from-env-file=secrets.env teslamate-secret --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```
