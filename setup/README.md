# Introduction

## Activate
```shell
source $HOME/VENV/lida3.10/bin/activate
```

## Setup a local venv on Macosx Apple Silicon
```shell
python3 -m pip install --upgrade pip
python3 -m pip install --no-cache-dir -r ./setup/requirements.txt
```

## Add a jupyter notebook kernel to VENV
```shell
VENV_NAME="lida3.10"
VENV_DIR="$HOME/VENV"
source ${VENV_DIR}/${VENV_NAME}/bin/activate;
python3 -m pip install --upgrade pip
python3 -m pip install ipykernel
deactivate
```

We need to reactivate the venv so that the ipython kernel is available after installation.
```shell
VENV_NAME="lida3.10"
VENV_DIR="$HOME/VENV"
source ${VENV_DIR}/${VENV_NAME}/bin/activate;
python3 -m ipykernel install --user --name=${VENV_NAME} --display-name ${VENV_NAME}
```
Note: 
* restart the vs code, to select the venv as jupyter notebook kernel

Reference:
* https://ipython.readthedocs.io/en/stable/install/kernel_install.html
* https://anbasile.github.io/posts/2017-06-25-jupyter-venv/