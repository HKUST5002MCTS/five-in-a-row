# five-in-a-row
this reciprotary is just for our group to upload the file or some references you think are useful <br>
you can directly put the website link here

the original part of MCST we use:https://github.com/zhuliquan/tictactoe_mcts

a new meaningful website https://ai-boson.github.io/mcts/, it clearly shows the structure of how to set the MCTS for 5-in-a-row game. you'd better see it carefully

## Li,Qichao
#### 30/11/2021--Group-7-2nd-version
recently, I try some strategies<br>
1. I limit the span tree into the adjacent places so as to reduce the inefficient effort(since in five-in-a-row game, it almost useless to add piece remote from the existing nodes). As a result, the depth of the MCST increase to 3(used to be less than 2, the complexity is O(k^n)) and we only add the new piece around the existing places each time. However, the AI still performs badly, and even do not know how to play when there are already 4 pieces existed.
2. I try to record the path of the rollout proccess(expand the tree when rolling out). However, it does not improve the performance of AI. Even worse, it reduces the the number of simulation times since the rollout way is not light anymore.
3. I try to reset the score we get each time we finish the game.(the way with fewer steps gets higher score: score = 20/depth), it seems a little bit useful, but still not block the player when the player has already had the 3-in-row situation.

# Notice:
12.1~
The next step is just to read some articles and try to use them in our own models

## Yang, Luyuan
#### 30/11/2021--Group-7-add parallel.ipynb
What I have done: added multi-threading ；
Achieve: now each time, it will simulate 1000 times.(the final print is the total simulation times) ；
Need to change: add strategy to 堵三子； 继续优化树，感觉1000次的模拟仍然不够！！

## Huang, Suizi
#### 01/12/2021--Group-7-add 3-in-a-row.ipynb
What I have done: added 3-in-a-row strategy
Achieve: It can block when 3 stones in a row, but still might not be in the best way ；
Need to change: Should we add more situations such as 4-in-a-row?

## Li, Qichao
#### 08/12/2021--Group-7-6th version.ipynb
What I have done: add the limit score and the strategy in rollout part<br>
Achieve: It seems to have the ability to create 3,3 situation by itself；<br>
Need to change: choose the suitable score and speed up the get_pos strategy.<br>

