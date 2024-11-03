# Travelling Salesman Problem (TSP) - Multi-Approach Solution

This repository contains my solution for the Travelling Salesman Problem (TSP) using three different algorithms: Greedy, Hill Climber Mutation, and Genetic Algorithm (GA). The TSP is a classic optimization problem that seeks the shortest route to visit each city exactly once and return to the starting city.

## Project Structure

The project includes:
- **Greedy Algorithm**: A simple heuristic that selects the nearest unvisited city at each step.
- **Hill Climber with Mutation**: An iterative optimization approach that improves a solution through small mutations.
- **Genetic Algorithm (GA)**: A population-based evolutionary algorithm with crossover and mutation.

### Code Structure

The main code is organized into sections for readability and modularity. Key sections include:

1. **Libraries and Data Loading**: 
   - Required libraries are imported, and data loading functions are defined to read city coordinates and compute distances between them.

2. **Distance Calculation and Tour Validation**:
   - A function to compute the total distance of a TSP tour and another function to check if a tour is valid (each city is visited exactly once, and it forms a cycle).

3. **Greedy Algorithm**:
   - A simple greedy solution for TSP that always moves to the nearest unvisited city. This algorithm serves as a baseline solution and provides a quick, though suboptimal, solution for small datasets.

4. **Hill Climber with Mutation**:
   - The Hill Climber algorithm iteratively improves an initial solution by performing mutations, specifically **swap mutation** or **scramble mutation**:
     - **Swap Mutation**: Randomly swaps two cities in the tour to create a new neighboring solution.
     - **Scramble Mutation**: Shuffles a subset of cities within the tour to explore alternate paths.
   - This algorithm may find better solutions than Greedy by exploring neighboring solutions, but it can get stuck in local minima.

5. **Genetic Algorithm (GA)**:
   - The Genetic Algorithm section includes:
     - **Selection**: Randomly selects two parents from the population.
     - **Order Crossover (OX)**: Combines genes from two parents while preserving the relative order of cities.
     - **Inversion Mutation**: Reverses a segment of the genome (tour) to introduce diversity.
   - GA parameters, such as population size, mutation rate, and number of generations, are configurable for experimentation.

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
