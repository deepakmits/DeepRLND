
## Project 2 - Continuous Control - 
Train a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.
## Solution - 
This solution is based on the DDPG algorithm, improvised on ddpg-pendulum session. The agent reaches an average score of 30 after 108 episodes. It uses actor critic method where each action taken by actor network is sort of evaluated by the critic network. Actor network is fully connected 2 hidden layers of 128 nodes each and critic network has fuly connectedd 400 and 300 nodes 2 hidden layers.Both actor and critic networks trained with a learning rate of **0.001**, using mini-batches of **256**, a replay buffer of **100000**, and a discount of **0.9**. The Ornstein-Uhlenbeck noise has a sigma of **0.1** and the soft update is made using a tau of **0.001**.
The training seems to be fairly stable for a RL task. The score kept on improving after the goal was reached.

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
Tryng the task using PPO and compare how both algorithms perform.
