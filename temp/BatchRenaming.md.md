# Steps of donkey car
In this part we will start from how to install packages to training neural network as well as how to utilize this tool.

## The following tutorial is based on Linux Ubuntu system


The official website of donkey car:
https://docs.donkeycar.com/

## Install Software On Donkeycar



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
Optional Install Tensorflow GPU - only for NVidia Graphics cards!!!

```sh
$ conda install tensorflow-gpu==2.2.0
```


## Install donkey car simulator
https://docs.donkeycar.com/guide/simulator/

Install

```sh
$ cd
$ cd project
$ git clone https://github.com/tawnkramer/gym-donkeycar
$ cd gym-donkeycar
$ conda activate donkey
$ pip install -e .[gym-donkeycar]

```

You may use an existing ~/mycar donkey application, or begin a new one. Here we will start fresh:

```sh
$ donkey createcar --path ~/mysim
$ cd ~/mysim

```
Edit your myconfig.py to enable donkey gym simulator wrapper, replace <user-name> and the other parts of the path:

```sh
$ DONKEY_GYM = True
$ DONKEY_SIM_PATH = "/home/<user-name>/projects/DonkeySimLinux/donkey_sim.x86_64"
$ DONKEY_GYM_ENV_NAME = "donkey-generated-track-v0"
```

## Start driving to collect training data
  
  
## Train Neural network
  
## How to use pre-trained model to simulate the donkey car

Please first go to the directory of mysim and use the virtue environment
  
```sh
$ python manage.py drive --model= /home/xxxxxbase on your the directory of your model
```
It will pops up the screen of the simulator.
  
Open your browser( Here I use is Google Chrome), and type 
  
  ```sh
$ <IP address of host PC>:8887
```

