# Taking inspiration from Bisin 2021 Spatial SIR Model

Used appendix as reference as well as GitHub see here: <https://github.com/andreamoro-git/BM-Spatial-SIR> (in python but whatever)

## Model Components (SARS-CoV-2)

### SIR 

Note: Fancy S represents the state space in paper but replacing with $\chi$ because I can...

$ \chi = \{S, A, Y, R, D\} $ - state space of suspectibles, asymptomatic, sYmptomatics, recovered, and dead.

$ h_{t}^{i} \in \chi$ agent $i$ at time $t$ and $ h_{t} = \frac{1}{N} \[S_t , A_t , Y_t , R_t , D_t \] \in \Delta^{\chi} $ - distribution of (N) agents in the population of state space

Why include exposed group - point of intervention!

decay function rather than strict radius of infection (continuous thing to play with) never have force of infection exactly zero

uniformally randomly move update discrete or continuous rate or brownian motion (2d gaussian)


### Spatial

Agent contacts are a result of geographically local matching rather than random through a stochastic process interaction model.

travel a distance $\mu$ every day ($t = \[0,T\]$) and come in contact for $d(h^m , h^n) < p$ with probability of infection $\pi$ and recovery rate $\rho$.


## Approach

Remove susceptible population as that will just be the space to start (see Fig 1) which yields ODE system:


$\frac{dI}{dt} = \beta S \frac{I}{N} - \rho I$

$\frac{dR}{dt} = \rho I$

$ N = S + I + R $

Translated to be continuous on bounded domain via reaction-diffusion equation set up...

$\frac{dI}{dt} - \alpha \Delta I = \beta S \frac{I}{N} - \rho I$

$\frac{dR}{dt} \alpha \Delta I = \rho I$

$ N = \int_{D} (S + I + R) ds \forall t $

$\partial_{\nu} S = \partial_{\nu} I = \partial_{\nu} R = 0$ (Boundary Conditions! - no one leaves)


### Pseudo Code

0. Start first without diffusion and use basic SIR in space (no multi city yet)

1. Initialize domain with agents in it based on initial conditions

    a. How do we get agents to "move"?

    b. Start with stationary but all agents are within infection distance of each other aka lattice of points in p intervals

2. Plotting movies in R - or plotting at $ t = 0, 1, 5, 10...$

WIP


## Dynamical System

$ H_{t+1} = T(H_t)H_t$ where $T(H_t)$ - transition matrix defined by local interaction model. What does this actually look like? Defined using Markov transition processes which I need to read up on...