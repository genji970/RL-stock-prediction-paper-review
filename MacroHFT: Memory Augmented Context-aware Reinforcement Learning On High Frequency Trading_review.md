https://arxiv.org/abs/2406.14537

Abstract : High dimensional and sophisticated sequential time series makes model to overfit easily \-\> Lack of generalization

use sub agent was proposed. But still choosing one sub agent that is suitable for model prediction is just another high biased, overfitting. Volatile markets make data drifting causing overfitting.

Introduction : Regarding crypto market as uniform , stationary makes model to overfit.

Main text: This paper suggests with low policy trained sub agents, incorporating them and by using softmax, makes new high dimensional hyper agent that decides cryptocurrency movement.  
There are two special vectors. First, trend. Second, volatility.

Putting condition vector into MLP and use logits for shift, chunk, scale criteria

Market Decomposition : For trend, Eliminating noise and slope from linear regression becomes an indicator of market trend.  
                       For volatility, avg volatility for each original non filtered(non filtered, using fluctuations)

Policy optimization : using argmax for action space in Loss function and temporal difference is better than monte carlo estimation since it updates fast during the traininig but it easliy  
overfit since Q \-\> apparantely good reward easily.(Sac can be used but in the stock market, just a few prob change can be resulted in a bad situation, Also have to think about commission fee)

Hence, this paper suggests Meta policy optimization with memory augmentation. 

This paper also points out rapid change of reward signal due to data drifting. It looks like RL's target divergence. RL so do soft update, update target network a little to fix a convergence point for a while.   
But as mentioned, due to stock market's butterfly effect, it is uneasy, unstable.

key is a main factor in calculating attention weight. And it is calculated by L2 distance. It is different from value itself which is consist of reawrad and Q value. But wtill, it somehow is related to reward.  
Still hard to solve overfitting proble itself. But by online learning? and finite capicity memory, it reflects current movement. But still there's a question that it can prevent very first fluctuation? I dont know  
