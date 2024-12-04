# devcontainer-julia-cuda
Wraps CUDA and julia in a devcontainer for fast setup and development

## Quickstart

- [open the devcontainer](https://code.visualstudio.com/docs/devcontainers/tutorial)
- Go to localhost:8888
- Type in your token

## Setup

### Token

Change the token in docker-compose.yml

`environment:
      JUPYTER_TOKEN: "Test1234!"`

to another value.

### GPUs

[Set the GPU usage](https://docs.docker.com/compose/how-tos/gpu-support/) in docker-compose.yml

### JuptyerLab

The src folder is mounted to the JupyterLab parent directory. This can be changed in docker-compose.yml

`volumes: 
    - ../src:/home/jovyan/projects`

## Dependencies

This essentially just wraps the [awesome CUDA extended julia-jupyterlab](https://github.com/b-data/jupyterlab-julia-docker-stack/blob/) in a devcontainer for fast and easy setup