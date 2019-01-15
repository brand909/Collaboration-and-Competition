# Collaboration-and-Competition
A deep reinforcement learning approach to a multi-agent system
## Introduction
![](Uploads/tennis.gif)

This environment has two agents, each controlling a racket. Hitting a ball over the net returns a reward of +0.1 to the given agent. Letting the ball hit the ground or go out of bounds returns a reward of -0.01. Thus, the reward structure is such that each agent wants to keep the ball in play. The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives a local observation, independent of the other agent. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. This task is episodic, and, after each episode, we sum the total rewards for the two respective agents and take the maximum of the 2 scores, yielding a single score for each episode. The environment is considered solved when the average (over 100 episodes) of those scores is at least +0.5. I implemented a deep deterministic policy gradient algorithm using pytorch to reach this average score.

![](Uploads/ddpg_algorithm)

## Initialization

1.) Select the environment that matches your operating system:
 
•Linux: [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
•Mac OSX: [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
•Windows (32-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
•Windows (64-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

(For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)


2.) Create (and activate) a new environment with Python 3.6, enter the following in the terminal:

Linux or Mac:
#
conda create --name drlnd python=3.6
source activate drlnd
#
Windows:
#
conda create --name drlnd python=3.6 
activate drlnd
#

3.) Clone the repository and navigate to the python/ folder. Then, install several dependencies:
#
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
#

4.) Create an IPython kernel for the drlnd environment:
#
python -m ipykernel install --user --name drlnd --display-name "drlnd"
#

5.) Before running code in a notebook, change the kernel to match the drlnd environment by using the drop-down Kernel menu:

![](Uploads/kernel.png)

## Implementation

To solve this, it's recommended that you use an actor-critic agent. I used a deep deterministic policy gradient (DDPG) algorithm, but there are other approaches. You can read about the DDPG algorithm [here](https://arxiv.org/pdf/1509.02971.pdf). The code for DDPG can be found in the file [agent.py](https://github.com/brand909/Collaboration-and-Competition/blob/master/agent.py), the neural network models can be found in the file [model.py](https://github.com/brand909/Collaboration-and-Competition/blob/master/model.py). See the implementation of the algorithm and its resulting scores in [Tennis.ipynb](https://github.com/brand909/Collaboration-and-Competition/blob/master/Tennis.ipynb) and [my report here](https://github.com/brand909/Collaboration-and-Competition/blob/master/REPORT.md).

 
 
