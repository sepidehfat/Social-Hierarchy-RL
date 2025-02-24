# Social-Hierarchy-RL

A reinforcement learning paradigm using openAIs multi-agent RL Gym environment to simulate the emergence of a hierarchy among agents as a result of an environment with constrained resources and penalties for competing (fighting) for scarce resources.

The code includes an environment class based on the OpenAI Gym library, a DQN agent class, as well as a training loop.

## Abstract: 
Social hierarchies are an ubiquitous feature in both human societies and countless other animal species. They structure the behavior of groups and individuals by determining, for example, resource allocation and conflict resolution. In this study, we explore the dynamics of social hierarchy in a simple simulated environment. Accordingly, our central question is how hierarchies emerge. We operationalize the emergence of social hierarchies as follows: Over time, the agents attain progressively unequal amounts of rewards, and simultaneously, their engagement in conflicts over available resources diminishes.
To answer, how hierarchies emerge, we built a 10 by 10 grid environment using the gym and pettingzoo API with limited "food" resources and ten agents with a discrete action space (up down, left, right, stay) which are trained with reinforcement learning. In this multi-agent reinforcement learning (MARL) setup, we use Deep Q Network (DQN) agents who act based on an epsilon greedy algorithm. To investigate the emergence of social hierarchies in this controlled setting, the agents are positively reinforced for eating food, get in “conflicts” with other agents when they try to eat the same food simultaneously, and are negatively reinforced if they lose the resulting conflict. While winners of individual conflicts are choosen randomly, each agent maintains a preference for fighting or submitting to other agents when a conflict arises over food allocation. Following conflicts, these preferences are updated via elementary policy gradient techniques.
We hypothesize that a social hierarchy emerges even in such simple environments with limited resources. If our hypothesis is confirmed, this would suggest that social hierarchies are not a human phenomenon but instead a very general phenomenon that emerges by default in environments in which agents maximize their own reward by consuming limited resources.
Future studies should investigate how different agents, different environmental conditions and opportunities for cooperation influence the development of social hierarchies.
