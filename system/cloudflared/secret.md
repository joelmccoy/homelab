# Create the Sealed Secret

Use the tpl file secrets.env and replace values
```bash
cp secrets.env.tpl secrets.env
```

Setup the Cloudflare tunnel
```bash
cloudflared tunnel login
cloudflared tunnel create <NAME>
cp <PATH_FROM_PREVIOUS_COMMAND> ./credentials.json 
```


Create the sealed secret
```bash
k create secret generic -n cloudflared --from-file=credentials.json cloudflared-credentials --dry-run=client -o yaml | kubeseal --controller-namespace=sealed-secrets -w templates/secret.yaml
```
