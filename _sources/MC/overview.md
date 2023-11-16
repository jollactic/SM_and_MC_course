# Monte-Carlo

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

<a target="_blank" href="https://colab.research.google.com/github/jollactic/Modelling_course/blob/main/CE_MC/Tutorial_LMO.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>


<div class="warning" style='padding:0.1em; background-color:#E9D8FD; color:#69337A'>
<span>
<p style='margin-top:1em; text-align:center'>
<b>Assignment:</b></p>
<p style='margin-left:1em;'>

Use the tutorial to predict the voltage profile (at various levels of approximation) for a cathode material where a spinel structured $LiMn_2O_4$ consists the intercalation material.

<p style='margin-top:1em; text-align:center'>
<b>Submission instructions:</b></p>
<p style='margin-left:1em;'>

<p style='margin-left:1em;'>
Upload your commented version of the note-book to the studium page. 

</p></span>
</div>

### Further reading:

1. [A pedagocially written article on the subject](https://iopscience.iop.org/article/10.1088/1361-648X/ab1bbc)

2. [An extensive DFT based study of the Ag-Pt system](http://manuscript.elsevier.com/S1359645416308205/pdf/S1359645416308205.pdf)

3. [Chapter 3 in *Understanding Molecular Simulation : From Algorithms to Applications* by Daan Frenkel & Berend Smit](https://ebookcentral.proquest.com/lib/uu/reader.action?docID=307221)

4. [Chapter 6 in *Atomistic Computer Simulations : A Practical Guide* by Veronika Brázdová and David R. Bowler](https://ebookcentral.proquest.com/lib/uu/reader.action?docID=1161544)