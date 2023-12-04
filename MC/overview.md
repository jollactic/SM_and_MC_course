# Monte-Carlo

# Monte Carlo Integration

Monte Carlo integration is a numerical technique for estimating definite integrals using random sampling. It is particularly useful when dealing with complex or high-dimensional integrals that are challenging to solve analytically. The basic idea is to use random sampling to obtain a statistical approximation of the integral.

## Area of a Single Circle

Consider the task of computing the area of a circle using Monte Carlo integration. The formula for the area of a circle is \(A = \pi r^2\), where \(r\) is the radius. Instead of relying on this formula, we can use random sampling to estimate the area.

1. **Generate Random Points**: Randomly scatter points within a bounding square that encloses the circle.

2. **Count Points Inside the Circle**: Determine how many points fall inside the circle by checking if the distance from the origin to each point is less than the radius of the circle.

3. **Estimate Area**: The ratio of points inside the circle to the total points generated provides an estimate of the fraction of the area covered by the circle. Multiply this ratio by the area of the bounding square to obtain the estimated area of the circle.

## Multiple Overlapping Circles

Extending the concept to multiple overlapping circles involves a similar process:

1. **Generate Random Points**: Scatter points within a bounding square that encompasses all the circles.

2. **Count Points Inside Any Circle**: For each point, check if it falls inside any of the circles.

3. **Estimate Total Area**: The ratio of points inside any circle to the total points generated gives an estimate of the fraction of the total area covered by the circles. Multiply this ratio by the area of the bounding square to obtain the estimated total area.


![Lattice](circles.gif)


## Detailed Balance

Detailed balance is a fundamental concept in Monte Carlo simulations, ensuring that the simulated system reaches a proper equilibrium state. It is a condition that the transition rates between different states in a Markov Chain Monte Carlo (MCMC) simulation are such that, when reached, the system maintains a balance between forward and reverse transitions. In other words, the probability of transitioning from one state to another is the same as the probability of transitioning back.

### Detailed Balance Condition

Mathematically, the detailed balance condition is expressed as follows:

$$
P_i \cdot T_{ij} = P_j \cdot T_{ji}
$$

Here:
- $P_i$ is the probability of being in state $i$,
- $P_j$ is the probability of being in state $j$,
- $T_{ij}$ is the transition probability from state $i$ to state $j$,
- $T_{ji}$ is the transition probability from state $j$ to state $i$.

This condition ensures that the system, when in equilibrium, does not favor transitions in one direction over the reverse.

### Detailed Balance in Monte Carlo Simulations

In Monte Carlo simulations, detailed balance is crucial for the proper sampling of the configuration space. The simulation generates a sequence of states by proposing moves, and detailed balance ensures that these moves are accepted or rejected in a way that preserves the equilibrium distribution.

In the context of a Metropolis-Hastings Monte Carlo algorithm, which is widely used, detailed balance is implemented through an acceptance probability. The probability of accepting a move from state $i$ to state $j$ ($A_{ij}$) is given by:

$$
A_{ij} = \min\left(1, \frac{P_j}{P_i} \cdot \frac{T_{ji}}{T_{ij}}\right)
$$

This formula ensures that, on average, transitions from $i$ to $j$ are as likely as transitions from $j$ to $i$, satisfying the detailed balance condition.

### Ensuring Convergence

Ensuring detailed balance is crucial for the convergence of the Monte Carlo simulation to the correct equilibrium distribution. Without detailed balance, the simulation might not reach a steady-state, leading to biased results.



## Metropolis Monte-Carlo (MC)

The Metropolis Monte Carlo simulation technique is a powerful computational method used to simulate the thermodynamcs of dissordered systems in condensed matter physics, chemistry, and materials science.

The Metropolis Monte Carlo simulation technique works by randomly proposing new configurations of the system, and accepting or rejecting them based on their energy difference relative to the current configuration. The probability of accepting a new configuration is determined by the Metropolis criterion, which ensures that the simulation samples the correct thermodynamic ensemble (it complies with the Boltzmann distribution).

The Metropolis criterion states that the probability of accepting a new configuration with energy difference $\Delta E$ is given by:

$$
\\
P(\Delta E) = min  \{ e^{-\Delta E/k_BT}, 1  \}
\\
$$

where $k_B$ is the Boltzmann constant, $T$ is the temperature, and $\Delta E$ is the energy difference between the proposed  configuration and the current configuration. This means that, if the propsoed configuration has a lower energy it is always accepted. 


In practice, the Metropolis Monte Carlo simulation technique involves the following steps:

1. Choose a starting configuration for the system.

2. Randomly propose a new configuration by moving one or more atoms or molecules in the system.

3. Calculate the energy difference between the proposed configuration and the current configuration.

4. Determine whether to accept or reject the proposed configuration based on the Metropolis criterion.

5. Record/save the current configuration into a data-base. *Note that the same configurations can be added twice or more when we reject proposed configurations. This is a key-point of the approach, low energy configuration shall be mre predominant in our data-base.* 

6. Repeat steps 2-4 for a large number $N$ of iterations , allowing the simulation to explore the configuration space of the system.

From the data-base generated in this procedure, we can calculate thermodynamic properties of the system, such as the heat capacity and free energy. In order to do so we simply take the average of the property calculated using all configurations in our data-base. For example the internal energy, $<U>$, can be calculated as follows:


$$
\\
<U> = \frac{1}{N} \sum_{n}^{N} E_i
\\
$$

where $N$ is the number of configurations in our data-base, and $E_n$ is the energy of configuration $n$. The concept can be generalized to any property that can be computed for the single configurations (so-called mechanical properties). 

$$
\\
<A> = \frac{1}{N} \sum_{n}^{N} A_n
\\
$$

[The concept os this type of sampling is neatly illustrated in this interactive example](https://chi-feng.github.io/mcmc-demo/app.html?algorithm=RandomWalkMH&target=banana).


### Tutorial

<a target="_blank" href="https://colab.research.google.com/github/jollactic/SM_and_MC_course/blob/main/MC/MC_lattic.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


<div class="warning" style='padding:0.1em; background-color:#E9D8FD; color:#69337A'>
<span>
<p style='margin-top:1em; text-align:center'>
<b>Assignment:</b></p>
<p style='margin-left:1em;'>


<p style='margin-top:1em; text-align:center'>
<b>Have fun</b></p>
<p style='margin-left:1em;'>

<p style='margin-left:1em;'>

</p></span>
</div>

### Random numbers

<a target="_blank" href="https://colab.research.google.com/github/jollactic/SM_and_MC_course/blob/main/MC/Random_numbers.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


### Further reading:

1. [A pedagocially written article on the subject](https://iopscience.iop.org/article/10.1088/1361-648X/ab1bbc)

2. [An extensive DFT based study of the Ag-Pt system](http://manuscript.elsevier.com/S1359645416308205/pdf/S1359645416308205.pdf)

3. [Chapter 3 in *Understanding Molecular Simulation : From Algorithms to Applications* by Daan Frenkel & Berend Smit](https://ebookcentral.proquest.com/lib/uu/reader.action?docID=307221)

4. [Chapter 6 in *Atomistic Computer Simulations : A Practical Guide* by Veronika Brázdová and David R. Bowler](https://ebookcentral.proquest.com/lib/uu/reader.action?docID=1161544)
