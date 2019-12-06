# The social evolution of cooperation

Henry Rachootin

The biological cooperation of evolution is fascinating, but it is also important to consider how cooperation emerges in social settings. The idea that biology is inherently competitive is widely believed but not particularly problematic, even if it is somewhat reductive. More often, the idea that society is or ought to be inherently competitive is a source of endless cruelty and ignorance. To remedy this, I investigate the question: **what factors can cause the natural emergence of cooperative behavior in a social network?**

In [2], Ohdaira  presents a model for social cooperation and selfishness. It is an evolutionary game theory networked prisoner's dilemma model, in which a network of agents play a single round of the prisoner's dilemma against each of their neighbors, then copy the strategy of their neighbor with the highest total score (or they don't change, if they have a higher score than their neighbors). The strategies are as simplistic as possible: they either always cooperate or always defect.

Ohdaira shows that added a 'decision cost' to the agents' strategies, which is a value chosen from a uniform distribution on [0, 1] which is subtracted from the agent's score after playing all of their rounds. This is meant to coarsely model the fact that different people justify their decisions to cooperate or defect in more or less complex ways, which makes their deliberation cost them more or less. This does nothing but hurt each agent proportional to their decision cost, but allows cooperation to dominate faster in ring lattice, Watts Strogatz [3], and Barabasi Albert [2] networks with average degree 4 than it does without the decision cost.

Odhaira uses a version of the prisoner's dilemma that rewards successful defection at `b=1.5` times the values of successful cooperation. I reproduced his result with a python implementation of the model, and further showed that with `b=1.67`, the introduction of the decision cost allows cooperation to dominate in all three networks, but defection dominates without it, as shown in Figures 1, 2, and 3.

![](https://raw.githubusercontent.com/sportsracer48/cooperation/master/code/rl.png)

Figure 1: Evolution of the ring lattice model with and without decision costs

![](https://raw.githubusercontent.com/sportsracer48/cooperation/master/code/ba.png)

Figure 2: Evolution of the Barabasi Albert model with and without decision costs

![](https://raw.githubusercontent.com/sportsracer48/cooperation/master/code/ba.png)

Figure 3: Evolution of the Watts Strogatz model with and without decision costs

Without any consideration for *why* people spend different amounts of time or resources considering their decisions, this shows that the mere fact that they *do* can allow cooperation to emerge naturally.

TODO: extension


[1] Barabasi AL, Albert R. Emergence of scaling in random networks. Science. 1999;286(5439):509-12.

[2] Ohdaira, T. Coevolution between the cost of decision and the strategy contributes to the evolution of cooperation. Sci Rep 9, 4465 (2019) doi:10.1038/s41598-019-41073-9. https://www.nature.com/articles/s41598-019-41073-9  

[3] Watts, Duncan J; Strogatz, Steven H., Nature (Jun 4, 1998): 440-2.
