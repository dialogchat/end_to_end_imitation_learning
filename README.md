# End-to-End Imitation Learning with the Udacity Simulator
## Overview

This code implements an autonomous car agent using Udacity's [self driving car simulator](https://github.com/udacity/self-driving-car-sim). The model is based on an end-to-end imitation learning algorithm as described in [NVIDIA's DaveNet2 paper](https://github.com/udacity/self-driving-car-sim).

## Dependencies

You will need a spedific version of Keras, Matplotlib .. to run this code. So the best way is to install everything into a virtual environment e.g. virtualenv.

Use Python 2.7 and install virtualenv
```
sudo apt-get install python-pip python-dev python-virtualenv
``` 
Create a virtualenv environment in terminal
```
virtualenv --system-site-packages car_simulation
```
Activate the virtualenv environment in terminal
```
source ~/car_simulation/bin/activate
```
Use TensorFlow with GPU
```
pip install tensorflow-gpu==1.0
```
Use TensorFlow without GPU
```
pip install tensorflow==1.0
```
Now install all other dependencies in the requirements.txt file:
```
pip install -r requirements.txt
```

## Usage


### Run the pretrained model

Start up [the Udacity self-driving simulator](https://github.com/udacity/self-driving-car-sim), choose a scene and press the Autonomous Mode button.  Then, run the model as follows:

```python
python drive.py model.h5
```

### To train the model

You'll need the data folder which contains the training images.

```python
python model.py
```

This will generate a file `model-<epoch>.h5` whenever the performance in the epoch is better than the previous best.  For example, the first epoch will generate a file called `model-000.h5`.

## Credits

The credits for this code go to [Udacity](https://github.com/udacity) and [naokishibuya](https://github.com/naokishibuya). I have contributed to this code by implementing some new model architectures.
