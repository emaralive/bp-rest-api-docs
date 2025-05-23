# BP REST API Docs #

Repository of documentation for the  BP REST API.

This project is based on [Slate](https://github.com/slatedocs/slate).

## Usage ##

### Instructions for local installation

- [Using Slate Natively](https://github.com/slatedocs/slate/wiki/Using-Slate-Natively)
- [Using Slate in Vagrant](https://github.com/slatedocs/slate/wiki/Using-Slate-in-Vagrant)
- [Using Slate in Docker](https://github.com/slatedocs/slate/wiki/Using-Slate-in-Docker)

### Updating and building the docs

The docs for the latest version of the REST API (v1) are in `source/includes/bp-rest-api-v1`. Each section of the docs has its own Markdown file. Once you have made changes, you can generate the docs locally with one of the following:

#### Natively

```
bundle exec middleman build
```
After this command completes, the generated docs can be found in the `build` directory. Open the `index.html` file in your browser to view the local version of the docs site.

#### Vagrant

```
vagrant ssh -c "cd /vagrant; bundle exec middleman build"
```
After this command completes, the generated docs can be found in the `build` directory. Open the `index.html` file in your browser to view the local version of the docs site.

#### Docker

```
docker run --rm --name slate -v $(pwd)/build:/srv/slate/build -v $(pwd)/source:/srv/slate/source slatedocs/slate build
```
After this command completes, the generated docs can be found in the `build` directory. Open the `index.html` file in your browser to view the local version of the docs site.

> [!Note]
> You may omit the final build argument and get the same result. By default, if given no command, the Dockerfile will run build.

### Deploying the docs

When you merge a PR to the trunk branch of this repository, a workflow runs that will automatically deploy the generated docs to the `gh-pages` branch. However, you can also deploy manually with the following:

```bash
./deploy.sh
```
