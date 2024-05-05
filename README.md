# HOMELAB-K8S-METALLB

Wrapper for [MetalLB helm chart](https://artifacthub.io/packages/helm/bitnami/metallb)

## Run

```sh
helm upgrade --install --create-namespace -n metallb-system metallb . --wait --wait-for-jobs --timeout 3m
# OR --atomic
```

## Updating Dependencies

```sh
rm -rf charts && helm dep update && cd charts && for filename in *.tgz; do tar -xf "$filename" && rm -f "$filename"; done; cd ..
```
