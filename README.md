 # Discrete Optimization Problem Using Genetic Algorithm

## Introduction

This project aims to implement a genetic algorithm to find the global maximum value of the function 𝑓(𝑥) = −𝑥\^2 + 6𝑥 over the integer interval [0, 30]. The implementation involves creating various components of the genetic algorithm, such as generating a random initial population, parent selection, survivor selection based on fitness, mutation, and recombination using single-point and uniform methods.

## Genetic Algorithm

A genetic algorithm (GA) is a heuristic optimization technique inspired by the process of natural selection and genetics. It is used to find approximate solutions to optimization and search problems. Here's how a genetic algorithm typically works:

1. <b> Initialization </b>: An initial population of candidate solutions is generated randomly.
2. <b> Fitness Evaluation</b>: The fitness of each candidate solution is evaluated using a fitness function that quantifies how well it solves the problem.
3.  <b> Selection</b>: Individuals from the population are selected to become parents for the next generation based on their fitness. This is typically done using methods like roulette wheel selection, tournament selection, or rank-based selection.
4. <b> Crossover</b>: Pairs of parents are selected and recombined to create offspring. Crossover points are chosen, and genetic material is exchanged between parents to create new solutions.
5.  <b> Mutation</b>: Random changes are introduced into some individuals of the population to maintain genetic diversity and prevent premature convergence.
6. <b> Survivor Selection</b>: The new population is formed by selecting individuals from the current population and the offspring population, typically based on their fitness.
7. <b> Termination</b>: The algorithm terminates when a stopping criterion is met, such as reaching a maximum number of generations or finding a satisfactory solution.

## Implementation Details

### Components of Genetic Algorithm 

1.  **Initial Population Generation**: Randomly generates an initial population within the specified interval.
2.  **Fitness Calculation**: Calculates the fitness of individuals in the population using the given function.
3.  **Parent Selection**: Implements a selection mechanism to choose parents based on their fitness.
4.  **Mutation**: Performs mutation on selected individuals to introduce diversity in the population.
5.  **Crossover**: Implements crossover using both single-point and uniform methods to produce offspring.

### Program Execution

The program allows receiving necessary inputs either from a file or from the console. The inputs required are:

-   Population size
-   Mutation probability
-   Recombination probability
-   Recombination type (1 for single-point, 2 for uniform)
-   Maximum number of iterations as the termination condition

There's no need to manually change parameters within the code. The program iterates until the termination condition is met.

## Usage

1.  Run the program.
2.  Input the required parameters when prompted.
3.  The program will execute the genetic algorithm and print the final population.

## Example Usage

<b> The input: </b>

Enter size of population: 10

Enter possibility of mutate: 0.1

Enter type of crossover (1 for single-point, 2 for uniform): 1

Enter possibility of crossover: 0.8 Enter maximum number of iterations: 100

<b> The out put: </b>

**[9, 20, 10, 30, 2, 11, 20, 11, 1, 20]**


### From the provided input and output, we can draw several conclusions about the behavior of the genetic algorithm:

1.  **Diverse Population**: The final population includes a variety of values ranging from 1 to 30, indicating that the initial random population generation effectively sampled across the entire search space.
2.  **Genetic Diversity**: The presence of different values in the final population suggests that both mutation and crossover operations contributed to maintaining genetic diversity throughout the optimization process.
3.  **Effectiveness of Crossover**: The presence of values like 20 in multiple individuals suggests that crossover operations might have propagated certain genetic material across the population. However, since the crossover probability was set to 0.8, not all pairs of parents underwent crossover, preserving some diversity.
4.  **Mutation Impact**: With a mutation probability of 0.1, we see some individuals with values such as 1 and 2, indicating that they might have undergone mutation. Mutation allows the algorithm to explore new regions of the search space by introducing small changes to individuals.
5.  **Convergence**: The algorithm terminated after 100 iterations. The final population might not represent the global maximum of the function, indicating that further iterations or adjustments to parameters might be necessary for better convergence.
6.  **Algorithm Performance**: The genetic algorithm successfully executed within the specified constraints and provided a population of potential solutions. However, further analysis, such as evaluating the fitness of individuals and tracking convergence over multiple runs, would be necessary to assess its overall performance and effectiveness in finding the global maximum.

Based on these observations, we can infer that the genetic algorithm effectively explored the search space, maintained genetic diversity, and generated potential solutions for the given optimization problem. Further experimentation and analysis could help fine-tune parameters and improve the algorithm's performance.

## Conclusion

This implementation demonstrates the use of genetic algorithms to solve discrete optimization problems. By following the README instructions, users can easily run the program and apply it to different optimization tasks.
