# Dockerfiles

This is a repo to hold various Dockerfiles for images I create.

* [hugo-builder](https://github.com/afreisinger/hugo-builder.git) Lightweight Alpine-Based Docker Image for [Hugo](https://gohugo.io/).

* [nginx-alpine](https://github.com/afreisinger/nginx-alpine.git) Publish docker image to multiple registries with nginx docker file.

## Cloning a project with submodules

```text
git clone --recursive https://github.com/afreisinger/dockerfiles.git
```

## Adding submodules to a Git repository

```text
git submodule add -f https://github.com/afreisinger/nginx-alpine.git nginx-alpine
```
## Updating submodules to a Git repository
```text
## Adding Submodules to a Git Repository
git submodule update --remote --merge
```
## Abouts

Almost all of these live on dockerhub under [afreisinger](https://hub.docker.com/u/afreisinger)

## Resources

More information about [Git Submodules: Adding, Using, Removing, Updating](https://chrisjean.com/git-submodules-adding-using-removing-and-updating/) by @chrisjean