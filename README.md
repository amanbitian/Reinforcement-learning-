# Reinforcement-learning-
![1_mjxLmTZkNFLjI6A807hcNg](https://user-images.githubusercontent.com/86042628/143725107-b144312f-807c-4794-99b5-fbb5873abd49.png)

## 1. Key Elements of Reinforcement Learning
![electronics-09-01363-g001](https://user-images.githubusercontent.com/86042628/143725108-d4380ac3-92dc-4e29-99dc-2578e0045114.png)

1. ***Environment*** — Physical world in which the agent operates
2. ***State*** — Current situation of the agent
3. ***Reward*** — Feedback from the environment
4. ***Policy*** — Method to map agent’s state to actions
5. ***Value*** — Future reward that an agent would receive by taking an action in a particular state

## 2. Types of Reinforcement: There are two types of Reinforcement: 
 

### Positive – 
Positive Reinforcement is defined as when an event, occurs due to a particular behavior, increases the strength and the frequency of the behavior. In other words, it has a positive effect on behavior. 

    Advantages of reinforcement learning are: 
        * Maximizes Performance
        * Sustain Change for a long period of time
        * Too much Reinforcement can lead to an overload of states which can diminish the results
 
### Negative – 
    Negative Reinforcement is defined as strengthening of behavior because a negative condition is stopped or avoided. 

    Advantages of reinforcement learning: 
        * Increases Behavior
        * Provide defiance to a minimum standard of performance
        * It Only provides enough to meet up the minimum behavior

`Various Practical applications of Reinforcement Learning –` 
 

    RL can be used in robotics for industrial automation.    
    RL can be used in **machine learning and data processing
    RL can be used to create training systems that provide custom instruction and materials according to the requirement of students.

RL can be used in large environments in the following situations: 
 

1. A model of the environment is known, but an analytic solution is not available;
2. Only a simulation model of the environment is given (the subject of simulation-based optimization)
3. The only way to collect information about the environment is to interact with it.

# 3. What is q-learning?
Q-learning is an ***off policy reinforcement learning algorithm that seeks to `find the best action to take given the current state`.*** It’s considered off-policy because the q-learning function learns from actions that are outside the current policy, like taking random actions, and therefore a policy isn’t needed. More specifically, q-learning seeks to learn a policy that maximizes the total reward.
**What’s ‘Q’?**  
The ‘q’ in q-learning stands for quality. Quality in this case represents `how useful a given action` is in gaining some future reward.
In Other words *Q-values (also called action values) to iteratively improve the behavior of the learning agent.*

i. **Q-Values or Action-Values:** Q-values are defined for states and actions. Q(S, A) is an estimation of how good is it to take the action A at the state S. This estimation of Q(S, A) will be iteratively computed using the TD- Update rule which we will see in the upcoming sections.

ii. **Rewards and Episodes:** An agent over the course of its lifetime starts from a start state, makes a number of transitions from its current state to a next state based on its choice of action and also the environment the agent is interacting in. At every step of transition, the agent from a state takes an action, observes a reward from the environment, and then transits to another state. If at any point of time the agent ends up in one of the terminating states that means there are no further transition possible. This is said to be the completion of an episode.

iii. **Temporal Difference or TD-Update:**
The Temporal Difference or TD-Update rule can be represented as follows :

![TD_Update-300x30](https://user-images.githubusercontent.com/86042628/143725309-4f193591-bbfc-4e71-9398-e9fa0b1542bd.jpg)


This update rule to estimate the value of Q is applied at every time step of the agents interaction with the environment. The terms used are explained below. :

     S : Current State of the agent.
     A : Current Action Picked according to some policy.
     S' : Next State where the agent ends up.
     A' : Next best action to be picked using current Q-value estimation, i.e. pick the action with the maximum Q-value in the next state.
     R : Current Reward observed from the environment in Response of current action.
     $\gamma$(>0 and <=1) : Discounting Factor for Future Rewards. Future rewards are less valuable than current rewards so they must be discounted. Since Q-value is an estimation of expected rewards from a state, discounting rule applies here as well.
     $\alpha$ : Step length taken to update the estimation of Q(S, A).

iv. **Choosing the Action to take using $\epsilon$-greedy policy:**
$\epsilon$-greedy policy of is a very simple policy of choosing actions using the current Q-value estimations. It goes as follows :

With probability (1-$\epsilon$) choose the action which has the highest Q-value.
With probability ($\epsilon$) choose any action at random.

[Read more GeekforGeek](https://www.geeksforgeeks.org/q-learning-in-python/)  
[Towards data science](https://towardsdatascience.com/simple-reinforcement-learning-q-learning-fcddc4b6fe56)
