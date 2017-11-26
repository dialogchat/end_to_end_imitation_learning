# End-to-End Imitation Learning with the Udacity Simulator
## Overview

This is the code for [this](https://youtu.be/EaY5QiZwSP4) video on Youtube by Siraj Raval. We're going to use Udacity's [self driving car simulator](https://github.com/udacity/self-driving-car-sim) as a testbed for training an autonomous car. 

## Dependencies

You will need a spedific version of Keras, Matplotlib .. to run this code. So the best way is to install everything into a virtual environment e.g. virtualenv.

# Use Python 2.7 and install virtualenv
```sudo apt-get install python-pip python-dev python-virtualenv``` 
# Create a virtualenv environment in terminal
```virtualenv --system-site-packages car_simulation```
# Activate the virtualenv environment in terminal
```source ~/car_simulation/bin/activate```
# Use TensorFlow with GPU
```pip install tensorflow-gpu==1.0```
# Use TensorFlow without GPU
```pip install tensorflow==1.0```

Now install all other dependencies in the requirements.txt file:
```pip install -r requirements.txt```

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

The credits for this code go to [naokishibuya](https://github.com/naokishibuya). I've merely created a wrapper to get people started.
