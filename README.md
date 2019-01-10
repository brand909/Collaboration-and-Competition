# Collaboration-and-Competition
A deep reinforcement learning approach to a multi-agent system
### Introduction
![](Uploads/tennis.gif)

In this environment, two agents control rackets respectively to bounce a ball over a net. Hitting a ball over the net returns a reward of +0.1 to the given agent. Letting the ball hit the ground or go out of bounds returns a reward of -0.01. Thus, the reward structure is such that each agent wants to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.
