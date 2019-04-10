# dev-env
_A development environment built upon docker._

## overview
The intention of this project is to provide an image with theecessary tools and packages required for a golang development environment which is convenient and accessible. The dev-env is built upon an [alpine golang image](https://hub.docker.com/_/golang), we extend this base image and include the following tools/packages:
- [golang](https://golang.org/)
- [groovy](http://groovy-lang.org/)
- [git](https://git-scm.com/)
- [hub](https://github.com/github/hub)
- [vi](https://www.vim.org/)
  - [golang plugin](https://github.com/fatih/vim-go)
  - [buffer switcher](https://github.com/manniwood/vim-buf)
  - [groovy syntax highlighting](https://github.com/vim-scripts/groovy.vim)
- [gcloud](https://cloud.google.com/sdk/gcloud/)
- [helm](https://helm.sh/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [jx](https://github.com/jenkins-x/jx)
- [dep](https://github.com/golang/dep)
- [ko](https://github.com/google/go-containerregistry/tree/master/cmd/ko)
- [ksd](https://github.com/mfuentesg/ksd)
- [delve](https://github.com/go-delve/delve)
- [pre-commit](https://pre-commit.com/)

## build
### local
Use the following command to build the docker image:
```
make build
```
### jx
Remote builds of this project are triggered via Pull Requests of Merges into master.

## run
To use the dev-env-base as a complete and stateful environment please see the [dev-env](https://github.com/jenkins-x/dev-env), or alternatively use the following as an example:
```
docker run --name dev-env-base \
           --rm \
           --tty \
           --interactive \
           gcr.io/jenkinsxio/dev-env-base:0.0.1
```
