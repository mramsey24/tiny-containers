# Demo Script

## Markdown Renderer
```bash
# See Running pods
kubectl get pods
```

```bash
$ cd /demo-markdown
$ kubectl apply -f function.yml
```

```bash
curl -4 http://127.0.0.1:31118 -d "# test"
```

```bash
# Delete the function we just added
$ kubectl delete -f function.yml
```
