# Task Scheduling using Ant Colony Optimization

## Overview

This project implements an Ant Colony Optimization (ACO) algorithm for task scheduling in a cloud computing environment. The goal is to assign tasks to virtual machines (VMs) in an efficient manner, minimizing the makespan (total execution time) while balancing the load among VMs.

## Features

- Implements Ant Colony Optimization (ACO) for task scheduling.

- Supports random instance generation for testing different task-VM configurations.

- Pheromone-based task assignment for optimized scheduling.

- Tracks convergence history and visualizes optimization progress.

- Supports benchmark file input and parsing.

- Plots convergence graphs to show algorithm performance.

## Dependencies

Make sure you have the following Python libraries installed:

pip install numpy matplotlib

## How It Works

1. Initialize tasks and VMs: Reads task and VM data from a file or generates random instances.

2. Construct Solutions: Each ant builds a solution by assigning tasks to VMs based on pheromone and heuristic values.

3. Evaluate Solutions: The makespan (completion time) is calculated for each solution.

4. Pheromone Update: Pheromone trails are updated to reinforce better solutions.

5. Iterate: Steps 2-4 repeat for a set number of iterations to improve scheduling.

6. Plot Convergence: A graph is generated to show the algorithm's performance over time.

## File Structure

- task_scheduler_aco.py - Main implementation of the ACO-based task scheduler.

- generate_input_file.py - Generates benchmark task-VM files for testing.

- parse_input_file.py - Parses input files to extract task, VM, and execution time data.

- plot_convergence.py - Generates and saves the convergence graph.

- run_experiments.py - Runs multiple experiments and prints performance results.

- README.md - Project documentation.

## Usage

### Running the Experiments

To run the full ACO optimization and analyze performance:

python task_scheduler_aco.py

Generating Random Input Files

To generate a random task-VM execution time file:

python generate_input_file.py

Example Output

Running experiments...
Results for n=10, m=5:
Optimal Assignment: [0, 3, 2, 1, 2, 3, 0, 1, 4, 4]
Makespan: 13.0
VM Times: [12.0, 12.0, 10.0, 12.0, 13.0]
Execution Time: 0.14s
Average VM Utilization: 90.77%
Load Balance (STD%): 7.54%

## Visualization

The script will generate a convergence graph to visualize the optimization process.

Example:

![image](https://github.com/user-attachments/assets/7d7f32df-7629-4086-a76e-677fd7de5f7f)
