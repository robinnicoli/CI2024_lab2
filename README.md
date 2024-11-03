# Travelling Salesman Problem (TSP) - Multi-Approach Solution

This repository contains my solution for the Travelling Salesman Problem (TSP) using three different algorithms: Greedy, Hill Climber Mutation, and Genetic Algorithm (GA). The TSP is a classic optimization problem that seeks the shortest route to visit each city exactly once and return to the starting city.

## Algorithms Overview

### Greedy Algorithm
The Greedy algorithm selects the nearest unvisited city at each step. This approach is fast but often suboptimal, especially for large datasets.

### Hill Climber with Mutation
The Hill Climber algorithm iteratively modifies an existing tour to minimize the total distance. It explores neighboring solutions through small changes:
- **Swap Mutation** randomly exchanges two cities in the tour.
- **Scramble Mutation** shuffles a subset of cities to explore alternate routes.
This method can yield better solutions than Greedy but is prone to getting trapped in local optima.

### Genetic Algorithm (GA)
The GA uses a population of solutions that evolve over generations. Key components include:
- **Selection**: Chooses parent solutions based on fitness.
- **Order Crossover (OX)**: Combines parents to produce a child while maintaining city order.
- **Inversion Mutation**: Randomly reverses a section of the tour to introduce variation.
The GA tends to produce better solutions than Greedy and Hill Climber, especially with larger problem sizes.

## Conclusion:
Each method has its strengths and weaknesses:
- Greedy algorithms are fast but lack accuracy.
- Hill Climbing improves on Greedy results but are limited by local optima.
- Genetic Algorithms provide a balance between exploration and exploitation, often resulting in better overall optimization.

Based on the results, the Genetic Algorithm generally outperforms the other approaches in terms of achieving a shorter total distance, though it requires more computational effort.
