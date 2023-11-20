# Lattice models

## lattice

In three dimensions, a lattice can be defined as a regular arrangement of points in three-dimensional space, where each point has identical surroundings and the arrangement repeats itself periodically in all directions. More formally, a lattice in three dimensions can be defined as a set of points of the form $\vec{r} = n_1\vec{a}_1 + n_2\vec{a}_2 + n_3\vec{a}_3$, where $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are three linearly independent vectors called the lattice vectors, and $n_1$, $n_2$, and $n_3$ are integers.

The lattice vectors $\vec{a}_1$, $\vec{a}_2$, and $\vec{a}_3$ are chosen such that they form a parallelepiped that contains all the lattice points. This parallelepiped is called the unit cell of the lattice, and it represents the repeating pattern of the lattice.


![Lattice](lattice.png)

The figure illustrates a 2d lattice with the unit cell marked out.

There are many types of lattices in three dimensions, each with different symmetry properties. Some common examples include the simple cubic lattice, the face-centered cubic lattice, and the body-centered cubic lattice. The simple cubic lattice is the most basic type of lattice, where each lattice point is at the corner of a cube. The face-centered cubic lattice has additional lattice points at the center of each face of the cube, while the body-centered cubic lattice has an additional lattice point at the center of the cube.


IMPORTANT #1: For systems with disorder (e.g gas and liquids) we make use of a "super lattice" contaning a large number of sites. The repeating unit can be threrfore be very large!

IMPORTANT #2: Neighbors (especially nearest neieghbors = NN ) are important in lattice models. We should explain the concept of periodic boundary conditions here and illustrate this concept in terms of which lattice site are connected (NN).



## Ideal Lattice Gas

The ideal lattice gas model is a simplified representation of a gas system in statistical mechanics. It provides a theoretical framework for studying the behavior of non-interacting particles in a lattice structure. This model serves as a fundamental reference for understanding the properties of real gases under certain conditions.

### Configurational entropy of an ideal lattice gas

Can we find an expression in terms of the fraction of occupied sites? 

### Chemical potential


## Interacting Lattice Gas with Nearest-Neighbor Interactions

In the context of statistical mechanics, an interacting lattice gas refers to a model where particles on a lattice experience interactions, specifically nearest-neighbor interactions. The energy associated with these interactions is denoted as $w$.

### Mixture

A lattice fully populated with two types os species A and B. 

### Bragg-Williams approximation (Mean-field approximation)

Can we derive the partion function using Christer Elvingssons notes and compute some thermodynamical quantity that we can later compare to an explicit Monte-Carlo simulation?

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