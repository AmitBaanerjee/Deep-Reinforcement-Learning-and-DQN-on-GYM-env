# Reinforcement-Learning-using-OpenAI-Gym-Library
Implementation of Deep Q- Network on 2 of the OpenAI Gym environments which have been developed for  building reinforcement learning algorithms

Deep Q Network Using OpenAI’s Gym
Deep Q Learning can be defined as a modified method of implementing Q Learning by combining the independent nature of Reinforcement Learning with the efficiency of Deep Learning. Neural Networks can be added as an agent that learns to environment state-action pairs to rewards. Neural Network now works as a function approximator to relate the input values to the outputs. Generally, in order for the Neural Network to train, we allow the Network itself to fill the Q table based on its prior experiences inside the environment and then ask it to learn various paths towards the goal, based on these values.

Mountain Car Environment
Introduction
The ‘MountainCar-V0’ is an Environment designed and available to be used in OpenAI’s Gym packages. This environment consists of two mountains and a valley between them as the main environmental element, a car as the agent and a yellow flag that symbolizes the final goal that the car has to reach. A car is placed on a one-dimensional track, positioned between two ‘mountains’ i.e. inside the ‘valley’. The task of the car is to drive up the mountain on the right towards the goal. However, the car's engine is not strong enough to scale the mountain in a single pass. Therefore, the only way to succeed is to drive back and forth to build up momentum. This characteristic has to be learned by the agent i.e. the ‘car’ by trial and error using Deep Q Learning.

Analysis & Graph
The Reward vs Number of Timesteps graph provides following information:

The graph demonstrates a steady increase in rewards as number of timesteps increase. This demonstrates that the car is steadily exploring and trying to reach the goal.
The dips or decrease in the graph shows that the car i.e. the agent is not successful in reaching the goal. This may be due to various reasons such as the episode is completed or if the car goes into the wrong direction, etc.
Once, the agent reaches around 90000 timesteps, we can deduce that the exploration phase is completed and the car starts to perform exploitation over the environment. This is evident because the graph remains almost constant throughout the next 10000 timesteps.


* Total time taken to train the agent = 2196 seconds
Outputs

Ice Hockey Environment
Introduction
The ‘IceHockey-ram-v0’ is an Environment based on ‘Atari 2600 game Ice Hockey’ and available to be used in OpenAI’s Gym packages. This environment consists of an Ice Hockey playground and two nets at each end of the playground. Here the agent is a team of two hockey players and the goal is to score a greater number of nets that then other team in order to win the game. This is a more complex environment to learn from as the agent not only has to complete with the predefined player program and learn how to score more of the predefined program’s nets, but also at the same time defending its own net from being score by the predefined program. These characteristics has to be learned by the agent i.e. the ‘player’ by observing and learning from the other team using Deep Q Learning.

Graph
The Reward vs Number of Timesteps graph provides following information:

In the start of agents learning phase, the agent has no idea about the working of its environment and hence the agent loses to the other team. This is evident as the agent gains negative rewards in the graph.
After around 10000 steps the agent starts to learn the game and its characteristics and the graph demonstrates a steady increase in rewards as number of timesteps increase. This demonstrates that the agent’s team is scoring more goals against the other team.
Once, the agent reaches around 20000 timesteps, we can deduce that the exploration phase is completed and the car starts to perform exploitation over the environment. This is evident because the graph remains almost constant throughout the next 20000 timesteps.


Total time taken to train the agent = 1207 seconds
Outputs
  

