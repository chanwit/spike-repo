# Spike Repo

```sh
# create a new blank cluster
kind create cluster

# set the token if you got one via GH client
export GITHUB_TOKEN=$(yq '."github.com".oauth_token' ~/.config/gh/hosts.yml)

# or you can do it manually
export GITHUB_TOKEN=<your github token>

# re-bootstrapping Flux
flux bootstrap github \
  --owner=chanwit \
  --repository=spike-repo \
  --path=./manifests/clusters/default \
  --branch=main
```
