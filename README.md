# Collaboration-and-Competition
A deep reinforcement learning approach to a multi-agent system
### Introduction
![](Uploads/tennis.gif)

This environment has two agents, each controlling a racket. Hitting a ball over the net returns a reward of +0.1 to the given agent. Letting the ball hit the ground or go out of bounds returns a reward of -0.01. Thus, the reward structure is such that each agent wants to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives a local observation, independent of the other agent. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

This task is episodic, and, after each episode, we sum the total rewards for the two respective agents and take the maximum of the 2 scores, yielding a single score for each episode. The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

### Initialization
 1.) Clone this repository
 
 2.)
