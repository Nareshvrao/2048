# 2048

Play: https://nareshvrao.github.io/2048/

Abstract
2048 is a very popular online game. It is very easy but hard to achieve its goal.
Therefore we decided to develop an AI agent to solve the game. We explored two
strategies in our project, one is ExpectiMax and the other is Deep Reinforcement
Learning. In ExpectiMax strategy, we tried 4 different heuristic function and combined
them to improve the performance of this method. In deep reinforcement learning, we
used sum of grid as reward and trained two hidden layers neural network. We achieved
98% in 2048 with setting depth limit to 3 in ExpectiMax method. But we didn’t
achieve a good result in deep reinforcement learning method, the max tile we achieved
is 512.

Introduction

Game 2048 is a popular single-player online game developed by Italian programmerGabriele Cirulli.
2048 is an online addictive single-player video game invaded the Internet in 2014. One
of reasons for the popularity of this game is that it is so easy but hard to win. It is not easy
for a human to get the final tile 2048 to win the game. However, we could build an Artificial
Intelligence game solver to help us get the highest score that human could not achieve.
In terms of the problem topic for 2048, we could view it from two aspects. Some people
believe it is a search problem and implement algorithms, such as expectimax, minimax
[1][2]. On the other hand, some view it as a learning problem and build a game solver with
reinforcement learning method, such as temporal difference learning, Q-learning[3][4].
In particular, the method used expectimax in [1] is to treat the game as adversarial.
The opponent is the computer and it will place the new tile on the board randomly. AI will
choose the maximum of the expected scores of the next states. However, we need to choose
weight matrix for evaluation function wisely, since it is very important for the next decision.
According to the result for [2], which uses the number of open tiles and heavy weight on
the edge as heurists, it achieved highest tile of 32768 for 36% of trials under limited search 1
depth of 8. But it need to think 150ms each move, which means the runtime for this method
is very large if we want to get high performance. In[1], the author compares Monte-Carlo
tree-search and expectimax depth-limited search. Since Monte-Carlo search do not have
any domain knowledge, it performs worse than expectimax search, which is given evaluation
function that rewards board properties.


2 Approaches
In the first part of projecrt, we implemented ExpectiMax search methods and improved
them with human heuristics. Since the search tree would expand exponentially, we tried to
use the depth-limited search to max performance in a limited computation resource. At last,
we attempted to use deep reinforcement learning with simple neural network. The neural
network was used to learn Q value for each state. However, training model is computationally
expensive for my laptop and the limited time, my performance is not very well. Although it
is better than human player, but not better than search trees.
