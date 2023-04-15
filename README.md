# Tetra Workspace (Kasm Image)

![Screenshot from 2022-11-28 17-33-05](https://user-images.githubusercontent.com/14095576/204409415-9cab4f7a-dfa1-456e-9fae-d512e7614429.png)

## Introduction

This repo provides a workspace for Tetra Bio Distributed volunteers to work on open-source medical hardware projects based on the [Ansible based template for KASM Ubuntu Focal Images](https://github.com/j-simmons-phd/kasm-core-focal-template) template provided by @j-simmons-phd.  The workspace is configured with the following software:

- git cli
- [Keychain](https://www.funtoo.org/Keychain)
- Firefox
- Python 3.8.x (part of the image template) with the following packages (not part of the image template)
    - pip
    - [JupyterLab](https://jupyter.org/)
    - [Jupyter Notebook](https://jupyter.org/)
    - [Voilà](https://voila.readthedocs.io/en/stable/index.html)
    - [Pint](https://pint.readthedocs.io/en/stable/)
- VS Code with the following extensions (note, auto-updates are disabled)
    - [Python extension by Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- Arduino v1.8.19
- 3D Slicers
    - [PrusaSlicer](https://www.prusa3d.com/page/prusaslicer_424/) 2.5.1

## How to Use this Repo

1. Clone this repo
1. Run `docker-compose pull` to download the image or run `docker-compose build` to build the workspace image 

## Using the image locally

Once built, the image can be pushed into the Kasm server per Kasm documentation or it can be run locally on port 6901 using docker-compose.

- **Starting the image locally:** Run `docker-compose up -d`
- **Stopping the image locally:** Run `docker-compose down`

When running locally, the workspace can be accessed at https://localhost:6901 with
- **User:** `kasm_user`
- **Passwordd:** `password`
