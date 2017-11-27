# End-to-End Imitation Learning with the Udacity Simulator
## Overview

This code implements an autonomous car agent using Udacity's [self driving car simulator](https://github.com/udacity/self-driving-car-sim). The model is based on an end-to-end imitation learning algorithm as described in [NVIDIA's DaveNet2 paper](https://arxiv.org/abs/1604.07316).

## Dependencies

You will need a spedific version of Keras, Matplotlib etc.. to run this code. So the best way to install without touching your config is to put everything into a virtual environment e.g. virtualenv.

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

Download and start up [the Udacity self-driving simulator](https://github.com/udacity/self-driving-car-sim), choose a scene and press the Autonomous Mode button.  Then, run the model in terminal as follows:

```python
python drive.py model-006.h5
```
The model should give you good performance on the lake track and bad performance on the jungle track. (Was trained for 20 min, 10 epochs on the lake track).

### To train the model

Once you created your IMG and driving_log.csv data in the /data directory you can start to train your model.
Before that you can go into model.py and create your own model, tune hyperparameter etc... that's were your creativity comes into play...

```python
python model.py
```

This will generate a file `model-<epoch>.h5` whenever the performance in the epoch is better than the previous best.  For example, the first epoch will generate a file called `model-000.h5`.

## Credits

The credits for this code go to [Udacity](https://github.com/udacity) and [naokishibuya](https://github.com/naokishibuya). I have contributed to this code by implementing some new model architectures.
