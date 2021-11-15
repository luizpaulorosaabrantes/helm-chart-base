# Basic helm chart repository creation

[Link](https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417)

Create a directory wich will be our source charts and use helm create command.

```bash
mkdir ./helm-chart-sources
helm create helm-chart-sources/helm-chart-test
```

### Lint the Chart 
 
The `helm lint` command runs a series of tests to verify that the cart is ok.

```bash
helm lint helm-chart-sources/*
```

### Package

The `helm package` command packages a chart into a versioned chart archive file.

```bash
helm package helm-chart-sources/*

- helm-chart-test.0.1.0.tgz will be created
```

## Repository index 

A repository index is a special file called `index.yaml` that has a list of all of the packeges supplied by the repository, together with metadata that allows retrieving and verifying those packages.