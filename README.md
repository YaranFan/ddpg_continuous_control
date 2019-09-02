# Continuous Control - Reacher Environment
This project solves the continuous control problem for the Reacher environment with Deep Deterministic Policy Gradients (DDPG).

## Project Details
We are working with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment in this project. Here is a simple summary of the environment:

* Set-up: Double-jointed arm which can move to target locations.
* Goal: The agents must move its hand to the goal location, and keep it there.
* Benchmark: the problem is considered solved when the average reward across all agents over 100 episodes is 30+. 
* Agents: There are two versions. The environment contains 1 or 20 agent linked to a single Brain.
* Agent Reward Function (independent):
  * +0.1 Each step agent's hand is in goal location.
* Brains: One Brain with the following observation/action space.
  * Vector Observation space: 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm of the two arm Rigidbodies.
  * Vector Action space: (Continuous) Size of 4, corresponding to torque applicable to two joints.
  * Visual Observations: None.

## Getting Started
1. Clone this repository.
2. Follow the instructions in [the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to install necessary packages and set up your environment
3. Download and unzip the Unity Environment.
    * Version 1: One (1) Agent
        * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip
    * Version 2: Twenty (20) Agents
        * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
        * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
        * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

## Instructions - How to use this Repository
This repository focuses on solving the V2 environment, which contains 20 agents. However, since we can treat V1 as a simplified version of V2, we can solve it with the same scripts that are provided here.

To train an agent or watch a smart agent, you only need to modify the [Continuous_Control.ipynb](Continuous_Control.ipynb) file from this repository. 
1. In part II. Environment, change the file path to ```env = UnityEnvironment(file_name=PATH_TO_THE_ENV)```. The ```PATH_TO_THE_ENV``` is the path to the app from you unzipped folder from Step 3 in Getting Started.
2. If you want to train an agent from scratch, set ```train_model = True``` in part III. Train an Agent.
3. If you just want to watch a smart agent, set ```train_model = False``` in part III. Train an Agent. The script will load the smart agent’s model weight from a pre-trained model.
4. For details about the model and the agent, please refer to [ddpg_agent.py]( ddpg_agent.py) and [model.py](model.py).

