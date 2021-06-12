# Steps of donkey car
In this part we will start from the xxxxxxxxxxxxx very useful software "KRename".

## The following tutorial is based on Linux Ubuntu system


The official website of donkey car:
https://docs.donkeycar.com/

Install Software On Donkeycar



First, open derminal and install miniconda as well as clone the donkey project

```sh
$ mkdir project
$ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
$ bash ./Miniconda3-latest-Linux-x86_64.sh
$ cd project
$ mkdir donkeycar
```

Get the latest donkeycar from Github

```sh
$ git clone https://github.com/autorope/donkeycar
$ cd donkeycar
$ git checkout master
```
If this is not your first install, update Conda and remove old donkey

```sh
$ conda update -n base -c defaults conda
$ conda env remove -n donkey
```
Create the Python anaconda environment

```sh
$ conda env create -f install/envs/ubuntu.yml
$ conda activate donkey
$ pip install -e .[pc]
```

