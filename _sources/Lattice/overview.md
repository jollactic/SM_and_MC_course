# Lattice models

## lattice

In three dimensions, a lattice can be defined as a regular arrangement of points in three-dimensional space, where each point has identical surroundings and the arrangement repeats itself periodically in all directions. More formally, a lattice in three dimensions can be defined as a set of points of the form $\vec{r} = n_1\vec{a}_1 + n_2\vec{a}_2 + n_3\vec{a}_3$, where $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are three linearly independent vectors called the lattice vectors, and $n_1$, $n_2$, and $n_3$ are integers.

The lattice vectors $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are chosen such that they form a parallelepiped that contains all the lattice points. This parallelepiped is called the unit cell of the lattice, and it represents the repeating pattern of the lattice.


![Lattice](lattice.png)

The figure illustrates a 2d lattice with the unit cell marker out.

There are many types of lattices in three dimensions, each with different symmetry properties. Some common examples include the simple cubic lattice, the face-centered cubic lattice, and the body-centered cubic lattice. The simple cubic lattice is the most basic type of lattice, where each lattice point is at the corner of a cube. The face-centered cubic lattice has additional lattice points at the center of each face of the cube, while the body-centered cubic lattice has an additional lattice point at the center of the cube.

## Ideal Lattice Gas

The ideal lattice gas model is a simplified representation of a gas system in statistical mechanics. It provides a theoretical framework for studying the behavior of non-interacting particles in a lattice structure. This model serves as a fundamental reference for understanding the properties of real gases under certain conditions.

### Introduction

In the ideal lattice gas model, the system is often conceptualized as a lattice, where each lattice site can be occupied by at most one particle. This model assumes non-interacting particles, neglecting any potential interactions between them. The simplicity of the ideal lattice gas makes it a useful starting point for studying the basic principles of statistical mechanics.

### Hamiltonian and Energy

The Hamiltonian for the ideal lattice gas model is straightforward, capturing the energy associated with placing particles on the lattice sites. It is expressed as:

$$
\\
 H = -\epsilon \sum_{i} n_i
\\
$$

Here:
- $$epsilon$) is the energy associated with placing a particle on a lattice site.
- $n_i$ is a binary variable equal to 1 if a particle occupies site $i$ and 0 otherwise.
- The sum is taken over all lattice sites.

### Partition Function

The partition function $Z$ for the ideal lattice gas is derived from the Hamiltonian and represents the sum of all possible configurations:

$$
\\
 Z = \sum_{\text{all configurations}} e^{-\beta H} 
\\
$$
Here:

- $\beta = \frac{1}{k_B T}$ is the inverse temperature, where $k_B$ is the Boltzmann constant and $T$ is the absolute temperature.

### Free Energy

The Helmholtz free energy ($F$) is obtained from the partition function:

$$ \\ F = -k_B T \ln Z \\ $$ 

### Internal Energy and Specific Heat

The internal energy ($U$) and specific heat ($C_V$) can be derived from the free energy:

$$ \\ U = -\frac{\partial \ln Z}{\partial \beta} \quad \text{and} \quad C_V = \frac{\partial U}{\partial T} \\ $$ 

### Entropy

The entropy ($S$) is given by:

$$ \\ S = \frac{\epsilon}{T} \frac{\partial \ln Z}{\partial \epsilon} + k_B \sum_{i} \left[ p_i \ln p_i + (1 - p_i) \ln (1 - p_i) \right] \\ $$ 

Here:
- $p_i$ is the probability of finding a particle at site $i$.

### Particle Density

The particle density ($n$) is given by the average number of particles per lattice site:

$$ \\ n = \frac{1}{\beta} \frac{\partial \ln Z}{\partial \epsilon} \\ $$ 

### Ideal Gas Law

In the limit of low particle density, the ideal lattice gas model converges to the ideal gas law:

$$ \\ PV = Nk_B T \\ $$ 

Here:
- $P$ is the pressure.
- $V$ is the volume.
- $N$ is the total number of particles.



## Interacting Lattice Gas with Nearest-Neighbor Interactions

In the context of statistical mechanics, an interacting lattice gas refers to a model where particles on a lattice experience interactions, specifically nearest-neighbor interactions. The energy associated with these interactions is denoted as $w$.

### Hamiltonian and Energy

The Hamiltonian for an interacting lattice gas is extended to include the interaction energy $w$ between nearest neighbors. It is expressed as:

$$ \\ H = -\epsilon \sum_{i} n_i - w \sum_{\langle i,j \rangle} n_i n_j \\ $$ 

Here:
- $\epsilon$ is the energy associated with placing a particle on a lattice site.
- $n_i$ is a binary variable equal to 1 if a particle occupies site $i$ and 0 otherwise.
- $w$ is the interaction energy between nearest neighbors.
- $\langle i, j \rangle$ denotes summation over nearest neighbors.

### Partition Function

The partition function ($Z$) for the interacting lattice gas is derived from the Hamiltonian:

$$ \\ Z = \sum_{\text{all configurations}} e^{-\beta H} \\ $$ 

Here:
- $\beta = \frac{1}{k_B T}$ is the inverse temperature, where $k_B$ is the Boltzmann constant and $T$ is the absolute temperature.

### Free Energy

The Helmholtz free energy ($F$) is obtained from the partition function:

$$ \\ F = -k_B T \ln Z \\ $$ 

### Internal Energy and Specific Heat

The internal energy ($U$) and specific heat ($C_V$) can be derived from the free energy:

$$ \\ U = -\frac{\partial \ln Z}{\partial \beta} \quad \text{and} \quad C_V = \frac{\partial U}{\partial T} \\ $$ 

### Entropy

The entropy ($S$) is given by:

$$ \\ S = \frac{\epsilon}{T} \frac{\partial \ln Z}{\partial \epsilon} + k_B \sum_{i} \left[ p_i \ln p_i + (1 - p_i) \ln (1 - p_i) \right] \\ $$ 

Here:
- $p_i$ is the probability of finding a particle at site $i$.

### Particle Density

The particle density ($n$) is given by the average number of particles per lattice site:

$$ \\ n = \frac{1}{\beta} \frac{\partial \ln Z}{\partial \epsilon} \\ $$ 







# Lattice Theory of Solutions

The lattice theory of solutions is a theoretical framework within statistical mechanics that provides a systematic approach to understanding the thermodynamic properties of solutions, particularly in the context of phase transitions and mixing behavior. This theory is particularly useful in describing idealized solutions and predicting their macroscopic properties.

## Introduction

In the lattice theory of solutions, the system is often represented as a lattice, where each lattice site can be occupied by a molecule or particle. This approach simplifies the complex interactions in a solution, making it a valuable tool for studying the thermodynamics of mixtures.

## Lattice Model Formulation

### Hamiltonian and Energy

The starting point is the formulation of a Hamiltonian that describes the energy of the system based on the interactions between neighboring lattice sites. For a binary solution, the energy of the system ($E$) can be expressed as:

$$ \\ E = -J \sum_{\langle i,j \rangle} \delta_{\sigma_i, \sigma_j} \\ $$ 

Here:
- $J$ is the interaction parameter.
- $\langle i,j \rangle$ denotes summation over nearest neighbors.
- $\delta_{\sigma_i, \sigma_j}$ is the Kronecker delta function, equal to 1 if $\sigma_i = \sigma_j$ and 0 otherwise.

### Entropy

The entropy ($S$) is introduced to account for the mixing of particles in the solution. Assuming ideal mixing, the entropy is given by the well-known expression:

$$ \\ S = -k_B \sum_{i} \left[p_i \ln p_i + (1 - p_i) \ln (1 - p_i)\right] \\ $$ 

Here:
- $k_B$ is the Boltzmann constant.
- $p_i$ is the probability of finding a particle of type $i$ at a lattice site.

## Thermodynamic Properties

### Free Energy

The Helmholtz free energy ($F$) is derived by combining the energy and entropy terms:

$$ \\ F = E - TS \\ $$ 

### Phase Transitions

By analyzing the free energy, the lattice theory of solutions predicts phase transitions in the system. For instance, in a binary solution, the model can describe demixing or phase separation as a function of temperature and composition.

## Limitations and Extensions

While the lattice theory of solutions provides valuable insights into the thermodynamics of idealized solutions, it has limitations in capturing real-world complexities, such as non-ideal mixing and interactions. Extensions, including mean-field theories and more sophisticated models, aim to address these limitations for a more accurate description of complex solutions.

## Applications

The lattice theory of solutions finds applications in various fields, including chemistry, physics, and materials science. It is particularly useful for predicting phase diagrams, studying phase transitions, and gaining a fundamental understanding of the thermodynamic behavior of solutions.

## Conclusion

The lattice theory of solutions offers a structured and mathematical approach to study the thermodynamics of solutions, providing a foundation for understanding phase transitions and mixing behavior. While it serves as a valuable theoretical tool for idealized scenarios, researchers often combine this approach with experimental data and more advanced theoretical models to capture the complexities of real-world solutions.




















## The Ising Model

The Ising model, named after physicist Ernst Ising, stands as a foundational concept in statistical mechanics, offering valuable insights into phase transitions and magnetic properties in materials. This mathematical model simplifies the intricate interactions within a system, making it particularly applicable in the exploration of ferromagnetism.

### Overview
The two-dimensional Ising model is a simplified representation of a magnetic material where each magnetic moment (spin) interacts only with its nearest neighbors. The system's elements, often representing magnetic moments, are assigned binary spins – typically up or down. These spins interact primarily with their nearest neighbors, influencing each other's orientation. The model's behavior is described by the following simple Hamiltonian:

$$ \\ H = -J \sum_{\langle i,j \rangle} s_i s_j - h \sum_{i} s_i \\ $$ 

Here:
- $J$ represents the strength of interactions between spins.
- $s_i$ is the spin at site $i$.
- $\langle i,j \rangle$ denotes summation over nearest neighbors.
- $h$ is an external magnetic field.


A defining feature of the Ising model is its ability to exhibit phase transitions. In particular, it undergoes a ferromagnetic transition where spins align, leading to the material becoming magnetized. This critical behavior is pivotal for understanding the emergence of macroscopic properties in various physical systems. The Ising model finds widespread applications in physics and material science. It serves as a crucial tool for studying critical phenomena and phase transitions. In material science, the model aids in comprehending magnetic properties in diverse materials, providing a bridge between microscopic interactions and macroscopic behaviors.


## Onsager's Connection to the Ising Model

Lars Onsager, a distinguished theoretical physicist, made a groundbreaking contribution to statistical mechanics by providing an exact solution for the two-dimensional Ising model in 1944. Onsager's solution was a significant breakthrough, as solving the Ising model exactly had proven to be a formidable mathematical challenge.

### Key Contributions

1. **Partition Function:**
   - Onsager derived a closed-form expression for the partition function of the two-dimensional Ising model, encapsulating the statistical properties of the system.

2. **Critical Temperature:**
   - Determined the critical temperature for the phase transition in the two-dimensional Ising model, where the material undergoes a transition from a disordered to an ordered state, exhibiting spontaneous magnetization.

3. **Magnetization Profile:**
   - Provided insights into the behavior of magnetization as a function of temperature, shedding light on the nature of the phase transition.




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