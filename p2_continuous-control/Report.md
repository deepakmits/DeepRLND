
## Project 2 - Continuous Control - 
Train a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.
## Solution - 
Average score of 30+ rewards across 100 consecutive episodes achieved with 108 episodes.
Environment Used - Reacher.app from Unity. <br>
Environment Info - The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Learning Algorithm Used - DDPG - 
1) Improvised on DDPG-PENDULUM Session. 
2) Network Architecture And Hyperparamenters - 
    Actor - Number of hidden layers - 2 each with 128 neurons <br>
    Critic - Number of hidden layers - 2 one with 400 and other with 300 neurons <br>
    BUFFER_SIZE = 100000            # replay buffer size <br>
    BATCH_SIZE = 256                # minibatch size <br>
    GAMMA = 0.9                     # discount factor <br>
    TAU = 1e-3                      # for soft update of target parameters <br>
    LR_ACTOR = 0.001                # learning rate of the actor <br>
    LR_CRITIC = 0.001               # learning rate of the critic <br>
    WEIGHT_DECAY = 1e-6              # L2 weight decay <br>

### Plot of Rewards - 

![Rewards](images/cc.png "Rewards")


### Improvements - 
With more hyperparameters tuning and some network architecture changes, number of episodes required can be reduced.<br>
Try solving the task using PPO and compare how both algorithms perform.
