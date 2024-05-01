# Project Background
Protein deficiency and poverty in the Philippines is a an alarming issue, especially among children and pregnant women. Limited access to protein-rich food contributes to malnutrition and stunted growth, affecting health and development while also worsening poverty in the long term. To tackle this issue, citizens of the Philippines have focused on catching fish as one of the ways to provide a more affordable source of protein. However, overfishing and inefficient resource allocation have compromised the steady and reliable supply of fish—and with it, protein—while also worsening the economic security of the people. 

Thus, this project strives to create a Mixed Integer Linear Program (MILP) to address this issue. Our MILP is designed to find an optimal strategy to catch and distribute fish among the people so as to maximize the overall protein distribution while minimizing all associated costs.

# Model Formulation
The Philippines is one of the world’s biggest archipelagos: it is made up of multiple islands interconnected by sea. As such, the Philippines is blessed with abundant natural resources from the sea, namely fish. However, a major challenge is posed in that this fish is not directly accessible to the people. For an ordinary person to consume fish, fish must be distributed through an intricate supply chain involving, from the very beginning, a fishing ground, and then a processing facility, and finally a city from where a person can directly buy fish. Consider the following diagram to illustrate this supply chain.

![](diagram.png)

A major challenge faced in the fisheries industry is thus deciding how to distribute fish in the most logistically efficient manner. Evidently, there are various geographical obstacles that separate the ordinary fish consumer from the fishing grounds—be it sea or land or even other obstacles—and hence the goal of this project would to be figure out an optimal strategy to distribute the most amount of fish while incurring the least amount of cost possible.

The problem thus centers around: (1) finding the optimal number of fish to be delivered from a fishing ground to a processing facility, (2) finding the optimal number of fish to be delivered from a processing facility to a city, (3) finding the optimal combination of facilities to be opened to ensure adequate fish processing capacity, and finally (4) finding the optimal amount of government subsidies required to provide access to fish consumption for the less fortunate—all while ensuring certain constraints are met. 

Indeed, this problem is a “Multi-Stage” Capacitated Facility Location Problem: each processing facility is a client to the fishing grounds, and each city is a client to the processing facilities.

# Code
The model was solved using Julia, particularly by using JuMP and GLPK as the solver.

# Authors
Nathan Ansel
Blauta Isaiah Rafael Tugano
Harrish Rahul Venkatraman
Lim Kyu Ha