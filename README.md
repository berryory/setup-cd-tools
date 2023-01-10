A Github Action to set up a variety of tools for Continuous Delivery.

## Supported Tools

- [jq](https://stedolan.github.io/jq/)
- [yq](https://github.com/mikefarah/yq)
- [kubectl](https://github.com/kubernetes/kubectl)
- [kustomize](https://github.com/kubernetes-sigs/kustomize)
- [skaffold](https://github.com/GoogleContainerTools/skaffold)
- [helm](https://github.com/helm/helm)
- [hub](https://github.com/github/hub)

## Usage

```
name: Deployment
on: [push]
jobs:
  deploy:
    name: Deploy
    runs-on: ubuntu-latest
    steps:
      ...
      - name: Set up tools
        uses: berryory/setup-cd-tools@v1.0.0
        with:
          kubectl: '1.25.4'
          kustomize: '4.5.7'
      ...
```
