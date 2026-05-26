# The pn Junction

p to this point in the text, we have been considering the properties of the semiconductor material. We calculated electron and hole concentrations in thermal equilibrium and determined the position of the Fermi level. We then considered the nonequilibrium condition in which excess electrons and holes are present in the semiconductor. We now wish to consider the situation in which a p-type and an n-type semiconductor are brought into contact with one another to form a pn junction. 

Most semiconductor devices contain at least one junction between p-type and n-type semiconductor regions. Semiconductor device characteristics and operation are intimately connected to these pn junctions, so considerable attention is devoted initially to this basic device. 

The electrostatics of the zero-biased and reverse-biased pn junction is considered in this chapter. The current–voltage characteristics of the pn junction diode are developed in the next chapter. ■ 

# 7.0 | PREVIEW

In this chapter, we will: 

■ Consider a uniformly doped pn junction, in which one region of the semiconductor is uniformly doped with acceptor atoms and the adjacent region is uniformly doped with donor atoms. 

Determine the energy-band diagram of a pn junction in thermal equilibrium. 

■ Discuss the creation of a space charge region between the p and n regions. 

Apply Poisson’s equation to determine the electric fi eld in the space charge region and calculate the built-in potential barrier. 

■ Analyze the changes that occur in the pn junction when a reverse-biased voltage is applied. Derive expressions for space charge width and depletion capacitance. 

■ Analyze the voltage breakdown characteristics of a pn junction. 

■ Consider the properties of a nonuniformly doped pn junction. Specifi c doping profi les can lead to desirable properties of the pn junction. 

# 7.1 | BASIC STRUCTURE OF THE pn JUNCTION

Figure 7.1a schematically shows the pn junction. It is important to realize that the entire semiconductor is a single-crystal material in which one region is doped with acceptor impurity atoms to form the p region and the adjacent region is doped with donor atoms to form the n region. The interface separating the n and p regions is referred to as the metallurgical junction. 

The impurity doping concentrations in the p and n regions are shown in Figure 7.1b. For simplicity, we will consider a step junction in which the doping concentration is uniform in each region and there is an abrupt change in doping at the junction. Initially, at the metallurgical junction, there is a very large density gradient in both electron and hole concentrations. Majority carrier electrons in the n region will begin diffusing into the p region, and majority carrier holes in the p region will begin diffusing into the n region. If we assume there are no external connections to the semiconductor, then this diffusion process cannot continue indefi nitely. As electrons diffuse from the n region, positively charged donor atoms are left behind. Similarly, as holes diffuse from the p region, they uncover negatively charged acceptor atoms. The net positive and negative charges in the n and p regions induce an electric fi eld in the region near the metallurgical junction, in the direction from the positive to the negative charge, or from the n to the p region. 

The net positively and negatively charged regions are shown in Figure 7.2. These two regions are referred to as the space charge region. Essentially all electrons and holes are swept out of the space charge region by the electric fi eld. Since the space charge region is depleted of any mobile charge, this region is also referred to as the depletion region; these two terms will be used interchangeably. Density gradients still exist in the majority carrier concentrations at each edge of the space charge region. We can think of a density gradient as producing a “diffusion force” that acts on the majority carriers. These diffusion forces, acting on the electrons and holes at the edges of the space charge region, are shown in the fi gure. The electric fi eld in the space charge region produces another force on the electrons and holes, which is in the opposite direction to the diffusion force for each type of particle. In thermal equilibrium, the diffusion force and the E-fi eld force exactly balance each other. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/47b9e5246356dcf9e1a1ccebf6ef08c819422aced115bce1a09a0869344c799d.jpg)



Figure 7.1 | (a) Simplifi ed geometry of a pn junction; (b) doping profi le of an ideal uniformly doped pn junction.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/cb99f4b8d8d93dfa1f2c0e437c086f67b77a1bca756371adda225c84b722481b.jpg)



Figure 7.2 | The space charge region, the electric fi eld, and the forces acting on the charged carriers.


# 7.2 | ZERO APPLIED BIAS

We have considered the basic pn junction structure and discussed briefl y how the space charge region is formed. In this section we will examine the properties of the step junction in thermal equilibrium, where no currents exist and no external excitation is applied. We will determine the space charge region width, electric fi eld, and potential through the depletion region. 

The analysis in this chapter is based on two assumptions that we have considered in previous chapters. The fi rst assumption is that the Boltzmann approximation is valid, which means that each semiconductor region is nondegenerately doped. The second assumption is that complete ionization exists, which means that the temperature of the pn junction is not “too low.” 

# 7.2.1 Built-in Potential Barrier

If we assume that no voltage is applied across the pn junction, then the junction is in thermal equilibrium—the Fermi energy level is constant throughout the entire system. Figure 7.3 shows the energy-band diagram for the pn junction in thermal equilibrium. The conduction and valance band energies must bend as we go through the space charge region, since the relative position of the conduction and valence bands with respect to the Fermi energy changes between p and n regions. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/f86587314c0a4ba1c3dc341fac5243ea1cf74f03c768a47b11a85b612179ae5f.jpg)



Figure 7.3 | Energy-band diagram of a pn junction in thermal equilibrium.


Electrons in the conduction band of the n region see a potential barrier in trying to move into the conduction band of the p region. This potential barrier is referred to as the built-in potential barrier and is denoted by $V _ { b i \bullet }$ . The built-in potential barrier maintains equilibrium between majority carrier electrons in the n region and minority carrier electrons in the p region, and also between majority carrier holes in the p region and minority carrier holes in the n region. This potential difference across the junction cannot be measured with a voltmeter because new potential barriers will be formed between the probes and the semiconductor that will cancel $V _ { b i }$ . The potential $V _ { b i }$ maintains equilibrium, so no current is produced by this voltage. 

The intrinsic Fermi level is equidistant from the conduction band edge through the junction; thus, the built-in potential barrier can be determined as the difference between the intrinsic Fermi levels in the p and n regions. We can defi ne the potentials $\phi _ { F n }$ and $\phi _ { F p }$ as shown in Figure 7.3, so we have 

$$
V _ {b i} = \left| \phi_ {F n} \right| + \left| \phi_ {F p} \right| \tag {7.1}
$$

In the n region, the electron concentration in the conduction band is given by 

$$
n _ {0} = N _ {c} \exp \left[ \frac {- (E _ {c} - E _ {F})}{k T} \right] \tag {7.2}
$$

which can also be written in the form 

$$
n _ {0} = n _ {i} \exp \left[ \frac {E _ {F} - E _ {F i}}{k T} \right] \tag {7.3}
$$

where $n _ { i }$ and $E _ { F i }$ are the intrinsic carrier concentration and the intrinsic Fermi energy, respectively. We may defi ne the potential $\phi _ { F n }$ in the n region as 

$$
e \phi_ {F n} = E _ {F i} - E _ {F} \tag {7.4}
$$

Equation (7.3) may then be written as 

$$
n _ {0} = n _ {i} \exp \left[ \frac {- (e \phi_ {F n})}{k T} \right] \tag {7.5}
$$

Taking the natural log of both sides of Equation (7.5), setting $n _ { 0 } = N _ { d } ,$ and solving for the potential, we obtain 

$$
\phi_ {F n} = \frac {- k T}{e} \ln \left(\frac {N _ {d}}{n _ {i}}\right) \tag {7.6}
$$

Similarly, in the p region, the hole concentration is given by 

$$
p _ {0} = N _ {a} = n _ {i} \exp \left[ \frac {E _ {F i} - E _ {F}}{k T} \right] \tag {7.7}
$$

where $N _ { a }$ is the acceptor concentration. We can defi ne the potential $\phi _ { F p }$ in the p region as 

$$
e \phi_ {F p} = E _ {F i} - E _ {F} \tag {7.8}
$$

Combining Equations (7.7) and (7.8), we fi nd that 

$$
\phi_ {F p} = + \frac {k T}{e} \ln \left(\frac {N _ {a}}{n _ {i}}\right) \tag {7.9}
$$

Finally, the built-in potential barrier for the step junction is found by substituting Equations (7.6) and (7.9) into Equation (7.1), which yields 

$$
V _ {b i} = \frac {k T}{e} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right) = V _ {t} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right) \tag {7.10}
$$

where $V _ { t } = k T / e$ and is defi ned as the thermal voltage. 

At this time, we should note a subtle but important point concerning notation. Previously in the discussion of a semiconductor material, $N _ { d }$ and $N _ { a }$ denoted donor and acceptor impurity concentrations in the same region, thereby forming a compensated semiconductor. From this point on in the text, $N _ { d }$ and $N _ { a }$ will denote the net donor and acceptor concentrations in the individual n and p regions, respectively. If the p region, for example, is a compensated material, then $N _ { a }$ will represent the difference between the actual acceptor and donor impurity concentrations. The parameter $N _ { d }$ is defi ned in a similar manner for the n region. 

Objective: Calculate the built-in potential barrier in a pn junction. 

Consider a silicon pn junction at T - 300 K with doping concentrations of $N _ { a } =$ $2 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

EXAMPLE 7.1 

# Solution

The built-in potential barrier is determined from Equation (7.10) as 

$$
V _ {b i} = V _ {t} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right) = (0. 0 2 5 9) \ln \left[ \frac {(2 \times 1 0 ^ {1 7}) (1 0 ^ {1 5})}{(1 . 5 \times 1 0 ^ {1 0}) ^ {2}} \right] = 0. 7 1 3 \mathrm{V}
$$

If we change the doping concentration in the p region of the pn junction such that the doping concentrations become $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , then the built-in potential barrier becomes $V _ { b i } = 0 . 6 3 5 \mathrm { ~ V ~ }$ . 

# ■ Comment

The built-in potential barrier changes only slightly as the doping concentrations change by orders of magnitude because of the logarithmic dependence. 

# ■ EXERCISE PROBLEM

Ex 7.1 (a) Calculate the built-in potential barrier in a silicon pn junction at $T = 3 0 0 ~ \mathrm { K }$ for (i) $\begin{array} { r } { \phantom { } _ { N _ { a } } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } , N _ { d } = 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } \mathrm { a n d } ( i i ) N _ { a } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } , N _ { d } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } . } \end{array}$ (b) Repeat part (a) for a GaAs pn junction. 

$$
[ \text { Ans. } (a) (i) 0. 7 3 6 \vee , (i i) 0. 6 7 1 \vee ; (b) (i) 1. 2 0 \vee , (i i) 1. 1 4 \vee ]
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/5ded35624a6cc4a7aed0c352986d20f463ff0df787c8509d641176adbbd340f8.jpg)



Figure 7.4 | The space charge density in a uniformly doped pn junction assuming the abrupt junction approximation.


# 7.2.2 Electric Field

An electric fi eld is created in the depletion region by the separation of positive and negative space charge densities. Figure 7.4 shows the volume charge density distribution in the pn junction assuming uniform doping and assuming an abrupt junction approximation. We will assume that the space charge region abruptly ends in the n region at $x = + x _ { n }$ and abruptly ends in the p region at $x = - x _ { p } \left( x _ { p } \right.$ is a positive quantity). 

The electric fi eld is determined from Poisson’s equation, which, for a onedimensional analysis, is 

$$
\frac {d ^ {2} \phi (x)}{d x ^ {2}} = \frac {- \rho (x)}{\epsilon_ {s}} = - \frac {d E (x)}{d x} \tag {7.11}
$$

where $\phi ( x )$ is the electric potential, E(x) is the electric fi eld, $\rho ( x )$ is the volume charge density, and $\epsilon _ { s }$ is the permittivity of the semiconductor. From Figure 7.4, the charge densities are 

$$
\rho (x) = - e N _ {a} \quad - x _ {p} <   x <   0 \tag {7.12a}
$$

and 

$$
\rho (x) = e N _ {d} \quad 0 <   x <   x _ {n} \tag {7.12b}
$$

The electric fi eld in the p region is found by integrating Equation (7.11). We have 

$$
\mathrm{E} = \int \frac {\rho (x)}{\epsilon_ {s}} d x = - \int \frac {e N _ {a}}{\epsilon_ {s}} d x = \frac {- e N _ {a}}{\epsilon_ {s}} x + C _ {1} \tag {7.13}
$$

where $C _ { 1 }$ is a constant of integration. The electric fi eld is assumed to be zero in the neutral p region for $x < - x _ { p }$ since the currents are zero in thermal equilibrium. Since there are no surface charge densities within the pn junction structure, the electric fi eld is a continuous function. The constant of integration is determined by setting $\mathrm { E } = 0 \mathrm { a t } x = - x _ { p } .$ The electric fi eld in the p region is then given by 

$$
\mathrm{E} = \frac {- e N _ {a}}{\epsilon_ {s}} (x + x _ {p}) \quad - x _ {p} \leq x \leq 0 \tag {7.14}
$$

In the n region, the electric fi eld is determined from 

$$
\mathrm{E} = \int \frac {(e N _ {d})}{\epsilon_ {s}} d x = \frac {e N _ {d}}{\epsilon_ {s}} x + C _ {2} \tag {7.15}
$$

where $C _ { 2 }$ is again a constant of integration and is determined by setting $\mathrm { \Delta E = 0 }$ at $x = x _ { n } ,$ since the E-fi eld is assumed to be zero in the n region and is a continuous function. Then 

$$
\mathrm{E} = \frac {- e N _ {d}}{\epsilon_ {s}} (x _ {n} - x) \quad 0 \leq x \leq x _ {n} \tag {7.16}
$$

The electric fi eld is also continuous at the metallurgical junction, or at $x = 0 .$ . Setting Equations (7.14) and (7.16) equal to each other at $x = 0$ gives 

$$
N _ {a} x _ {p} = N _ {d} x _ {n} \tag {7.17}
$$

Equation (7.17) states that the number of negative charges per unit area in the p region is equal to the number of positive charges per unit area in the n region. 

Figure 7.5 is a plot of the electric fi eld in the depletion region. The electric fi eld direction is from the n to the p region, or in the negative x direction for this geometry. For the uniformly doped pn junction, the E-fi eld is a linear function of distance through the junction, and the maximum (magnitude) electric fi eld occurs at the metallurgical junction. An electric fi eld exists in the depletion region even when no voltage is applied between the p and n regions. 

The potential in the junction is found by integrating the electric fi eld. In the p region then, we have 

$$
\phi (x) = - \int \mathrm{E} (x) d x = \int \frac {e N _ {a}}{\epsilon_ {s}} (x + x _ {p}) d x \tag {7.18}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/41ab2ad2b1136d253405c1d2cf78a2cd4a771d90a6a5f9267c6434d17c0bf854.jpg)



Figure 7.5 | Electric fi eld in the space charge region of a uniformly doped pn junction.


or 

$$
\phi (x) = \frac {e N _ {a}}{\epsilon_ {s}} \left(\frac {x ^ {2}}{2} + x _ {p} \cdot x\right) + C _ {1} ^ {\prime} \tag {7.19}
$$

where $C _ { 1 } ^ { \prime }$ is again a constant of integration. The potential difference through the pn junction is the important parameter, rather than the absolute potential, so we may arbitrarily set the potential equal to zero at $x = - x _ { p } .$ The constant of integration is then found as 

$$
C _ {1} ^ {\prime} = \frac {e N _ {a}}{2 \epsilon_ {s}} x _ {p} ^ {2} \tag {7.20}
$$

so that the potential in the p region can now be written as 

$$
\phi (x) = \frac {e N _ {a}}{2 \epsilon_ {s}} (x + x _ {p}) ^ {2} \quad (- x _ {p} \leq x \leq 0) \tag {7.21}
$$

The potential in the n region is determined by integrating the electric fi eld in the n region, or 

$$
\phi (x) = \int \frac {e N _ {d}}{\epsilon_ {s}} (x _ {n} - x) d x \tag {7.22}
$$

Then 

$$
\phi (x) = \frac {e N _ {d}}{\epsilon_ {s}} \left(x _ {n} \cdot x - \frac {x ^ {2}}{2}\right) + C _ {2} ^ {\prime} \tag {7.23}
$$

where $C _ { 2 } ^ { \prime }$ is another constant of integration. The potential is a continuous function, so setting Equation (7.21) equal to Equation (7.23) at the metallurgical junction, or at $x = 0$ , gives 

$$
C _ {2} ^ {\prime} = \frac {e N _ {a}}{2 \epsilon_ {s}} x _ {p} ^ {2} \tag {7.24}
$$

The potential in the n region can thus be written as 

$$
\phi (x) = \frac {e N _ {d}}{\epsilon_ {s}} \left(x _ {n} \cdot x - \frac {x ^ {2}}{2}\right) + \frac {e N _ {a}}{2 \epsilon_ {s}} x _ {p} ^ {2} \quad (0 \leq x \leq x _ {n}) \tag {7.25}
$$

Figure 7.6 is a plot of the potential through the junction and shows the quadratic dependence on distance. The magnitude of the potential at $x = x _ { n }$ is equal to the builtin potential barrier. Then from Equation (7.25), we have 

$$
V _ {b i} = \left| \phi (x = x _ {n}) \right| = \frac {e}{2 \epsilon_ {s}} \big (N _ {d} x _ {n} ^ {2} + N _ {a} x _ {p} ^ {2} \big) \tag {7.26}
$$

The potential energy of an electron is given by $E = - e \phi$ , which means that the electron potential energy also varies as a quadratic function of distance through the space charge region. The quadratic dependence on distance was shown in the energyband diagram of Figure 7.3, although we did not explicitly know the shape of the curve at that time. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/99ed79b376e7160dd95dbd27812b75480658d2978dddcea4c6284a59b94ee9c1.jpg)



Figure 7.6 | Electric potential through the space charge region of a uniformly doped pn junction.


# 7.2.3 Space Charge Width

We can determine the distance that the space charge region extends into the p and n regions from the metallurgical junction. This distance is known as the space charge width. From Equation (7.17), we may write, for example, 

$$
x _ {p} = \frac {N _ {d} x _ {n}}{N _ {a}} \tag {7.27}
$$

Then, substituting Equation (7.27) into Equation (7.26) and solving for $x _ { n } ,$ we obtain 

$$
x _ {n} = \left\{\frac {2 \epsilon_ {s} V _ {b i}}{e} \left[ \frac {N _ {a}}{N _ {d}} \right] \left[ \frac {1}{N _ {a} + N _ {d}} \right] \right\} ^ {1 / 2} \tag {7.28}
$$

Equation (7.28) gives the space charge width, or the width of the depletion region, $x _ { n }$ extending into the n-type region for the case of zero applied voltage. 

Similarly, if we solve for $x _ { n }$ from Equation (7.17) and substitute into Equation (7.26), we fi nd 

$$
x _ {p} = \left\{\frac {2 \epsilon_ {s} V _ {b i}}{e} \left[ \frac {N _ {d}}{N _ {a}} \right] \left[ \frac {1}{N _ {a} + N _ {d}} \right] \right\} ^ {1 / 2} \tag {7.29}
$$

where $x _ { p }$ is the width of the depletion region extending into the p region for the case of zero applied voltage. 

The total depletion or space charge width W is the sum of the two components, or 

$$
W = x _ {n} + x _ {p} \tag {7.30}
$$

Using Equations (7.28) and (7.29), we obtain 

$$
W = \left\{\frac {2 \epsilon_ {s} V _ {b i}}{e} \left[ \frac {N _ {a} + N _ {d}}{N _ {a} N _ {d}} \right] \right\} ^ {1 / 2} \tag {7.31}
$$

The built-in potential barrier can be determined from Equation (7.10), and then the total space charge region width is obtained using Equation (7.31). 

# EXAMPLE 7.2

Objective: Calculate the space charge width and electric fi eld in a pn junction for zero bias. 

Consider a silicon pn junction at $T = 3 0 0 \mathrm { K }$ with doping concentrations of $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

# ■ Solution

In Example 7.1, we determined the built-in potential barrier as $V _ { b i } = 0 . 6 3 5 \mathrm {  ~ V ~ } .$ . From Equation (7.31), the space charge width is 

$$
\begin{array}{l} W = \left\{\frac {2 \epsilon_ {s} V _ {b i}}{e} \left[ \frac {N _ {a} + N _ {d}}{N _ {a} N _ {d}} \right] \right\} ^ {1 / 2} \\ = \left\{\frac {2 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 6 3 5)}{1 . 6 \times 1 0 ^ {- 1 9}} \left[ \frac {1 0 ^ {1 6} + 1 0 ^ {1 5}}{(1 0 ^ {1 6}) (1 0 ^ {1 5})} \right] \right\} ^ {1 / 2} \\ = 0. 9 5 1 \times 1 0 ^ {- 4} \mathrm{cm} = 0. 9 5 1 \mu \mathrm{m} \\ \end{array}
$$

Using Equations (7.28) and (7.29), we can fi nd $x _ { n } = 0 . 8 6 4 4 \mu \mathrm { m } .$ , and $x _ { p } = 0 . 0 8 6 4 \mu \mathrm { m } .$ 

The peak electric fi eld at the metallurgical junction, using Equation (7.16) for example, is 

$$
\mathrm{E} _ {\max} = - \frac {e N _ {d} x _ {n}}{\epsilon_ {s}} = - \frac {(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 5}) (0 . 8 6 4 4 \times 1 0 ^ {- 4})}{(1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4})} = - 1. 3 4 \times 1 0 ^ {4} \mathrm{V/cm}
$$

# ■ Comment

The peak electric fi eld in the space charge region of a pn junction is quite large. We must keep in mind, however, that there is no mobile charge in this region; hence there will be no drift current. We may also note, from this example, that the width of each space charge region is a reciprocal function of the doping concentration: The depletion region will extend further into the lower-doped region. 

# ■ EXERCISE PROBLEM

Ex 7.2 A silicon pn junction at T - 300 K with zero applied bias has doping concentrations of $N _ { d } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Determine $x _ { n } , x _ { p } , W ,$ , and $| \mathrm { E } _ { \mathrm { m a x } } | .$ . 

$$
x _ {p} = 4. 1 1 \times 1 0 ^ {- 5} \mathrm{cm}, W = 4. 5 2 \times 1 0 ^ {- 5} \mathrm{cm}, \left| E _ {\max} \right| = 3. 1 8 \times 1 0 ^ {4} \mathrm{V/cm}
$$

$$
(\text { Ans. } x _ {n} = 4. 1 1 \times 1 0 ^ {- 6} \text { cm },
$$

# TEST YOUR UNDERSTANDING

TYU 7.1 Calculate $V _ { b i } , x _ { n } , x _ { p } , W ,$ and $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ for a silicon pn junction at zero bias and $T = 3 0 0 \mathrm { K }$ for doping concentrations of (a) $N _ { a } = 2 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } , N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and 

$$
\begin{array}{l} (b) N _ {a} = 4 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}, N _ {d} = 3 \times 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}. \\ W = 0. 5 0 6 4 \mu m, \left| E _ {\max} \right| = 2. 7 6 \times 1 0 ^ {4} V / c m ] \\ E _ {\max} \left| = 4. 7 7 \times 1 0 ^ {4} \mathrm{V/cm}; (b) \mathrm{V} _ {b i} = 0. 6 9 9 \mathrm{V}, x _ {n} = 0. 0 5 9 6 \mu \mathrm{m}, x _ {p} = 0. 4 4 6 9 \mu \mathrm{m}, \right. \\ \left. \left[ A n s. (a) V _ {b i} = 0. 7 7 2 V, x _ {n} = 0. 3 0 8 5 \mu m, x _ {p} = 0. 0 1 5 4 \mu m, W = 0. 3 2 4 0 \mu m, \right. \right. \\ \end{array}
$$

TYU 7.2 Repeat Exercise Problem Ex 7.2 for a GaAs pn junction. $( \mathrm { U } 9 / \Lambda _ { \mathrm { \Lambda ^ { } } } 0 \mathrm { I } \times 9 8 ^ { \circ } \mathfrak { E } = \left| \mathrm { \mathfrak { x } } \right|$ 

$$
(A n s. V _ {i} = 1. 1 8 6 \mathrm{V}, x _ {i} = 0. 0 5 5 9 0 \mu m, x _ {d} = 0. 5 5 9 0 \mu m, W = 0. 6 1 4 9 \mu m,
$$

# 7.3 | REVERSE APPLIED BIAS

If we apply a potential between the p and n regions, we will no longer be in an equilibrium condition—the Fermi energy level will no longer be constant through the system. Figure 7.7 shows the energy-band diagram of the pn junction for the case when a positive voltage is applied to the n region with respect to the p region. As the positive potential is downward, the Fermi level on the n side is below the Fermi level on the p side. The difference between the two is equal to the applied voltage in units of energy. 

The total potential barrier, indicated by $V _ { \mathrm { t o t a l } } ,$ , has increased. The applied potential is the reverse-biased condition. The total potential barrier is now given by 

$$
V _ {\text { total }} = \left| \phi_ {F n} \right| + \left| \phi_ {F p} \right| + V _ {R} \tag {7.32}
$$

where $V _ { R }$ is the magnitude of the applied reverse-biased voltage. Equation (7.32) can be rewritten as 

$$
V _ {\text { total }} = V _ {b i} + V _ {R} \tag {7.33}
$$

where $V _ { b i }$ is the same built-in potential barrier we had defi ned in thermal equilibrium. 

# 7.3.1 Space Charge Width and Electric Field

Figure 7.8 shows a pn junction with an applied reverse-biased voltage $V _ { R } .$ Also indicated in the fi gure are the electric fi eld in the space charge region and the electric fi eld $\mathrm { E _ { a p p } , }$ induced by the applied voltage. The electric fi elds in the neutral p and n regions are essentially zero, or at least very small, which means that the magnitude of the electric fi eld in the space charge region must increase above the thermal-equilibrium value due to the applied voltage. The electric fi eld originates on positive charge and terminates on negative charge; this means that the number of positive and negative charges must increase if the electric fi eld increases. For given impurity doping concentrations, the number of positive and negative charges in the depletion region can be increased only if the space charge width W increases. The space charge width W increases, therefore, with an increasing reverse-biased voltage $V _ { R } .$ We are assuming that the electric fi eld in the bulk n and p regions is zero. This assumption will become clearer in the next chapter when we discuss the current–voltage characteristics. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/40404cf3ee96a2e2cc59798a4d48db5fc4cf4323d85b027c4cf57d156244f4ee.jpg)



Figure 7.7 | Energy-band diagram of a pn junction under reverse bias.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/6060d71b7649b2cc90babeab6a094d19272fd8efe8390b853d2b95599d1ac294.jpg)



Figure 7.8 | A pn junction, with an applied reverse-biased voltage, showing the directions of the electric fi eld induced by $V _ { R }$ and the space charge electric fi eld.


In all of the previous equations, the built-in potential barrier can be replaced by the total potential barrier. The total space charge width can be written from Equation (7.31) as 

$$
W = \left\{\frac {2 \epsilon_ {s} (V _ {b i} + V _ {R})}{e} \left[ \frac {N _ {a} + N _ {d}}{N _ {a} N _ {d}} \right] \right\} ^ {1 / 2} \tag {7.34}
$$

showing that the total space charge width increases as we apply a reverse-biased voltage. By substituting the total potential barrier $V _ { \mathrm { t o t a l } }$ into Equations (7.28) and (7.29), the space charge widths in the n and p regions, respectively, can be found as a function of applied reverse-biased voltage. 

# EXAMPLE 7.3

Objective: Calculate the width of the space charge region in a pn junction when a reversebiased voltage is applied. 

Again consider a silicon pn junction at $T = 3 0 0 \mathrm { K }$ with doping concentrations of $N _ { a } =$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Assume that $n _ { i } = 1 . 5 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 3 }$ and $V _ { R } = 5 \mathrm { V } .$ . 

# ■ Solution

The built-in potential barrier was calculated in Example 7.1 for this case and is $V _ { b i } = 0 . 6 3 5 \mathrm { V }$ . The space charge width is determined from Equation (7.34). We have 

$$
W = \left\{\frac {2 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 6 3 5 + 5)}{1 . 6 \times 1 0 ^ {- 1 9}} \left[ \frac {1 0 ^ {1 6} + 1 0 ^ {1 5}}{(1 0 ^ {1 6}) (1 0 ^ {1 5})} \right] \right\} ^ {1 / 2}
$$

so that 

$$
W = 2. 8 3 \times 1 0 ^ {- 4} \mathrm{cm} = 2. 8 3 \mu \mathrm{m}
$$

# ■ Comment

The space charge width has increased from 0.951 m at zero bias to 2.83 m at a reverse bias of 5 V. 

# ■ EXERCISE PROBLEM

Ex 7.3 (a) A silicon pn junction at $T = 3 0 0$ K has doping concentrations of $N _ { a } = 5 \times$ 

$1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . A reverse-biased voltage of $V _ { R } = 4 \mathrm { V }$ is applied. 

Determine $V _ { b i } , x _ { n } , x _ { p } ,$ and W. (b) Repeat part (a) for $V _ { R } = 8 \mathrm { V } .$ 

m]  $9 L \Sigma ^ { \bullet } \mathsf { I } = \mathcal { M } \ { } ^ { \bullet } \mathsf { U } \Sigma \mathsf { t } \bar { \Sigma } ^ { \bullet } \mathsf { I } = { } ^ { d } x \ { } ^ { \bullet } \hat { \mathbf { u } } \tau \bar { I } \mathsf { \Pi } \hat { \zeta } \bar { \Sigma } \mathsf { t } \mathsf { I } ^ { \bullet } 0 = { } ^ { u } x \ ^ { \ast } 8 \mathsf { I } L ^ { \bullet } 0 = { } ^ { u } \mathcal { A } \ ( q )$ 

m;  $6 5 { \sf I } ^ { \cdot } { \sf I } = \boldsymbol { M } ^ { \cdot } \mathbf { u } \mathbf { u } ^ { \prime } \dot { \boldsymbol { \nu } } \mathsf { S } { \sf 0 } ^ { \cdot } { \sf I } = { } ^ { d _ { \cal X } } \dot { \mathbf { u } } \mathbf { u } ^ { \prime } \dot { \boldsymbol { \nu } } \mathsf { S } { \sf 0 } { \sf { I } } \dot { \mathbf { \tilde { \xi } } } 0 = { } ^ { u _ { \cal X } } \dot { \mathbf { \tilde { \xi } } } _ { \Lambda } 8 { \sf { I } } L ^ { \cdot } { \sf 0 } = { } ^ { u _ { \cal A } } \left( { \boldsymbol { p } } \right) \dot { \mathbf { \tilde { \xi } } } \mathbf { u } \mathbf { u } \mathbf { \tilde { \xi } } \mathbf { \tilde { \mathrm { s u } } } \mathbf { \tilde { \xi } }$ 

The magnitude of the electric fi eld in the depletion region increases with an applied reverse-biased voltage. The electric fi eld is still given by Equations (7.14) and (7.16) and is still a linear function of distance through the space charge region. Since $x _ { n }$ and $x _ { p }$ increase with reverse-biased voltage, the magnitude of the electric fi eld also increases. The maximum electric fi eld still occurs at the metallurgical junction. 

The maximum electric fi eld at the metallurgical junction, from Equations (7.14) and (7.16), is 

$$
\mathrm{E} _ {\max} = \frac {- e N _ {d} x _ {n}}{\epsilon_ {s}} = \frac {- e N _ {\alpha} x _ {p}}{\epsilon_ {s}} \tag {7.35}
$$

If we use either Equation (7.28) or (7.29) in conjunction with the total potential barrier, $V _ { b i } + V _ { R } ,$ then 

$$
\mathrm{E} _ {\max} = - \left\{\frac {2 e (V _ {b i} + V _ {R})}{\epsilon_ {s}} \left(\frac {N _ {a} N _ {d}}{N _ {a} + N _ {d}}\right) \right\} ^ {1 / 2} \tag {7.36}
$$

We can show that the maximum electric fi eld in the pn junction can also be written as 

$$
\mathrm{E} _ {\max} = \frac {- 2 (V _ {b i} + V _ {R})}{W} \tag {7.37}
$$

where W is the total space charge width. 

Objective: Design a pn junction to meet maximum electric fi eld and voltage specifi cations. 

Consider a silicon pn junction at $T = 3 0 0 ~ \mathrm { K }$ with a p-type doping concentration of $N _ { a } = 2 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ . Determine the n-type doping concentration such that the maximum electric fi eld is $\left| \mathrm { E } _ { \mathrm { m a x } } \right| = 2 . 5 \times 1 0 ^ { 5 }$ V/cm at a reverse-biased voltage of $V _ { R } = 2 5 \ : \mathrm { V }$ . 

# ■ Solution

The maximum electric fi eld is given by Equation (7.36). Neglecting $V _ { b i }$ compared to $V _ { R } ,$ we can write 

$$
\left| \mathrm{E} _ {\max} \right| \cong \left\{\frac {2 e \mathrm{V} _ {R}}{\epsilon_ {s}} \left(\frac {N _ {a} N _ {d}}{N _ {a} + N _ {d}}\right) \right\} ^ {1 / 2}
$$

DESIGN 

EXAMPLE 7.4 

or 

$$
2. 5 \times 1 0 ^ {5} = \left\{\frac {2 (1 . 6 \times 1 0 ^ {- 1 9}) (2 5)}{(1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4})} \left[ \frac {(2 \times 1 0 ^ {1 7}) N _ {d}}{2 \times 1 0 ^ {1 7} + N _ {d}} \right] \right\} ^ {1 / 2}
$$

which yields 

$$
N _ {d} = 8. 4 3 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}
$$

# ■ Conclusion

A smaller value of $N _ { d }$ results in a smaller value of $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ for a given reverse-biased voltage. The value of $N _ { d }$ determined in this example, then, is the maximum value that will meet the specifi cations. 

# ■ EXERCISE PROBLEM

Ex 7.4 The maximum electric fi eld in a reverse-biased GaAs pn junction at $T = 3 0 0 \mathrm { K }$ is to be limited to $\vert \mathrm { E } _ { \mathrm { m a x } } \vert = 7 . 2 \times 1 0 ^ { 4 }$ V/cm. The doping concentrations are $N _ { d } = 5 \times$ $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Determine the maximum reverse-biased voltage that can be applied. $\left( \Lambda \ \mathrm { I } \boldsymbol { \tau } ^ { \cdot } \boldsymbol { \xi } = { } ^ { \ u } \Lambda \ { } ^ { \cdot } \mathrm { s u } \mathrm { \ddot { y } } \right)$ ( 

# 7.3.2 Junction Capacitance

Since we have a separation of positive and negative charges in the depletion region, a capacitance is associated with the pn junction. Figure 7.9 shows the charge densities in the depletion region for applied reverse-biased voltages of $V _ { R }$ and $V _ { R } + d V _ { R } .$ An increase in the reverse-biased voltage $d V _ { R }$ will uncover additional positive charges in the n region and additional negative charges in the p region. The junction capacitance is defi ned as 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/3a9bdcc5549e22b4a92234e9a1bc7565781a23099db13a6c057d2146c304c33d.jpg)



Figure 7.9 | Differential change in the space charge width with a differential change in reverse-biased voltage for a uniformly doped pn junction.


$$
C ^ {\prime} = \frac {d Q ^ {\prime}}{d V _ {R}} \tag {7.38}
$$

where 

$$
d Q ^ {\prime} = e N _ {d} d x _ {n} = e N _ {a} d x _ {p} \tag {7.39}
$$

The differential charge $d Q ^ { \prime }$ is in units of $\mathrm { C } / \mathrm { c m } ^ { 2 }$ so that the capacitance $C ^ { \prime }$ is in units of farads per square centimeter F/cm2), or capacitance per unit area. 

For the total potential barrier, Equation (7.28) may be written as 

$$
x _ {n} = \left\{\frac {2 \epsilon_ {s} (V _ {b i} + V _ {R})}{e} \left[ \frac {N _ {a}}{N _ {d}} \right] \left[ \frac {1}{N _ {a} + N _ {d}} \right] \right\} ^ {1 / 2} \tag {7.40}
$$

The junction capacitance can be written as 

$$
C ^ {\prime} = \frac {d Q ^ {\prime}}{d V _ {R}} = e N _ {d} \frac {d x _ {n}}{d V _ {R}} \tag {7.41}
$$

so that 

$$
C ^ {\prime} = \left\{\frac {e \epsilon_ {s} N _ {a} N _ {d}}{2 (V _ {b i} + V _ {R}) (N _ {a} + N _ {d})} \right\} ^ {1 / 2} \tag {7.42}
$$

Exactly the same capacitance expression is obtained by considering the space charge region extending into the p region $x _ { p } .$ The junction capacitance is also referred to as the depletion layer capacitance. 

Objective: Calculate the junction capacitance of a pn junction. 

Consider the same pn junction as that in Example 7.3. Again assume that $V _ { R } = 5 \mathrm { V } .$ 

EXAMPLE 7.5 

# ■ Solution

The junction capacitance is found from Equation (7.42) as 

$$
C ^ {\prime} = \left\{\frac {(1 . 6 \times 1 0 ^ {- 1 9}) (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (1 0 ^ {1 6}) (1 0 ^ {1 5})}{2 (0 . 6 3 5 + 5) (1 0 ^ {1 6} + 1 0 ^ {1 5})} \right\} ^ {1 / 2}
$$

or 

$$
C ^ {\prime} = 3. 6 6 \times 1 0 ^ {- 9} \mathrm{F/cm} ^ {2}
$$

If the cross-sectional area of the pn junction is, for example, $A = 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 } .$ , then the total junction capacitance is 

$$
C = C ^ {\prime} \cdot A = 0. 3 6 6 \times 1 0 ^ {- 1 2} \mathrm{F} = 0. 3 6 6 \mathrm{pF}
$$

# ■ Comment

The value of junction capacitance is usually in the pF, or smaller, range. 

# ■ EXERCISE PROBLEM

Ex 7.5 Consider a GaAs pn junction at T - 300 K doped to $N _ { a } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } =$ $2 \times 1 0 ^ { 1 6 }$ cm3. (a) Calculate $V _ { b i \cdot } \left( b \right)$ Determine the junction capacitance $C ^ { \prime }$ for ${ \cal V } _ { \cal R } =$ 4 V. (c) Repeat part (b) for $V _ { R } = 8 \mathrm { V }$ . 

$$
[ \mathrm{Ans.} (a) \mathrm{V} _ {b i} = 1. 1 6 \mathrm{V}; (b) \mathrm{C} ^ {\prime} = 8. 4 8 \times 1 0 ^ {- 9} \mathrm{F/cm} ^ {2}; (\mathrm{c}) \mathrm{C} ^ {\prime} = 6. 3 6 \times 1 0 ^ {- 9} \mathrm{F/cm} ^ {2} ]
$$

If we compare Equation (7.34) for the total depletion width W of the space charge region under reverse bias and Equation (7.42) for the junction capacitance $C ^ { \prime }$ , we fi nd that we can write 

$$
C ^ {\prime} = \frac {\epsilon_ {s}}{W} \tag {7.43}
$$

Equation (7.43) is the same as the capacitance per unit area of a parallel plate capacitor. Considering Figure 7.9, we may have come to this same conclusion earlier. Keep in mind that the space charge width is a function of the reverse-biased voltage so that the junction capacitance is also a function of the reverse-biased voltage applied to the pn junction. 

# 7.3.3 One-Sided Junctions

Consider a special pn junction called the one-sided junction. If, for example, $N _ { a } \gg$ $N _ { d } ,$ this junction is referred to as a $\mathfrak { p } ^ { + } \mathfrak { n }$ junction. The total space charge width, from Equation (7.34), reduces to 

$$
W \approx \left\{\frac {2 \epsilon_ {s} (V _ {b i} + V _ {R})}{e N _ {d}} \right\} ^ {1 / 2} \tag {7.44}
$$

Considering the expressions for $x _ { n }$ and $x _ { p } ,$ we have for the $\mathfrak { p } ^ { + } \mathfrak { n }$ junction 

$$
x _ {p} \ll x _ {n} \tag {7.45}
$$

and 

$$
W \approx x _ {n} \tag {7.46}
$$

Almost the entire space charge layer extends into the low-doped region of the junction. This effect can be seen in Figure 7.10. 

The junction capacitance of the $\mathfrak { p } ^ { + } \mathfrak { n }$ junction reduces to 

$$
C ^ {\prime} \approx \left\{\frac {e \epsilon_ {s} N _ {d}}{2 (V _ {b i} + V _ {R})} \right\} ^ {1 / 2} \tag {7.47}
$$

The depletion layer capacitance of a one-sided junction is a function of the doping concentration in the low-doped region. Equation (7.47) may be manipulated to give 

$$
\left(\frac {1}{C ^ {\prime}}\right) ^ {2} = \frac {2 (V _ {b i} + V _ {R})}{e \epsilon_ {s} N _ {d}} \tag {7.48}
$$

which shows that the inverse capacitance squared is a linear function of applied reverse-biased voltage. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/47baf1f3890763362e906e274fe601f1c35be833088814d5ce4b6a5860231823.jpg)



Figure 7.10 | Space charge density of a one-sided pn junction.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/8a49566aa2ad0d60c783efe767adc6059210dec247ace7fceba133ad672bc12b.jpg)



Figure 7.11 | (1/C	)2 versus $V _ { R }$ of a uniformly doped pn junction.


Figure 7.11 shows a plot of Equation (7.48). The built-in potential of the junction can be determined by extrapolating the curve to the point where $( 1 / C ^ { \prime } ) ^ { 2 } = 0 .$ . The slope of the curve is inversely proportional to the doping concentration of the low-doped region in the junction; thus, this doping concentration can be experimentally determined. The assumptions used in the derivation of this capacitance include uniform doping in both semiconductor regions, the abrupt junction approximation, and a planar junction. 

Objective: Determine the impurity doping concentrations in a $\mathfrak { p } ^ { + } \mathfrak { n }$ junction given the parameters from Figure 7.11. 

Assume that the intercept and the slope of the curve in Figure 7.11 are $V _ { b i } = 0 . 7 2 5 \ : \mathrm { V }$ and $6 . 1 5 \times 1 0 ^ { 1 5 } ( \mathrm { F / c m ^ { 2 } } ) ^ { - 2 } ( \mathrm { V } ) ^ { - 1 }$ , respectively, for a silicon $\mathfrak { p } ^ { + } \mathfrak { n }$ junction at $T = 3 0 0 \mathrm { K } .$ . 

EXAMPLE 7.6 

# Solution

The slope of the curve in Figure 7.11 is given by 2/e $\epsilon _ { s } N _ { d } ,$ so we may write 

$$
N _ {d} = \frac {2}{e \epsilon_ {s}} \cdot \frac {1}{\text { slope }} = \frac {2}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (6 . 1 5 \times 1 0 ^ {1 5})}
$$

or 

$$
N _ {d} = 1. 9 6 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}
$$

From the expression for $V _ { b i } ,$ which is 

$$
V _ {b i} = V _ {t} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right)
$$

we can solve for $N _ { a }$ as 

$$
N _ {a} = \frac {n _ {i} ^ {2}}{N _ {d}} \exp \left(\frac {V _ {b i}}{V _ {t}}\right) = \frac {(1 . 5 \times 1 0 ^ {1 0}) ^ {2}}{1 . 9 6 3 \times 1 0 ^ {1 5}} \exp \left(\frac {0 . 7 2 5}{0 . 0 2 5 9}\right)
$$

which yields 

$$
N _ {a} = 1. 6 4 \times 1 0 ^ {1 7} \mathrm{cm} ^ {- 3}
$$

# ■ Comment

The results of this example show that $N _ { a } \gg N _ { d } ;$ therefore the assumption of a one-sided junction was valid. 

# ■ EXERCISE PROBLEM

Ex 7.6 The experimentally measured junction capacitance of a one-sided silicon $\mathfrak { n } ^ { + } \mathfrak { p }$ junction biased at $V _ { R } = 3 \mathrm { ~ V ~ }$ and at $T = 3 0 0 \mathrm { K }$ is $C = 0 . 1 0 5 \mathrm { p F } .$ The built-in potential barrier is found to be $V _ { b i } = 0 . 7 6 5 \ : \mathrm { V } .$ . The cross-sectional area is $A = 1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ . Find the doping concentrations. $( \phantom { - } _ { \varepsilon - } \mathbf { U } \mathbf { \mathscr { O } } \mathbf { \mathscr { L } } _ { \varepsilon } 0 \mathbf { I } \times \boldsymbol { \mathsf { Z } } 0 ^ { \circ } \mathscr { E } = ^ { p } N \mathbf { \mathscr { \Sigma } } _ { \varepsilon - } \mathbf { U } \mathbf { \mathscr { O } } \mathbf { \mathscr { I } } \times \mathbf { \mathscr { I } } 0 ^ { \circ } \mathscr { S } = ^ { p } N \cdot \mathbf { \mathscr { S } } \mathbf { \mathscr { U } } \mathbf { \mathscr { V } } )$ 

A one-sided pn junction is useful for experimentally determining the doping concentrations and built-in potential. 

# TEST YOUR UNDERSTANDING

TYU 7.3 (a) A silicon pn junction at $T = 3 0 0 \mathrm { K }$ is reverse biased at $V _ { R } = 8 \mathrm { V }$ . The doping concentrations are $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } .$ . Determine $x _ { n } , x _ { p } ,$ W, and $\left| \operatorname { E } _ { \operatorname { m a x } } \right| . \left( b \right)$ Repeat part (a) for a reverse-biased voltage of $V _ { R } = 1 2 \mathrm { V }$ . 

$$
x _ {p} = 1. 7 3 \times 1 0 ^ {- 5} \mathrm{cm}, W = 1. 9 0 \times 1 0 ^ {- 4} \mathrm{cm}, | E _ {\max} | = 1. 3 4 \times 1 0 ^ {5} \mathrm{V/cm} ]
$$

$$
W = 1. 5 7 \times 1 0 ^ {- 4} \mathrm{cm}, \left| \mathrm{E} _ {\max} \right| = 1. 1 1 \times 1 0 ^ {5} \mathrm{V/cm}; (b) x _ {n} = 1. 7 3 \times 1 0 ^ {- 4} \mathrm{cm},
$$

$$
\left. \left[ \text { Ans. } (a) x _ {n} = 1. 4 3 \times 1 0 ^ {- 4} \mathrm{cm}, x _ {p} = 1. 4 3 \times 1 0 ^ {- 5} \mathrm{cm}, \right. \right.
$$

TYU 7.4 A silicon pn junction at $T = 3 0 0$ K has doping concentrations of $N _ { d } = 3 \times$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 8 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , and has a cross-sectional area of $A = 5 \times$ $1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ . Determine the junction capacitance at (a) $V _ { R } = 2 \mathrm { V }$ and (b) $V _ { R } = 5 \mathrm { \ V } .$ . 478 pF] . 0 ) b pF; ( 694 . 0 ) a [Ans. ( 

# 7.4 | JUNCTION BREAKDOWN

In the last section, we determined the effects of applying a reverse-biased voltage across the pn junction. However, the reverse-biased voltage may not increase without limit; at some particular voltage, the reverse-biased current will increase rapidly. The applied voltage at this point is called the breakdown voltage. 

Two physical mechanisms give rise to the reverse-biased breakdown in a pn junction: the Zener effect and the avalanche effect. Zener breakdown occurs in highly doped pn junctions through a tunneling mechanism. In a highly doped junction, the conduction and valence bands on opposite sides of the junction are suffi ciently close during reverse bias that electrons may tunnel directly from the valence band on the p side into the conduction band on the n side. This tunneling process is schematically shown in Figure 7.12a. 

The avalanche breakdown process occurs when electrons and/or holes, moving across the space charge region, acquire suffi cient energy from the electric fi eld to create electron–hole pairs by colliding with atomic electrons within the depletion region. The avalanche process is schematically shown in Figure 7.12b. The newly created electrons and holes move in opposite directions due to the electric fi eld and thereby create a reverse-biased current. In addition, the newly generated electrons and/or holes may acquire suffi cient energy to ionize other atoms, leading to the avalanche process. For most pn junctions, the predominant breakdown mechanism will be the avalanche effect. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/d0fa8704c2f702965ea50a923798f950dfeb6de700937fec7195a707987e2fae.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/cde425573516e26476928f3a49eca32405232909b102dc4f2bde39636689e2c3.jpg)



Figure 7.12 | (a) Zener breakdown mechanism in a reverse-biased pn junction; (b) avalanche breakdown process in a reverse-biased pn junction.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/758fe364fcc3f24c21c0e339bb9a778227f868c309ae3bcc7e107622052be2a8.jpg)



Figure 7.13 | Electron and hole current components through the space charge region during avalanche multiplication.


If we assume that a reverse-biased electron current $I _ { n 0 }$ enters the depletion region at $x = 0$ as shown in Figure 7.13, the electron current $I _ { n }$ will increase with distance through the depletion region due to the avalanche process. At x - W, the electron current may be written as 

$$
I _ {n} (W) = M _ {n} I _ {n 0} \tag {7.49}
$$

where $M _ { n }$ is a multiplication factor. The hole current is increasing through the depletion region from the n to p region and reaches a maximum value at $x = 0$ . The total current is constant through the pn junction in steady state. 

We can write an expression for the incremental electron current at some point x as 

$$
d I _ {n} (x) = I _ {n} (x) \alpha_ {n} d x + I _ {p} (x) \alpha_ {p} d x \tag {7.50}
$$

where $\alpha _ { n }$ and $\alpha _ { p }$ are the electron and hole ionization rates, respectively. The ionization rates are the number of electron–hole pairs generated per unit length by an electron $( \alpha _ { n } )$ or by a hole $( \alpha _ { p } )$ . Equation (7.50) may be written as 

$$
\frac {d I _ {n} (x)}{d x} = I _ {n} (x) \alpha_ {n} + I _ {p} (x) \alpha_ {p} \tag {7.51}
$$

The total current I is given by 

$$
I = I _ {n} (x) + I _ {p} (x) \tag {7.52}
$$

which is a constant. Solving for $I _ { p } ( x )$ from Equation (7.52) and substituting into Equation (7.51), we obtain 

$$
\frac {d I _ {n} (x)}{d x} + (\alpha_ {p} - \alpha_ {n}) I _ {n} (x) = \alpha_ {p} I \tag {7.53}
$$

If we make the assumption that the electron and hole ionization rates are equal so that 

$$
\alpha_ {n} = \alpha_ {p} \equiv \alpha \tag {7.54}
$$

then Equation (7.53) may be simplifi ed and integrated through the space charge region. We will obtain 

$$
I _ {n} (W) - I _ {n} (0) = I \int_ {0} ^ {W} \alpha d x \tag {7.55}
$$

Using Equation (7.49), Equation (7.55) may be written as 

$$
\frac {M _ {n} I _ {n 0} - I _ {n} (0)}{I} = \int_ {0} ^ {W} \alpha d x \tag {7.56}
$$

Since Mn $I _ { n 0 } \approx I$ and since $I _ { n } ( 0 ) = I _ { n 0 } .$ Equation (7.56) becomes 

$$
1 - \frac {1}{M _ {n}} = \int_ {0} ^ {W} \alpha d x \tag {7.57}
$$

The avalanche breakdown voltage is defi ned to be the voltage at which $M _ { n }$ approaches infi nity. The avalanche breakdown condition is then given by 

$$
\int_ {0} ^ {W} \alpha d x = 1 \tag {7.58}
$$

The ionization rates are strong functions of electric fi eld and, since the electric fi eld is not constant through the space charge region, Equation (7.58) is not easy to evaluate. 

If we consider, for example, a one-sided $\mathfrak { p } ^ { + } \mathfrak { n }$ junction, the maximum electric fi eld is given by 

$$
\mathrm{E} _ {\max} = \frac {e N _ {d} x _ {n}}{\epsilon_ {s}} \tag {7.59}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/b136feef3b9cae26596319683ebe86ba07d503c7822bc302a996c35013feed56.jpg)



Figure 7.14 | Critical electric fi eld at breakdown in a onesided junction as a function of impurity doping concentrations. (From Sze and $N _ { g } / I 4 J . )$


The depletion width $x _ { n }$ is given approximately as 

$$
x _ {n} \approx \left\{\frac {2 \epsilon_ {s} V _ {R}}{e} \cdot \frac {1}{N _ {d}} \right\} ^ {1 / 2} \tag {7.60}
$$

where $V _ { R }$ is the magnitude of the applied reverse-biased voltage. We have neglected the built-in potential $V _ { b i }$ . 

If we now defi ne $V _ { R }$ to be the breakdown voltage $V _ { B } ,$ the maximum electric fi eld, $\mathrm { { E } } _ { \operatorname* { m a x } } .$ will be defi ned as a critical electric fi eld, $\mathrm { E } _ { \mathrm { c r i t } } ,$ at breakdown. Combining Equations (7.59) and (7.60), we may write 

$$
V _ {B} = \frac {\epsilon_ {s} \mathrm{E} _ {\text {crit}} ^ {2}}{2 e N _ {B}} \tag {7.61}
$$

where $N _ { B }$ is the semiconductor doping in the low-doped region of the one-sided junction. The critical electric fi eld, plotted in Figure 7.14, is a slight function of doping. 

We have been considering a uniformly doped planar junction. The breakdown voltage will decrease for a linearly graded junction. (See Section 7.5.) Figure 7.15 shows a plot of the breakdown voltage for a one-sided abrupt junction and a linearly graded junction. If we take into account the curvature of a diffused junction as well, the breakdown voltage will be further degraded. 

Objective: Design an ideal one-sided $\mathfrak { n } ^ { + } \mathfrak { p }$ junction diode to meet a breakdown voltage specifi cation. 

Consider a silicon pn junction diode at $T = 3 0 0 ~ \mathrm { K } .$ Assume that $N _ { d } = 3 \times 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ . Design the diode such that the breakdown voltage is $V _ { B } = 1 0 0 \mathrm { V } $ . 

# Solution

From Figure 7.15, we fi nd that the doping concentration in the low-doped side of a one-sided abrupt junction should be approximately $4 \times 1 0 ^ { 1 5 }$ cm3 for a breakdown voltage of 100 V. 

DESIGN EXAMPLE 7.7 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/0c5a3d6a39202ebecf3046f5f2b2781f699a177830b556f09fec27cdcd7b10cd.jpg)



Figure 7.15 | Breakdown voltage versus impurity concentration in uniformly doped and linearly graded junctions. (From Sze [14].)


For a doping concentration of $4 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , the critical electric fi eld, from Figure 7.14, is approximately $3 . 7 \times 1 0 ^ { 5 } \mathrm { V / c m } .$ . Then, using Equation (7.61), we fi nd the breakdown voltage as 

$$
V _ {B} = \frac {\epsilon_ {s} \mathrm{E} _ {\text {crit}} ^ {2}}{2 \mathrm{e} N _ {B}} = \frac {(1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (3 . 7 \times 1 0 ^ {5}) ^ {2}}{2 (1 . 6 \times 1 0 ^ {- 1 9}) (4 \times 1 0 ^ {1 5})} = 1 1 0 \mathrm{V}
$$

which correlates very well with the results from Figure 7.15. 

# ■ Conclusion

As Figure 7.15 shows, the breakdown voltage increases as the doping concentration decreases in the low-doped region. 

# ■ EXERCISE PROBLEM

Ex 7.7 A one-sided, planar, uniformly doped silicon pn junction diode is required to have a reverse-biased breakdown voltage of $V _ { B } = 6 0 \mathrm { V }$ . What is the maximum doping concentration in the low-doped region such that this specifi cation is met? 

$$
(\text { Ans. } N _ {B} \approx 8 \times 1 0 ^ {1 5} \text { cm } ^ {- 3})
$$

# *7.5 | NONUNIFORMLY DOPED JUNCTIONS

In the pn junctions considered so far, we have assumed that each semiconductor region has been uniformly doped. In actual pn junction structures, this is rarely true. In some electronic applications, specifi c nonuniform doping profi les are used to obtain special pn junction capacitance characteristics. 

# 7.5.1 Linearly Graded Junctions

If we start with a uniformly doped n-type semiconductor, for example, and diffuse acceptor atoms through the surface, the impurity concentrations will tend to be like those shown in Figure 7.16. The point $x = x ^ { \prime }$ on the fi gure corresponds to the metallurgical junction. The depletion region extends into the p and n regions from the metallurgical junction as we have discussed previously. The net p-type doping concentration near the metallurgical junction may be approximated as a linear function of distance from the metallurgical junction. Likewise, as a fi rst approximation, the net n-type doping concentration is also a linear function of distance extending into the n region from the metallurgical junction. This effective doping profi le is referred to as a linearly graded junction. 

Figure 7.17 shows the space charge density in the depletion region of the linearly graded junction. For convenience, the metallurgical junction is placed at $x = 0 .$ . The space charge density can be written as 

$$
\rho (x) = e a x \tag {7.62}
$$

where a is the gradient of the net impurity concentration. 

The electric fi eld and potential in the space charge region can be determined from Poisson’s equation. We can write 

$$
\frac {d \mathrm{E}}{d x} = \frac {\rho (x)}{\epsilon_ {s}} = \frac {e a x}{\epsilon_ {s}} \tag {7.63}
$$

so that the electric fi eld can be found by integration as 

$$
\mathrm{E} = \int \frac {e a x}{\epsilon_ {s}} d x = \frac {e a}{2 \epsilon_ {s}} \left(x ^ {2} - x _ {0} ^ {2}\right) \tag {7.64}
$$

The electric fi eld in the linearly graded junction is a quadratic function of distance rather than the linear function found in the uniformly doped junction. The maximum electric fi eld again occurs at the metallurgical junction. We may note that the electric fi eld is zero at both $x = + x _ { 0 }$ and at $x = - x _ { 0 } .$ The electric fi eld in a nonuniformly doped semiconductor is not exactly zero, but the magnitude of this fi eld is small, so setting $\mathrm { E } = 0$ in the bulk regions is still a good approximation. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/5ef88f45745987bd1200bfdad7a5db90fded07f857bf4c85fd660a6feefc8d08.jpg)



Figure 7.16 | Impurity concentrations of a pn junction with a nonuniformly doped p region.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/6e30760e10f2ceec84c3bf6c78279fec08c376b7b93e6288232d1d6910989902.jpg)



Figure 7.17 | Space charge density in a linearly graded pn junction.


The potential is again found by integrating the electric fi eld as 

$$
\phi (x) = - \int \mathrm{E} d x \tag {7.65}
$$

If we arbitrarily set $\phi = 0 \mathrm { a t } x = - x _ { 0 } .$ , then the potential through the junction is 

$$
\phi (x) = \frac {- e a}{2 \epsilon_ {s}} \left(\frac {x ^ {3}}{3} - x _ {0} ^ {2} x\right) + \frac {e a}{3 \epsilon_ {s}} x _ {0} ^ {3} \tag {7.66}
$$

The magnitude of the potential at $x = + x _ { 0 }$ will equal the built-in potential barrier for this function. We then have that 

$$
\phi (x _ {0}) = \frac {2}{3} \cdot \frac {e a x _ {0} ^ {3}}{\epsilon_ {s}} = V _ {b i} \tag {7.67}
$$

Another expression for the built-in potential barrier for a linearly graded junction can be approximated from the expression used for a uniformly doped junction. We can write 

$$
V _ {b i} = V _ {t} \ln \left[ \frac {N _ {d} (x _ {0}) N _ {a} (- x _ {0})}{n _ {i} ^ {2}} \right] \tag {7.68}
$$

where $N _ { d } ( x _ { 0 } )$ and $N _ { a } ( - x _ { 0 } )$ are the doping concentrations at the edges of the space charge region. We can relate these doping concentrations to the gradient, so that 

$$
N _ {d} (x _ {0}) = a x _ {0} \tag {7.69a}
$$

and 

$$
N _ {a} (- x _ {0}) = a x _ {0} \tag {7.69b}
$$

Then the built-in potential barrier for the linearly graded junction becomes 

$$
V _ {b i} = V _ {t} \ln \left(\frac {a x _ {0}}{n _ {i}}\right) ^ {2} \tag {7.70}
$$

There may be situations in which the doping gradient is not the same on either side of the junction, but we will not consider that condition here. 

If a reverse-biased voltage is applied to the junction, the potential barrier increases. The built-in potential barrier $V _ { b i }$ in the above equations is then replaced by the total potential barrier $V _ { b i } + V _ { R } .$ . Solving for $x _ { 0 }$ from Equation (7.67) and using the total potential barrier, we obtain 

$$
x _ {0} = \left\{\frac {3}{2} \cdot \frac {\epsilon_ {s}}{e a} (V _ {b i} + V _ {R}) \right\} ^ {1 / 3} \tag {7.71}
$$

The junction capacitance per unit area can be determined by the same method that we used for the uniformly doped junction. Figure 7.18 shows the differential charge $d Q ^ { \prime }$ , which is uncovered as a differential voltage $d V _ { R }$ is applied. The junction capacitance is then 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/982e6b2ee994b419a7ac0ec9fb9d44ac28024d8a3aee44b8640f2c6d11f340e4.jpg)



Figure 7.18 | Differential change in space charge width with a differential change in reverse-biased voltage for a linearly graded pn junction.


$$
C ^ {\prime} = \frac {d Q ^ {\prime}}{d V _ {R}} = (e a x _ {0}) \frac {d x _ {0}}{d V _ {R}} \tag {7.72}
$$

Using Equation (7.71), we obtain1 

$$
C ^ {\prime} = \left\{\frac {e a \epsilon_ {s} ^ {2}}{1 2 (V _ {b i} + V _ {R})} \right\} ^ {1 / 3} \tag {7.73}
$$

We may note that $C ^ { \prime }$ is proportional to $( V _ { b i } \ : + \ : V _ { R } ) ^ { - 1 / 3 }$ for the linearly graded junction as compared to $C ^ { \prime } \alpha ( V _ { b i } + V _ { R } ) ^ { - 1 / 2 }$ for the uniformly doped junction. In the linearly graded junction, the capacitance is less dependent on reverse-biased voltage than in the uniformly doped junction. 

# 7.5.2 Hyperabrupt Junctions

The uniformly doped junction and linearly graded junction are not the only possible doping profi les. Figure 7.19 shows a generalized one-sided $\mathfrak { p } ^ { + } \mathfrak { n }$ junction where the generalized n-type doping concentration for $x > 0$ is given by 

$$
N = B x ^ {m} \tag {7.74}
$$

The case of $m = 0$ corresponds to the uniformly doped junction, and $m = + 1$ corresponds to the linearly graded junction just discussed. The cases of $m = + 2$ and $m = + 3$ shown would approximate a fairly low-doped epitaxial n-type layer grown on a much more heavily doped n substrate layer. When the value of m is negative, we have what is referred to as a hyperabrupt junction. In this case, the n-type doping is larger near the metallurgical junction than in the bulk semiconductor. Equation (7.74) is used to approximate the n-type doping over a small region near $x = x _ { 0 }$ and does not hold at x - 0 when m is negative. 

<table><tr><td>p+</td><td>n</td></tr><tr><td colspan="2">x=0</td></tr></table>

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/572d6eeb905d01fe8e67fb8e21c67201d1b68213eb0a8c9af1e2605cf9e000fb.jpg)



Figure 7.19 | Generalized doping profi les of a one-sided pn junction.



(From Sze [14].)


The junction capacitance can be derived using the same analysis method as before and is given by 

$$
C ^ {\prime} = \left\{\frac {e B \epsilon_ {s} ^ {(m + 1)}}{(m + 2) (V _ {b i} + V _ {R})} \right\} ^ {1 / (m + 2)} \tag {7.75}
$$

When m is negative, the capacitance becomes a very strong function of reverse-biased voltage, a desired characteristic in varactor diodes. The term varactor comes from the words variable reactor and means a device whose reactance can be varied in a controlled manner with bias voltage. 

If a varactor diode and an inductance are in parallel, the resonant frequency of the LC circuit is 

$$
f _ {r} = \frac {1}{2 \pi \sqrt {L C}} \tag {7.76}
$$

The capacitance of the diode, from Equation (7.75), can be written in the form 

$$
C = C _ {0} (V _ {b i} + V _ {R}) ^ {- 1 / (m + 2)} \tag {7.77}
$$

In a circuit application, we would, in general, like to have the resonant frequency be a linear function of reverse-biased voltage $V _ { R } ,$ so we need 

$$
C \alpha V ^ {- 2} \tag {7.78}
$$

From Equation (7.77), the parameter m required is found from 

$$
\frac {1}{m + 2} = 2 \tag {7.79a}
$$

or 

$$
m = - \frac {3}{2} \tag {7.79b}
$$

A specifi c doping profi le will yield the desired capacitance characteristic. 

# 7.6 | SUMMARY

■ A uniformly doped pn junction is initially considered, in which one region of a semiconductor is uniformly doped with acceptor impurities and the adjacent region is uniformly doped with donor impurities. 

■ A space charge region, or depletion region, is formed on either side of the metallurgical junction separating the n and p regions. This region is essentially depleted of any mobile electrons or holes. A net positive charge density, due to the positively charged donor impurity ions, exists in the n region and a net negative charge density, due to the negatively charged acceptor impurity ions, exists in the p region. 

■ An electric fi eld exists in the depletion region due to the net space charge density. The direction of the electric fi eld is from the n region to the p region. 

■ A potential difference exists across the space charge region. Under zero applied bias, this potential difference, known as the built-in potential barrier, maintains thermal equilibrium and holds back majority carrier electrons in the n region and majority carrier holes in the p region. 

■ An applied reverse-biased voltage (n region positive with respect to the p region) increases the potential barrier, the space charge width, and the magnitude of the electric fi eld. 

■ As the reverse-biased voltage changes, the amount of charge in the depletion region changes. This change in charge with voltage defi nes the junction capacitance. 

■ Avalanche breakdown occurs when a suffi ciently large reverse-biased voltage is applied to the pn junction. A large reverse-biased current may then be induced in the pn junction. The breakdown voltage, as a function of the doping concentrations in the pn junction, is derived. In a one-sided pn junction, the breakdown voltage is a function of the doping concentration in the low-doped region. 

■ The linearly graded junction represents a nonuniformly doped pn junction. Expressions for the electric fi eld, built-in potential barrier, and junction capacitance are derived. The functional relationships differ from those of the uniformly doped junction. 

■ Specifi c doping profi les can be used to obtain specifi c capacitance characteristics. A hyperabrupt junction is one in which the doping decreases away from the metallurgical junction. This type of junction is advantageous in varactor diodes that are used in resonant circuits. 

# GLOSSARY OF IMPORTANT TERMS

abrupt junction approximation The assumption that there is an abrupt discontinuity in space charge density between the space charge region and the neutral semiconductor region. 

avalanche breakdown The process whereby a large reverse-biased pn junction current is created due to the generation of electron–hole pairs by the collision of electrons and/or holes with atomic electrons within the space charge region. 

built-in potential barrier The electrostatic potential difference between the p and n regions of a pn junction in thermal equilibrium. 

critical electric fi eld The peak electric fi eld in the space charge region at breakdown. 

depletion layer capacitance Another term for junction capacitance. 

depletion region Another term for space charge region. 

hyperabrupt junction A pn junction in which the doping concentration on one side decreases away from the metallurgical junction to achieve a specifi c capacitance– voltage characteristic. 

junction capacitance The capacitance of the pn junction under reverse bias. 

linearly graded junction A pn junction in which the doping concentrations on either side of the metallurgical junction are approximated by a linear distribution. 

metallurgical junction The interface between the p- and n-doped regions of a pn junction. 

one-sided junction A pn junction in which one side of the junction is much more heavily doped than the adjacent side. 

reverse bias The condition in which a positive voltage is applied to the n region with respect to the p region of a pn junction so that the potential barrier between the two regions increases above the thermal-equilibrium built-in potential barrier. 

space charge region The region on either side of the metallurgical junction in which there is a net charge density due to ionized donors in the n region and ionized acceptors in the p region. 

space charge width The width of the space charge region, a function of doping concentrations and applied voltage. 

varactor diode A diode whose reactance can be varied in a controlled manner with bias voltage. 

# CHECKPOINT

After studying this chapter, the reader should have the ability to: 

■ Describe why and how the space charge region is formed. 

■ Draw the energy-band diagram of a zero-biased and reverse-biased pn junction. 

■ Defi ne and derive the expression of the built-in potential barrier voltage. 

■ Derive the expression for the electric fi eld in space charge region of the pn junction. 

■ Describe what happens to the parameters of the space charge region when a reversebiased voltage is applied. 

■ Defi ne and explain the junction capacitance. 

■ Describe the characteristics and properties of a one-sided pn junction. 

■ Describe the avalanche breakdown mechanism in a reverse-biased pn junction. 

■ Describe how a linearly graded junction is formed. 

■ Defi ne a hyperabrupt junction. 

# REVIEW QUESTIONS

1. Defi ne the built-in potential voltage and describe how it maintains thermal equilibrium. 

2. Why is an electric fi eld formed in the space charge region? Why is the electric fi eld a linear function of distance in a uniformly doped pn junction? 

3. Where does the maximum electric fi eld occur in the space charge region? 

4. Why is the space charge width larger in the lower doped side of a pn junction? 

5. What is the functional dependence of the space charge width on reverse-biased voltage? 

6. Why does the space charge width increase with reverse-biased voltage? 

7. Why does a capacitance exist in a reverse-biased pn junction? Why does the capacitance decrease with increasing reverse-biased voltage? 

8. What is a one-sided pn junction? What parameters can be determined in a one-sided pn junction? 

9. Why does the breakdown voltage of a pn junction decrease as the doping concentration increases? 

10. What is a linearly graded junction? 

11. What is a hyperabrupt junction and what is one advantage or characteristic of such a junction? 

# PROBLEMS

# Section 7.2 Zero Applied Bias

7.1 (a) Calculate $V _ { b i }$ in a silicon pn junction at T - 300 K for (a) $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = ( i ) 2 \times 1 0 ^ { 1 5 } , ( i i ) 2 \times 1 0 ^ { 1 6 }$ , and (iii) $2 \times 1 0 ^ { 1 7 }$ cm3. (b) Repeat part (a) for $N _ { a } = 2 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ . 

7.2 Calculate the built-in potential barrier, $V _ { b i ; }$ , for Si, Ge, and GaAs pn junctions if they each have the following dopant concentrations at $T = 3 0 0 \mathrm { K } \mathrm { \Omega }$ : 

7.3 (a) Plot the built-in potential barrier for a symmetrical $( N _ { a } = N _ { d } )$ silicon pn junction at $T = 3 0 0 \mathrm { K }$ over the range $1 0 ^ { 1 4 } \leq N _ { a } = N _ { d } \leq 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } .$ . (b) Repeat part (a) for a GaAs pn junction. (c) Repeat parts (a) and (b) for $T = 4 0 0 \mathrm { K }$ . 

7.4 An abrupt silicon pn junction at zero bias has dopant concentrations of $N _ { a } = 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } . T = 3 0 0 \mathrm { K }$ . (a) Calculate the Fermi level on each side of the junction with respect to the intrinsic Fermi level. (b) Sketch the equilibrium energyband diagram for the junction and determine $V _ { b i }$ from the diagram and the results of part (a). (c) Calculate $V _ { b i }$ using Equation (7.10), and compare the results to part (b). (d ) Determine $x _ { n } , x _ { p } ,$ and the peak electric fi eld for this junction. 

7.5 Repeat problem 7.4 for the case when the doping concentrations are $N _ { a } = N _ { d } = 2 \times$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . 

7.6 A silicon pn junction in thermal equilibrium at T - 300 K is doped such that $E _ { F } - E _ { F i } = 0 . 3 6 5 \ : \mathrm { e V }$ in the n region and $E _ { F i } - E _ { F } = 0 . 3 3 0 \ : \mathrm { e V }$ in the p region. 

(a) Sketch the energy-band diagram for the pn junction. (b) Find the impurity doping concentration in each region. (c) Determine $V _ { b i \cdot }$ . 

7.7 Consider a uniformly doped GaAs pn junction with doping concentrations of $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Plot the built-in potential barrier $V _ { b i }$ versus temperature over the range $2 0 0 \leq T \leq 4 0 0 \mathrm { K } .$ . 

7.8 (a) Consider a uniformly doped silicon pn junction at $T = 3 0 0 \mathrm { K } .$ At zero bias, 25 percent of the total space charge region is in the n-region. The built-in potential barrier is $V _ { b i } = 0 . 7 1 0 \mathrm { V } .$ . Determine (i) $N _ { a } , ( i i ) N _ { d } , ( i i i ) x _ { n } , ( i \nu ) x _ { p } ,$ and $\left( \nu \right) \left| \operatorname { E } _ { \operatorname* { m a x } } \right| . \left( b \right)$ Repeat part (a) for a GaAs pn junction with $V _ { b i } = 1 . 1 8 0 \mathrm { V } .$ 

7.9 Consider the impurity doping profi le shown in Figure $\mathrm { P } 7 . 9$ in a silicon pn junction. For zero applied voltage, (a) determine $V _ { b i } , \left( b \right)$ calculate $x _ { n }$ and $x _ { p } , ( c )$ sketch the thermal equilibrium energy-band diagram, and (d) plot the electric fi eld versus distance through the junction. 

7.10 Consider a uniformly doped silicon pn junction with doping concentrations $N _ { a } = 2 \times$ $1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . (a) Determine $V _ { b i }$ at $T = 3 0 0 \mathrm { K } . ( b )$ Determine the temperature at which $V _ { b i }$ increases by 2 percent. (Trial and error may have to be used.) 

7.11 The doping concentrations in a uniformly doped silicon pn junction are $N _ { a } = 4 \times$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The measured built-in potential barrier is $V _ { b i } =$ 0.550 V. Determine the temperature at which this result occurs. 

7.12 An “isotype” step junction is one in which the same impurity type doping changes from one concentration value to another value. An n-n isotype doping profi le is shown in Figure P7.12. (a) Sketch the thermal equilibrium energy-band diagram of the isotype junction. (b) Using the energy-band diagram, determine the built-in potential barrier. (c) Discuss the charge distribution through the junction. 

7.13 A particular type of junction is an n region adjacent to an intrinsic region. This junction can be modeled as an n-type region to a lightly doped p-type region. Assume the doping concentrations in silicon at $T = 3 0 0 \mathrm { K }$ are $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } =$ $1 0 ^ { 1 2 } \mathrm { c m } ^ { - 3 }$ . For zero applied bias, determine (a) $V _ { b i } , \left( b \right) { \boldsymbol { x } } _ { n } , \left( c \right) { \boldsymbol { x } } _ { p } ,$ and $( d ) \left| \mathrm { E } _ { \operatorname* { m a x } } \right|$ . Sketch the electric fi eld versus distance through the junction. 

7.14 We are assuming an abrupt depletion approximation for the space charge region. That is, no free carriers exist within the depletion region and the semiconductor abruptly changes to a neutral region outside the space charge region. This approximation is 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/54b59ed610064d6f2ee7e861f14426b9d84e8782253247dfb036abd1f95a6ea7.jpg)



Figure P7.9 | Figure for Problem 7.9.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/03b3ca7630d25daf179c1f7f98d02045c74758721a76f6226dbf6bf544147520.jpg)



Figure P7.12 | Figure for Problem 7.12.


adequate for most applications, but the abrupt transition does not exist. The space charge region changes over a distance of a few Debye lengths, where the Debye length in the n region is given by 

$$
L _ {D} = \left[ \frac {\epsilon_ {s} k T}{e ^ {2} N _ {d}} \right] ^ {1 / 2}
$$

Calculate $L _ { D }$ and fi nd the ratio of $L _ { D } / x _ { n }$ for the following conditions. The p-type doping concentration is $N _ { a } = 8 \times 1 0 ^ { 1 7 }$ cm3 and the n-type doping concentration is (a) $N _ { d } = 8 \times 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 } , ( b ) N _ { d } = 2 . 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , and (c) $N _ { d } = 8 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ . 

7.15 Examine the electric fi eld versus distance through a uniformly doped silicon pn junction at $T = 3 0 0 \mathrm { K }$ as a function of doping concentrations. Assume zero applied bias. Sketch the electric fi eld versus distance through the space charge region and calculate $| \mathrm { E } _ { \mathrm { m a x } } |$ for: (a) $N _ { a } = 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $1 0 ^ { 1 4 } \leq N _ { d } \leq 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and (b) $N _ { a } = 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ and $1 0 ^ { 1 4 } \leq$ $N _ { d } \leq 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } .$ . (c) What can be said about the results for $N _ { d } \geq 1 0 0 N _ { a } \mathrm { o r } N _ { a } \geq 1 0 0 N _ { d } ?$ 

# Section 7.3 Reverse Applied Bias

7.16 An abrupt silicon pn junction at T - 300 K has impurity doping concentrations of $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Calculate $( a ) \ V _ { b i } , ( b )$ W at (i) $V _ { R } = 0$ and (ii) $V _ { R } = 5 \mathrm { V } ,$ and $\left( c \right) \left| \mathrm { E } _ { \operatorname* { m a x } } \right|$ at (i) $V _ { R } = 0$ and (ii) $V _ { R } = 5 .$ 

7.17 Consider the pn junction described in Problem 7.10 for $T = 3 0 0 \mathrm { K }$ . The crosssectional area of the junction is $2 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ and the applied reverse-biased voltage is $V _ { R } = 2 . 5 \ : \mathrm { V } .$ Calculate (a) $\begin{array} { r } { V _ { b i } , \left( b \right) \boldsymbol { x } _ { n } , \boldsymbol { x } _ { p } , W , \left( c \right) \vert \mathrm { E } _ { \operatorname* { m a x } } \vert , } \end{array}$ and (d) the junction capacitance. 

7.18 An ideal one-sided silicon $\mathfrak { p } ^ { + } \mathfrak { n }$ junction at $T = 3 0 0 ~ \mathrm { K }$ is uniformly doped on both sides of the metallurgical junction. It is found that the doping relation is $N _ { a } = 8 0 N _ { d }$ and the built-in potential barrier is $V _ { b i } = 0 . 7 4 0 \ : \mathrm { V } .$ . A reverse-biased voltage of $V _ { R } = 1 0 \mathrm { V }$ is applied. Determine (a) $N _ { a } , N _ { d } ; \left( b \right) x _ { p } , x _ { n } ; \left( c \right) | \mathrm { E } _ { \operatorname* { m a x } } | ;$ and $( d ) C _ { j } ^ { \prime } .$ 

7.19 A silicon $\mathfrak { n } ^ { + } \mathfrak { p }$ junction is biased at $V _ { R } = 5 \mathrm { V } .$ (a) Determine the change in built-in potential barrier if the doping concentration in the p region increases by a factor of 3. (b) Determine the ratio of junction capacitance when the acceptor doping is $3 N _ { a }$ compared to that when the acceptor doping is $N _ { a } . \mathrm { ~ } ( c )$ Why does the junction capacitance increase when the doping concentration increases? 

7.20 (a) The peak electric fi eld in a reverse-biased silicon pn junction is $| \mathrm { E } _ { \mathrm { m a x } } | = 3 \times 1 0 ^ { 5 }$ V/cm. The doping concentrations are $N _ { d } = 4 \times 1 0 ^ { 1 5 }$ cm3 and $N _ { a } = 4 \times 1 0 ^ { 1 7 }$ cm3. Find the magnitude of the reverse-biased voltage. (b) Repeat part (a) for $N _ { d } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 4 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } .$ (c) Repeat part (a) for $N _ { d } = N _ { a } = 4 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 } .$ . 

7.21 Consider two pn silicon junctions at $T = 3 0 0$ K reverse biased at $V _ { R } = 5 \mathrm { V } .$ . The impurity doping concentrations in junction A are $N _ { a } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , and those in junction B are $N _ { a } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Calculate the ratio of the following parameters for junction A to junction B: (a) $W , \left( b \right) | \mathrm { E } _ { \operatorname* { m a x } } | ,$ and $( c ) C _ { j } ^ { \prime } .$ 

7.22 Consider a uniformly doped GaAs pn junction at $T = 3 0 0 \mathrm { K }$ . The junction capacitance at zero bias is $C _ { j } ( 0 )$ and the junction capacitance with a 10-V reverse-biased voltage is $C _ { j } ( 1 0 )$ . The ratio of the capacitances is 

$$
\frac {C _ {j} (0)}{C _ {j} (1 0)} = 3. 1 3
$$

Also under reverse bias, the space charge width into the p region is 0.2 of the total space charge width. Determine (a) $V _ { b i }$ and $( b ) N _ { a } , N _ { d } .$ . 

7.23 A GaAs pn junction at $T = 3 0 0$ K has impurity doping concentrations of $N _ { a } = 2 \times 1 0 ^ { 1 6 }$ $\mathrm { c m } ^ { - 3 }$ and $N _ { d } = 5 \times 1 0 ^ { 1 5 }$ cm3. It is determined that the ratio of junction capacitance at two reverse-biased voltages is $C _ { j } ^ { ' } \left( V _ { R 1 } \right) / C _ { j } ^ { ' } ( V _ { R 2 } ) = 1 . 5$ , where $V _ { R 1 } = 0 . 5 \ : \mathrm { V } .$ Determine $V _ { R 2 } .$ . 

7.24 (a) The impurity doping concentrations in a silicon pn junction at $T = 3 0 0 \mathrm { K }$ are $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The cross-sectional area of the pn junction is $5 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . Determine the junction capacitance at (i) $V _ { R } = 0$ and (ii) ${ \cal V } _ { R } =$ 5 V. (b) Repeat part (a) for a GaAs pn junction. 

7.25 An abrupt silicon pn junction at $T = 3 0 0 \mathrm { K }$ is uniformly doped with $N _ { a } = 2 \times$ $1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The cross-sectional area of the pn junction is $8 \times$ $1 0 ^ { - 4 } \mathrm { c m } ^ { 2 } .$ . An inductance is placed in parallel with the pn junction. (a) With a reversebiased voltage of $V _ { R } = 1 0 \mathrm { V }$ applied to the pn junction, the resonant frequency of the circuit is $f = 1 . 2 5$ MHz. What is the value of the inductance? (b) Using the results of part (a), what is the resonant frequency if the reverse-biased voltage is (i) $V _ { R } = 1 \mathrm { V }$ and (ii) $V _ { R } = 5 \mathrm { V } ?$ 

7.26 (a) A uniformly doped silicon $\mathfrak { p } ^ { + } \mathfrak { n }$ junction at $T = 3 0 0 \mathrm { K }$ is to be designed such that, at a reverse-biased of $V _ { R } = 1 0 ~ \mathrm { V } ,$ , the maximum electric fi eld is limited to $| \mathrm { E } _ { \operatorname* { m a x } } | = 2 . 5 \times$ $1 0 ^ { 5 } \mathrm { V / c m }$ . Determine the maximum doping concentration in the n region. (Use an approximate value for $V _ { b i \cdot } )$ (b) Repeat part (a) if the maximum electric fi eld is limited to $| \mathrm { E } _ { \mathrm { m a x } } | = 1 0 ^ { 5 } \mathrm { V } / \mathrm { c m }$ . 

7.27 (a) A GaAs pn junction at $T = 3 0 0 \mathrm { K } ,$ with a cross-sectional area of $1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ , is to be designed that meets the following specifi cations. At a reverse-biased voltage of $V _ { R } = 2 \mathrm { V } ,$ 20 percent of the total space charge width is to be in the p region and the total junction capacitance is to be 0.6 pF. Determine $N _ { a } , N _ { d } ,$ and W. (b) Repeat part (a) if $V _ { R } = 5 \mathrm { V } .$ 

7.28 A silicon pn junction at $T = 3 0 0$ K has the doping profi le shown in Figure P7.28. Calculate $( a ) \ V _ { b i } , ( b ) \ x { x _ { n } }$ and $x _ { p }$ at zero bias, and (c) the applied bias required so that $x _ { n } = 3 0 \mu \mathrm { m }$ . 

7.29 Consider a silicon pn junction with the doping profi le shown in Figure P7.29. $T = 3 0 0 \mathrm { K } .$ . (a) Calculate the applied reverse-biased voltage required so that the space charge region extends entirely through the p region. (b) Determine the space charge width into the n region with the reverse-biased voltage calculated in part (a). (c) Calculate the peak electric fi eld for this applied voltage. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/d37f46bb71e147c7840c8f7f48bc3f6827079c84a6bc5cd07c38b3ece3d1f56c.jpg)



Figure P7.28 | Figure for Problem 7.28.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/a4dfc99077e7cbeb4afd58d19d6bb8ada267cd0d50e04e9740fe63fe59899801.jpg)



Figure P7.29 | Figure for Problem 7.29.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/9539a9bc7d50ec096116ddbd61a63899cd3eb3133bb6d56419bbabfc158a3346.jpg)



Figure P7.33 | Figure for Problem 7.33.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-22/a977c150-564c-4440-aae2-1d10e49c4454/e364e8db2684e3161cca7c0b3967ab5751800bd80661225a646fe784daacc12f.jpg)



Figure P7.34 | Figure for Problem 7.34.


7.30 A silicon $\mathfrak { p } ^ { + } \mathfrak { n }$ junction has doping concentrations of $N _ { a } = 2 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } =$ $2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The cross-sectional area is $1 0 ^ { - 5 }$ cm2. Calculate (a) $V _ { b i }$ and (b) the junction capacitance at $( i ) \ V _ { R } = 1 \ : \mathrm { V } , ( i i ) \ V _ { R } = 3 \ : \mathrm { V } ,$ and (iii) $V _ { R } = 5 \mathrm { V } . ( c )$ Plot $1 / C ^ { 2 }$ versus $V _ { R }$ and show that the slope can be used to fi nd $N _ { d }$ and the intercept at the voltage axis yields $V _ { b i }$ 

7.31 The total junction capacitance of a GaAs pn junction at $T = 3 0 0 \mathrm { K }$ is found to be 1.10 pF at $V _ { R } = 1 \mathrm { V } .$ The doping concentration in one region is measured and found to be $8 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ , and the built-in potential is found to be $V _ { b i } = 1 . 2 0 \ : \mathrm { V } .$ Determine (a) the doping in the other region of the pn junction and (b) the cross-sectional area. (c) The reverse-biased voltage is changed and the capacitance is found to be 0.80 pF. What is the value of $V _ { R } ?$ 

7.32 Examine how the capacitance $C ^ { \prime }$ and the function $( 1 / C ^ { \prime } ) ^ { 2 }$ vary with reverse-biased voltage $V _ { R }$ as the doping concentrations change. In particular, consider these plots versus $N _ { a }$ for $N _ { a } \geq 1 0 0 N _ { d }$ and versus $N _ { d }$ for $N _ { d } \geq 1 0 0 N _ { a } .$ . 

*7.33 A pn junction has the doping profi le shown in Figure P7.33. Assume that $x _ { n } > x _ { 0 }$ for all reverse-biased voltages. (a) What is the built-in potential across the junction? (b) For the abrupt junction approximation, sketch the charge density through the junction. (c) Derive the expression for the electric fi eld through the space charge region. 

*7.34 A silicon PIN junction has the doping profi le shown in Figure P7.34. The $^ { 6 6 } \mathrm { T } ^ { 5 }$ corresponds to an ideal intrinsic region in which there is no impurity doping concentration. A reverse-biased voltage is applied to the PIN junction so that the total depletion width extends from 2 m to 2 m. (a) Using Poisson’s equation, calculate the magnitude of the electric fi eld at $x = 0 . ( b )$ Sketch the electric fi eld through the PIN junction. (c) Calculate the reverse-biased voltage that must be applied. 

# Section 7.4 Junction Breakdown

7.35 Consider a silicon $\mathfrak { n } ^ { + } \mathfrak { p }$ junction diode. The critical electric fi eld for breakdown in silicon is approximately $\mathrm { E } _ { c r i t } = 4 \times 1 0 ^ { 5 } \mathrm { V / c m }$ . Determine the maximum p-type doping concentration such that the breakdown voltage is $\mathrm { ( } a ) 4 0 \mathrm { V }$ and (b) 20 V. 

7.36 Design an abrupt silicon $\mathfrak { n } ^ { + } \mathfrak { p }$ junction diode that has a reverse breakdown voltage of 80 V. 

7.37 (a) The n-type doping concentration in an abrupt pn GaAs junction diode is $N _ { d } =$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Determine the breakdown voltage. (b) Repeat part (a) for $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ 

7.38 (a) A symmetrically doped silicon pn junction diode has doping concentrations of $N _ { a } = N _ { d } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Assuming the critical electric fi eld is $\mathrm { E } _ { c r i t } = 4 \times 1 0 ^ { 5 }$ V/cm, determine the breakdown voltage. (b) Repeat part (a) if the doping concentrations are $N _ { a } = N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

7.39 An abrupt silicon $\mathfrak { p } ^ { + } \mathfrak { n }$ junction has an n-region doping concentration of $N _ { d } = 5 \times$ $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . What must be the minimum n-region width such that avalanche break down occurs before the depletion region reaches an ohmic contact (punchthrough)? 

7.40 A silicon pn junction diode is doped with $N _ { a } = N _ { d } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ . Zener breakdown occurs when the peak electric fi eld reaches 106 V/cm. Determine the reverse-biased breakdown voltage. 

7.41 A diode will very often have the doping profi le shown in Figure P7.29, which is known as an $\mathfrak { n } ^ { + } \mathfrak { p p } ^ { + }$ diode. Under reverse bias, the depletion region must remain within the p region to avoid premature breakdown. Assume the p-region doping is $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Determine the reverse-biased voltage such that the depletion region remains within the p region and does not reach breakdown if the p-region width is (a) $7 5 \mu \mathrm { m }$ and (b) 150 m. For each case, state whether the maximum depletion width or the breakdown voltage is reached fi rst. 

7.42 Consider a silicon pn junction at $T = 3 0 0$ K whose doping profi le varies linearly from $N _ { a } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 } \mathrm { t o } N _ { d } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ over a distance of 2 m. Estimate the breakdown voltage. 

# Section 7.5 Nonuniformly Doped Junctions

7.43 Consider a linearly graded junction. (a) Starting with Equation (7.62), derive the expression for the electric fi eld given in Equation (7.64). (b) Derive the expression for the potential through the space charge region given by Equation (7.66). 

7.44 The built-in potential barrier of a linearly graded silicon pn junction at $T = 3 0 0 \mathrm { K }$ is $V _ { b i } = 0 . 7 0 { \mathrm { V } } .$ The junction capacitance measured at $V _ { R } = 3 . 5 \mathrm { V } \mathrm { i s } C ^ { \prime } = 7 . 2 \times 1 0 ^ { - 9 }$ F/cm2. Find the gradient, a, of the net impurity concentration. 

# Summary and Review

7.45 (a) A one-sided silicon np junction at $T = 3 0 0 \mathrm { K }$ is doped at $N _ { d } = 3 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ Design the junction such that $C _ { j } = 0 . 4 5$ pF at $V _ { R } = 5 \mathrm { V } .$ (b) Calculate the junction capacitance at (i) $V _ { R } = 2 . 5 \ : \mathrm { V }$ and (ii) $V _ { R } = 0 \mathrm { V } .$ 

7.46 A one-sided pn junction with a cross-sectional area of $1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ has a measured builtin potential of $V _ { b i } = 0 . 8 \mathrm { V } \mathrm { a t } T = 3 0 0 \mathrm { K }$ . A plot of $( 1 / C _ { j } ) ^ { 2 }$ versus $V _ { R }$ is linear for $V _ { R } <$ 1 V and is essentially constant for $V _ { R } > 1 \mathrm { V } .$ The capacitance is $C _ { j } = 0 . 0 8 2$ pF at ${ \cal V } _ { \cal R } =$ 1 V. Determine the doping concentrations on either side of the metallurgical junction that will produce this capacitance characteristic. 

*7.47 Silicon, at $T = 3 0 0 \mathrm { K } ,$ is doped at $N _ { d 1 } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ for $x < 0$ and $N _ { d 2 } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ for $x > 0$ to form an n  n step junction. (a) Sketch the energy-band diagram. (b) Derive an expression for $V _ { b i \bullet } \left( c \right)$ Sketch the charge density, electric fi eld, and potential through the junction. (d) Explain where the charge density came from and is located. 

*7.48 A diffused silicon pn junction has a linearly graded junction on the p side with $a =$ $2 \times 1 0 ^ { 1 9 } \mathrm { c m } ^ { - 4 }$ , and a uniform doping of $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ on the n side. (a) If the depletion width on the p side is $0 . 7 \mu \mathrm { m }$ at zero bias, fi nd the total depletion width, built-in potential, and maximum electric fi eld at zero bias. (b) Plot the potential function through the junction. 

# READING LIST



1. Dimitrijev, S. Principles of Semiconductor Devices. New York: Oxford University Press, 2006. 





2. Kano, K. Semiconductor Devices. Upper Saddle River, NJ: Prentice Hall, 1998. 





*3. Li, S. S. Semiconductor Physical Electronics. New York: Plenum Press, 1993. 





4. Muller, R. S., and T. I. Kamins. Device Electronics for Integrated Circuits, 2nd ed. New York: John Wiley and Sons, 1986. 





5. Navon, D. H. Semiconductor Microdevices and Materials. New York: Holt, Rinehart & Winston, 1986. 





6. Neudeck, G. W. The PN Junction Diode. Vol. 2 of the Modular Series on Solid State Devices, 2nd ed. Reading, MA: Addison-Wesley, 1989. 





*7. Ng, K. K. Complete Guide to Semiconductor Devices. New York: McGraw-Hill, 1995. 





8. Pierret, R. F. Semiconductor Device Fundamentals. Reading, MA: Addison-Wesley, 1996. 





*9. Roulston, D. J. An Introduction to the Physics of Semiconductor Devices. New York: Oxford University Press, 1999. 





10. Shur, M. Introduction to Electronic Devices. New York: John Wiley and Sons, 1996. 





*11. Shur, M. Physics of Semiconductor Devices. Englewood Cliffs, NJ: Prentice Hall, 1990. 





12. Singh, J. Semiconductor Devices: Basic Principles. New York: John Wiley and Sons, 2001. 





13. Streetman, B. G., and S. K. Banerjee. Solid State Electronic Devices, 6th ed. Upper Saddle River, NJ: Pearson Prentice Hall, 2006. 





14. Sze, S. M., and K. K. Ng. Physics of Semiconductor Devices, 3rd ed. Hoboken, NJ: John Wiley and Sons, 2007. 





15. Sze, S. M. Semiconductor Devices: Physics and Technology, 2nd ed. New York: John Wiley and Sons, 2001. 





*16. Wang, S. Fundamentals of Semiconductor Theory and Device Physics. Englewood Cliffs, NJ: Prentice Hall, 1989. 





17. Yang, E. S. Microelectronic Devices. New York: McGraw-Hill, 1988. 

