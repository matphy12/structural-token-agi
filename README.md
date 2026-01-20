# structural-token-agi
A minimal framework for AGI based on structural tokens, hypergraph reasoning, Transformer-based composition, and AlphaZero-style reinforcement learning.

---

English：

The basic idea of an AGI architecture can, in fact, be summarized in just a few statements. Of course, in practice, various concrete issues may arise and additional methods may be required for optimization:

1.Directly treat subgraphs of a hypergraph as structural tokens. Using a Transformer architecture, predict the next object (subgraph) to be used, conditioned on the current state of the reasoning chain.

2.Use an AlphaZero-style approach to optimize parameters. The key difference is that we allow network growth: existing parameters are kept fixed, and reinforcement learning is used to update the parameters of the expanded neural network.

3.The internal reasoning chains of important subgraphs (i.e., subgraphs themselves), together with the subgraphs appearing inside reasoning chains, are used for training, so that they are gradually internalized into stable structures.

The reward function includes, but is not limited to, the following components:

Compression gain: after introducing a new object or a new composite morphism, how much the average length of reasoning chains is reduced (rewarding “shortcut” effects similar to those provided by the Fundamental Theorem of Calculus).

Stability score: structures that are less sensitive to perturbations receive higher scores, in order to filter out stable structures.

Reuse frequency: the frequency with which a given structure repeatedly appears across different reasoning tasks.

---

中文：

AGI的架构的基本思想，总结下来其实可能就这么几句话，当然，实践过程中可能会遇到一些具体的问题需要解决或者采用一些新方法来优化：

1、直接把超图的子图作为结构 token，用Transformer的架构，在当前推理链状态下预测下一步要使用的对象（子图）。

2、用AlphaZero的方法优化参数，区别在于我们允许神经网络的增生，方法是先保持原有参数，再用强化学习更新增生后的神经网络的参数。

3、重要子图的内部推理链（子图）与推理链内部的子图用于训练，使其逐步化为稳定结构。

奖励函数包括但不限于：

压缩增益：引入某个新对象/新复合态射后，平均推理链长度下降多少（奖励微积分基本定理那样“短路”情况）

稳定性得分：越不容易被扰动的得分越高，以筛选出稳定的结构

复用率：某结构在不同推理任务下反复出现的频率。
