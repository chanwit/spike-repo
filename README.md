# Spike Repo

## How to re-bootstrap when things go wrong.

```sh
# create a new blank cluster
kind create cluster

# set the token
export GITHUB_TOKEN=$(cat github_token)

# re-bootstrapping Flux
flux bootstrap github \
  --owner=chanwit \
  --repository=spike-repo \
  --path=./manifests/clusters/default \
  --branch=main
```
