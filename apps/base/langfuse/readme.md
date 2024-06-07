```
kubectl create secret generic langfuse-secrets -n langfuse --dry-run=client --from-env-file=.env.secret -o yaml > langfuse-secrets.yaml
```

```
kubeseal --format=yaml --cert=../../../keys/pub-sealed-secrets.pem < langfuse-secrets.yaml > langfuse-secrets-sealed.yaml
```