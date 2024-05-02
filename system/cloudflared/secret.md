# Create the Sealed Secret

Use the tpl file secrets.env and replace values
```
cp secrets.env.tpl secrets.env
```

Create the sealed secret
```bash
k create secret generic -n cloudflared --from-env-file=secrets.env cloudflared-credentials --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```
