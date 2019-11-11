# The social evolution of cooperation

Henry Rachootin

While the biological evolution of cooperation is interesting and important to understand, the social evolution of cooperation may be more relevant to the modern world. The idea that people are inherently selfish is shockingly common and constantly used to justify all manners of heinous behavior. Similarly to how agent based models can demonstrate the emergence of altruism in biological systems, they can show how it comes about in social networks. Similarly to [1], I will draw on this social/biological metaphor to show that people, even 'rational' self interested people, can be inherently cooperative, with cooperative behaviors arising naturally from selective pressures under certain conditions.

I will start by replicating the experiment from [2], which shows how having a cost for decision making in scale free social networks is adaptive and coupled to cooperativity. Ohdaira's model uses evolutionary game theory and a networked iterated prisoner's dilemma (IPD). I will implement the same model in python. The goal will be a cooperativity vs time graph (with cooperativity measured by the frequency of cooperation among all the agents), and the experiment will be replicated if it increases to a mostly cooperative population.

To extend this model, I will allow the agents to communicate their strategies to each other, in order to model the way that memes spread in short time scales (less than a generation) in the real world. I'm a bit concerned that I don't have a clear understanding of how to implement this memetic spread, but I have a feeling it will be illuminating, as it is analogous to the jump from individual competition to genetic competition, as described in [1].

My first move is to read [2] thoroughly and implement Ohdaira IPD model.

[1] Dawkins, Richard, 1941-. The Selfish Gene. Oxford ; New York :Oxford University Press, 1989.

Dawkins presents the genetic model of evolution, and demonstrates that it describes many of the phenomena of biology much better than an individual model of evolution. He posits that it is not individuals that are fit in an environment, but genes and genomes in an environment and population. He also compares the genes of biology to the memes of culture, showing how this information based approach is applicable in more situations.

[2] Ohdaira, T. Coevolution between the cost of decision and the strategy contributes to the evolution of cooperation. Sci Rep 9, 4465 (2019) doi:10.1038/s41598-019-41073-9. https://www.nature.com/articles/s41598-019-41073-9  

Ohdaira uses a spatially arranged, evolutionary, agent based, prisoner’s dilemma model to demonstrate the relationship between cooperation and the cost of decision making. The model assumes that each agent uses some time or resource to make a decision, while playing with its neighbors. When the cost of decision making is added to the game, cooperation emerges, but the extent to which the cost influences the cooperativity depends on the network topology and connectedness. Particularly, in scale-free topologies, players with high cost of decision dominate, and are cooperative.
