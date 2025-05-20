# Mean Field Game Model of Systemic Risk

This Porject was done for the Course Financial Engineering(IE612).This project is an implementation of Mean Field Game to study Systemic Risk for an interconnected network of banks. Here you can find a simulation of a Mean Field Game (MFG) model of systemic risk based on the Linear-Quadratic framework as described by Carmona, Fouque, and Sun (2013). The model explores the dynamics of banks (agents) controlling their borrowing and lending through a state variable that evolves according to a stochastic differential equation (SDE). In addition, the project investigates default probabilities through simulation of coupled (interacting) and independent bank dynamics.

## Project Structure

- **notebooks/**: Contains Jupyter notebooks for simulating different aspects of the MFG model and default behavior.
  - **trials.ipynb**: Simulates bank asset dynamics using SDEs under various control strategies (both open-loop and closed-loop formulations), including the computation of theoretical solutions.
  - **default_probability.ipynb**: Estimates the probability of bank defaults under two models—coupled and independent—by tracking the running minimum of bank assets.
- **README.md**: Overview of the project, model description, setup instructions, and usage guidelines.
- **Report.pdf**: Detailed report of the Course project.

## Model Description

The MFG model focuses on the interactions between multiple agents (banks) in a financial system. Each bank’s decision-making is influenced by the collective behavior of all participants, leading to emergent phenomena such as synchronization and systemic risk. The project implements both open-loop and closed-loop Nash equilibria using techniques from stochastic control theory, dynamic programming, and the Pontryagin stochastic maximum principle.

Additional simulations in this repository include a detailed analysis of default probabilities. By modeling the asset dynamics of banks and tracking the running minimum of each bank's asset value, the model quantifies the likelihood of bank defaults under two cases:

1. **Coupled System**: Banks interact via an interbank lending/borrowing term (`a * (mean_X - X)`), capturing systemic risk due to interdependencies.
2. **Independent System**: Banks evolve solely based on individual random shocks, serving as a baseline scenario.


## Dependencies

Ensure that the following Python packages (and their dependencies) are installed:
- numpy
- scipy
- matplotlib
