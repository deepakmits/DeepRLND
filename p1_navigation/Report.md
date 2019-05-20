## Project 1 - Navigation - Traning DeepRL agent to collect yellow bananas.
Solution - Average score of 13+ rewards across 100 consecutive episodes achieved with 403 episodes.
Environment Used - Banana.app from Unity.
Envrironment has 37 states with 4 discrete actions.

### Learning Algorithm Used - DQN - 
1) Vanilla Deep Q-Learning Network from DQN session used. 
2) Network Architecture And Hyperparamenters - 
    Number of hidden layers - 2 each with 64 neurons, <br>
    Activation function used RELU, <br>
    BATCH_SIZE = 64         # minibatch size <br>
    GAMMA = 0.99            # discount factor <br>
    TAU = 1e-3              # for soft update of target parameters . <br>
    LR = 5e-4               # learning rate <br>

### Plot of Rewards - 

![Rewards](images/Rewards.png "Rewards")


### Improvements - 
With more hyperparameters tuning and some network architecture changes, number of episodes required can be reduced.<br>
Currently plain DQN has been used, other option to try out is Rainbow and Double DQN, to see the improvements.




