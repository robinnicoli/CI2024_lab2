# Travelling Salesman Problem (TSP) - Multi-Approach Solution

This repository contains my solution for the Travelling Salesman Problem using three different algorithms: Greedy, Hill Climber Mutation, and Genetic Algorithm (GA). 

## Algorithms Overview

### Greedy Algorithm
The Greedy algorithm selects the nearest unvisited city at each step. This approach is fast but often not very optimal, especially for large datasets.

### Hill Climber with Mutation
The Hill Climber algorithm iteratively modifies an existing tour to minimize the total distance. It explores neighboring solutions through small changes:
- Swap Mutation: randomly exchanges two cities in the tour.
- Scramble Mutation: shuffles a subset of cities to explore alternate routes.
This method should  yield better solutions than the greedy algorithm but is likely to get trapped in a local optima.

### Genetic Algorithm
The GA uses a population of solutions that evolve over generations. Key components include:
- Selection: Chooses parent solutions based on fitness.
- Order Crossover: Combines parents to produce a child while maintaining city order.
- Inversion Mutation: Randomly reverses a section of the tour to introduce variation.
The GA should in theory produce better solutions than both previous algorithmes, especially with larger problem sizes.

