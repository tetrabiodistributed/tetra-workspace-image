# Tetra Workspace (Kasm Image)

![Screenshot from 2022-11-28 17-33-05](https://user-images.githubusercontent.com/14095576/204409415-9cab4f7a-dfa1-456e-9fae-d512e7614429.png)

## Introduction

This repo provides an Immutable-Infrastructure-as-Code (IIaC) workspace based on the [KASM Ubuntu Jammy Image](https://hub.docker.com/r/kasmweb/core-ubuntu-jammy) for Tetra Bio Distributed's medical/PPE open-source hardware (OSHW) development.  The workspace is configured with the following software:

- Node JS Tools
    - nodejs v16.14.0
    - npm v8.3.1 (included with nodejs)
    - npx v8.3.1 (included with nodejs)
    - yarn v1.22.11
- Utilities
    - [git](https://git-scm.com/) 2.41.1
    - [Keychain](https://www.funtoo.org/Keychain)
    - Vim (pre-installed) with @capsulecorplab [vimrc](https://gist.github.com/capsulecorplab/495058e7a57ed8adaed3c40c80d09739#file-vimrc)
- Firefox
- Python 3.10 (part of the image template) with the following packages (not part of the image template)
    - pip
    - [JupyterLab](https://jupyter.org/)
    - [Jupyter Notebook](https://jupyter.org/)
    - [Pint](https://pint.readthedocs.io/en/stable/)
    - [LinkML](https://linkml.io/linkml/)
    - [Jinja2](https://jinja.palletsprojects.com/en/3.1.x/)
- VS Code with the following extensions (note, auto-updates are disabled)
    - [Python extension by Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    - [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- Knowledge Capture Tools
    - [JabRef](https://www.jabref.org/) v5.5.6
- OSHW Design Tools
    - [Arduino](https://wiki-content.arduino.cc/en/software) 1.8.19
        - [Arduino CLI](https://github.com/arduino/arduino-cli) 0.33.0
        - [megaTinyCore](https://github.com/SpenceKonde/megaTinyCore) 2.6.8
        - [Arduino Pico](https://github.com/earlephilhower/arduino-pico) 3.3.0
        - [Arduino ESP32](https://github.com/espressif/arduino-esp32) 2.0.9
    - [KiCAD](https://www.kicad.org/) 7.0.5
    - [FreeCAD](https://www.freecad.org/) 0.19
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
