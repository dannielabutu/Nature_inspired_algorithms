# Search and optimization using  Nature_inspired_algorithms

## INTRODUCTION
For several decades, vehicle routing optimization has been a significant challenge in most countries. This issue has become more pressing with the rise of just-in-time production and increasing population, leading to a significant gap in transportation efficiency. To address this, we aim to provide an efficient and reliable solution to the Vehicle Routing Problem (VRP) (Shitong, 2021). Numerous optimization problems exist across various industries such as engineering design, manufacturing operations, finance, and transportation. These problems share a common objective: to minimize or maximize a set of conflicting goals, a concept known as multi-objective optimization problems (MOPs). The primary goal in MOPs is to identify a comprehensive collection of optimized solutions that represent the best possible trade-offs in performance, known as the Pareto front (PF). These optimal solutions, referred to as nondominated or Pareto optimum solutions, map effectively to the PF (Wenjing et al., 2019).
Evolutionary Algorithms (EAs) have emerged as a preferred method due to their population-based search strategy, which inherently benefits from parallelism. EAs facilitate the discovery of solutions that are well-distributed across the PF. By maintaining population diversity, EAs enable decision-makers to evaluate performance more effectively and choose the best option or solutions (Haitao et al., 2023).

**Background concept**

In this problem, we are addressing a real-world problem of routing optimization for vehicle networks on the motorway.

Routing optimization plays a vital role in a well-performed network. Today’s world of interconnected system from enhancing efficient transportation, logistics to seamless data transmission. Almost all machine learning algorithms can be thought of as solutions to optimization problems. The fascinating thing is that one can still interpret all of these algorithms as solutions to optimization problems even in situations where the original machine learning technique had its roots in other disciplines, like biology (Wenjing et al, 2023).

## Constraints:
	Distance Constraint: If the distance between Car i and Car j is greater than 6000m, there is no connection, so Xij = 0 and rij = 0
	Connectivity Constraints: Ensure that each Car connects to exactly one Car or a BS, and each Car or BS is connected to exactly one Car.
Search and Optimization Requirements Specification
The object of this project is to
	Develop algorithm that identify the most efficient routing paths.
	Calculate the end-to-end transmission rate and latencies for each path.
	Comparison of the different routing paths to identify the optimal one.
    easier for a decision-maker to
    
 The optimization of vehicle network performance on highways is a significant problem in the era of complex connection. The real-world issue of route optimization in automotive networks is addressed. Vehicles need to be able to access the internet efficiently while they are travelling. This is accomplished by
**Problem Definition and Formulation**

The optimization of vehicle network performance on highways is a significant problem in the era of complex connection. The real-world issue of route optimization in automotive networks is addressed. Vehicles need to be able to access the internet efficiently while they are travelling. This is accomplished by enabling the vehicles to function as relay nodes, sending signals to other cars until they eventually connect to the base station (BS). Finding the best data packet routing path to a base station (BS) while taking important performance parameters (latency, end – to – end transmission) into account is the main goal. The primary focus of this assignment is to develop a solution for the multi-objective optimization problem in vehicle networks on motorways. The aim is to find the most optimal routing path given a network of base stations and cars, while optimizing for two key metrics: latency and end-to-end data transmission rate.

To formulate a mathematical function to solve this optimization problem, we use a mathematical modeling approach. We therefore break down the problem and formulate it mathematically:

## Decision Variables:

Let Xab be a binary variable

Where

Xab = 1 if there is a link from car i to car j, and Xab = 0 otherwise

Let rab represent the data transmission rate between Car a and Car b.

Parameters:

Dab represents the distance between car a and b.

Lab represents the latency imposed by the link between Car a and Car b.

Therefore, the objective function is:

Cost_Function = (weight_of_latency * (1 / latency(route))) + ((minimum_Transmission(route)) * weight_of_ete)

F = Fitness value of a route

Wl = Weight of latency

L(r) = Latency of the route

W ete= Weight of end-to-end (ETE) transmission rate

 mT(r) = Minimum transmission rate of the route

**Constraints:**

•	Distance Constraint: If the distance between Car a and Car b is greater than 6000m, there is no connection, so Xab = 0 and rab = 0

$d =\sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$


| distance (d)         | Transmission rate (Mbps) |
|----------------------|--------------------------|
| d>= 6000 m           | 0                        |
| 6000 m > d >= 4000 m | 1                        |
| 4000 m > d >= 3000 m | 2                        |
| 3000 m > d >= 2000 m | 4                        |
| 2000 m > d >= 1000 m | 6                        |
| 1000 m > d >= 500 m  | 8                        |
| 500 m  > d           | 10                       |

**Search and Optimization Requirements Specification**

1.   Develop algorithm that identify the most efficient routing paths using python.
2.   Evaluate the results using figures and graphs.
3.   Comparison of the implemented algorithm performance based on time complexity, convergence.
**Objective of the Assessment.**
1.	To find the optimal routing path using Dijkstra, Genetic Algorithm (GA) and Particle swamp optimization (PSO) algorithm
2.	To find the end – to – end transmission rate and latency using Genetic Algorithm (GA) and Particle swamp optimization (PSO) algorithm
3.	To evaluate the performance of various algorithm used and understand their strength and weakness.



**METHODOLOGY USED TO SOLVE THE PROBLEM**

This study employs a multi-faceted computational approach to address the problem of optimizing the routing of data packets across a network of vehicles, each represented by a node within a graph structure. The objective is to ascertain the most efficient path for data transmission, maximizing the rate of transmission while minimizing latency to either of two fixed base stations. The steps outlined below shows the procedures followed to achieve the objective of the problem.

Furthermore, three algorithms were used for this project. Dijkstra's algorithm is implemented to find the shortest distance while genetic algorithm (GA) and particle swam algorithm were used to find the multi-objective problem of minimum and maximum (end to end) transmission rate and latency.


Data Acquisition and Pre-processing:
The initial phase involves importing a dataset comprising the geographical coordinates (X, Y) of 100 vehicles using a python library called pandas. To this existing dataset, we append the coordinates of two predetermined base stations, BS_1 and BS_2 (101 and 102 respectively).
