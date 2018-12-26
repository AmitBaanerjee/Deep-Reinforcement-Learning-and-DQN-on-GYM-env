  --------------------------------------------------------
  **Project 4 Bonus: OpenAI Gym Library Implementation**
  --------------------------------------------------------

**Amit Banerjee**

UBIT Name: amitbane

Person ID:50287084

*amitbane@buffalo.edu*

**Abstract**

The objective of this project is implementation of Deep Q Network using
two environments of OpenAI’s Gym Library. For this project, we have
implemented the Mountain car v0 environment and Ice Hockey ram v0
environment using DQN. The output of DQN for both these environments is
that the agent is able to learn from the environment settings and after
a set number of iterations it progresses towards the intended goal. The
above stated observations are shown using graphs and figures in the
subsequent sections.

**1 Introduction**

Reinforcement learning is a subsection of machine learning which
consists of states and actions rather than input variables and target
sections as present in other sections of machine learning such as
supervised learning and unsupervised learning. A typical reinforcement
learning algorithm uses the Q-values which are stored from previous
experiences and calculates the optimum step for next states. Using DQN
is an approach which combines deep learning and reinforcement learning
algorithms together. The states and actions are fed inside the neural
network and the network learns relations regarding steps which will give
maximum rewards versus the steps which make the agent move away from the
goal. In the end of training period, the agent is made to move on the
environment to see if he can reach the required target after the
training period of our neural network model.

The gym library is a collection of test problems and environments that
you can use to work out your reinforcement learning algorithms. These
environments have a shared interface, allowing you to write general
algorithms

**2 Implementation**

**2.1 Mountain Car Environment**

For first part of the project, we made the agent explore and interact
with the mountain car environment of OpenAI. The mountain car
environment description is that there is a car on on a one-dimensional
track, positioned between two mountains. The goal is to drive up the
mountain on the right. However, the car's engine is not strong enough to
scale the mountain in a single pass. Therefore, the only way to succeed
is to drive back and forth to build up momentum and reach the top of the
second mountain.\[1\] To figure out how back the car needs to go to get
a momentum for reaching the target is a task of reinforcement learning.
The model is being trained on a DQN using a layer normalized multi-layer
perceptron policy. The outputs of trained DQN model are as follows: -

  ![](media/image1.tiff){width="2.7308081802274717in" height="1.8315726159230097in"}   ![](media/image2.tiff){width="3.0101859142607172in" height="2.0128718285214346in"}
  ------------------------------------------------------------------------------------ ------------------------------------------------------------------------------------
  ![](media/image3.tiff){width="2.810945975503062in" height="1.8835465879265092in"}    ![](media/image4.tiff){width="2.8994619422572177in" height="1.9271172353455819in"}

Fig 1: Output of Mountain car environment

*Observations: -*

-   The outputs which are present in figure 1 are the training images of
    the model. It can be seen that the agent tries to take multiple
    steps back and forth initially to learn the environment. In the
    initial steps, it is not able to reach the target as it does not
    have a clear idea of how much momentum is required to reach the
    target. But after a set number of iterations, it gains a clear idea
    of what steps need to be taken to reach the target. The rewards
    received in the previous steps give it a clear idea of what needs to
    be done and in the later iterations it reaches the goal more
    frequently.

![](media/image5.tiff){width="3.9903674540682417in"
height="2.8300371828521436in"}

Figure 2: Time steps vs Reward Graph

-   From figure 2 it can be inferred that during the initial time steps
    the model does not receive much positive rewards but in later
    stages, as it understands the model better the rewards keep
    increasing. The convergence point is reached at around 45000 steps
    as we can see the reward is maximum at that particular point. After
    that point of time, it again starts to explore the environment to
    find a better policy hence the graph slope starts dropping from that
    point onwards.

-   For training the model on 50000 time steps, the time taken was
    1525.17 seconds. Increasing the number of time steps will make the
    model train slower and learn to many more converges. It was seen
    that the car reaches the target many times. Hence reducing the
    number of steps will also lead to faster results and the car will
    still reach the intended goal using the MLP policy being used with
    DQN.

**2.2 Ice Hockey Environment**

For the second part of the project, we made the model train an interact
with the Atari ice hockey environment. The environment states that there
are two computer simulated hockey opponents who try to score goals
against the agent. The agent needs to defend against the opponents who
try to score a goal against them and try to counter them by scoring in
their net.\[2\] The DQN model is trained to make the agent learn better
about the environment and try to understand the concept of what the goal
and what rewards will be awarded for winning the game and losses for
letting the opponent score any goal.

The outputs of the DQN trained model are as follows: -

  ![](media/image6.tiff){width="2.4487007874015747in" height="3.1054407261592303in"}
  ------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------
  ![](media/image8.tiff){width="2.405518372703412in" height="3.0981572615923008in"}

Fig 3: Output of Atari Ice Hockey Environment

-   As it can be seen from the outputs of figure 3 above, the agent
    struggles against the opponents in the first initial iterations and
    as a result the opponent were able to score goals before the agent.
    But after a few iterations, it can be seen that the agent is able to
    defend against the opponent and is also able to score a goal. This
    shows that the agent is able to learn more and more about the
    environment as time progresses and hence perform better.

![](media/image9.png){width="3.939825021872266in"
height="2.847916666666667in"}

> Fig 4: Time step vs Reward graph for Atari environment

-   It can be seen from figure 4 above that 50000 iterations is not
    enough for the agent to find an optimal state-value function for
    such a complex environment. As a result, the agent is not able to
    understand whether the reward received is the most optimal reward
    and hence after end of each episode it tries to explore more states
    and actions and as a result the reward keep dropping after every
    peak. If the number of iterations are increased, the model will
    converge better and there will be a more consistent graph.

-   The total time required for the model to train is 1207 seconds. As
    stated in the previous point, it is not enough to find an optimum
    convergence point. Hence the model did not perform well for 50000
    steps and the number of time steps, iterations need to be increased.

**3 Conclusion**

It can be concluded that the both the environments were implemented
successfully using DQN and OpenAI’s Gym package.
