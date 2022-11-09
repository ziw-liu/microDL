# Image translation exercise adapted from DL@MBL 2022

The [course repository](https://github.com/dlmbl) contains delicious nuggets on deep learning for image anlaysis! The image translation repository from the course is [here](https://github.com/dlmbl/image_translation).

Following walkthrough shows how to download a relatively small dataset, how to setup a conda environment with microDL on an intel x64 computer, and how to train and evaluate an image translation model.

## Get the terminal ready

If the `(base)` prefix is not present in front of the shell prompt, you need to initialize conda and restart the terminal:

```sh
conda init bash
```

## Download data

Open the terminal and run the shell script that downloads the data. You are welcome to examine the script to understand the steps.

```sh
bash download_data.sh 
```

## Setup microDL

Open the terminal and run the shell script that fetches the correct release of microDL repository and adds it to python search path. You are welcome to examine the script to understand the steps. `source` command is needed to add the environment variables set in the script to the current shell.

```sh
source setup_microdl.sh 
```

## Setup and activate the new conda environment

```sh
conda env create --file=microDL/conda_env_microdl_care.yml
conda activate microdl2022
```

## Start jupyter lab

### If working on a virtual desktop (e.g., NoMachine)

Launch jupyter lab from the terminal within your session:

```sh
jupyter lab
```

### If working on a terminal

Launch a jupyter lab server that you can connect from your browser:

```sh
jupyter lab --ip=0.0.0.0 --port=8888 --no-browser
```

Then you can access your notebooks in your browser at:

```sh
http://<your server address>:8888?<token generated by jupyter lab>
```

`<your server address>` is the host address you use to connect via ssh or nomachine, and *not the hostname displayed by jupyter lab in the terminal*. You do need to copy the token shown by the jupyter lab server in the terminal.

## Open the notebook
  
Open [this notebook](exercise.ipynb), and continue with the instructions in the notebook.