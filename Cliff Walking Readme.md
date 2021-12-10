## CLIFF WALKING

## DOCUMENTATION MANUAL

Cliff Walking:
The implementation of SARSA and Q-learning, as well as the comparison of resultant agent behaviors between these two approaches, will be the focus of the next sections.

In a nutshell, the Cliff class will represent the board and will be able to:
>Keep track of where an agent is right now.
>Determine the agent's next move and if the game is over when given an action.
>As a reward, provide feedback.

These are the most important functions in the Cliff class. The nxtPosition function accepts an action and returns the agent's next location on the board; if the agent runs into a wall (reaches the boundary), it stays in the same place.

HERE,IS OUR CLIFF

![1_zpwb_n5V5BNNfbfCk5i8Tw.png](attachment:1_zpwb_n5V5BNNfbfCk5i8Tw.png)

Q-learning learns values for the best policy, the one that travels right up to the cliff's edge. Unfortunately, as a result of the "epsilon-greedy" action selection, it periodically falls off the cliff. SARSA, on the other hand, considers the action chosen and learns the longer but safer way via the grid's top reaches.

Despite the fact that Q-learning learns the values of the optimum policy, it performs worse online than SARSA, which learns the roundabout policy. Of course, both techniques would asymptotically converge to the optimal policy if were steadily lowered.

SARSA:
![1_tOL0d-fufdWdE8mC7Dk21Q.png](attachment:1_tOL0d-fufdWdE8mC7Dk21Q.png)


Q-lEARNING:

![1_3R7eX6N6P1yFOVQwJ7jJGw.png](attachment:1_3R7eX6N6P1yFOVQwJ7jJGw.png)


```python

```
