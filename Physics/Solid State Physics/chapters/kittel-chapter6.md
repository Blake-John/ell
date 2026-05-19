# 6

# Free Electron Fermi Gas

ENERGY LEVELS IN ONE DIMENSION 134 

EFFECT OF TEMPERATURE ON THE FERMI-DIRAC DISTRIBUTION 136 

FREE ELECTRON GAS IN THREE DIMENSIONS 137 

HEAT CAPACITY OF THE ELECTRON GAS 141 Experimental heat capacity of metals 145 Heavy fermions 147 

ELECTRICAL CONDUCTIVITY AND OHM’S LAW 147 Experimental electrical resistivity of metals 148 Umklapp scattering 151 

MOTION IN MAGNETIC FIELDS 152 Hall effect 153 

THERMAL CONDUCTIVITY OF METALS 156 Ratio of thermal to electrical conductivity 156 

PROBLEMS 157 

1. Kinetic energy of electron gas 157 

2. Pressure and bulk modulus of an electron gas 157 

3. Chemical potential in two dimensions 157 

4. Fermi gases in astrophysics 157 

5. Liquid $\mathbf { \bar { H } e ^ { 3 } }$ 158 

6. Frequency dependence of the electrical conductivity 158 

7. Dynamic magnetoconductivity tensor for free electrons 158 

8. Cohesive energy of free electron Fermi gas 159 

9. Static magnetoconductivity tensor 159 

10. Maximum surface resistance 159 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/92e11021a8adc0da5c198edd7d22285600c35ca4da07c1a1fde06646aff98cf7.jpg)



Figure 1 Schematic model of a crystal of sodium metal. The atomic cores are $\mathrm { N a ^ { + } }$ ions: they are immersed in a sea of conduction electrons. The conduction electrons are derived from the 3s valence electrons of the free atoms. The atomic cores contain 10 electrons in the configuration $1 s ^ { 2 } 2 s ^ { 2 } 2 p ^ { 6 }$ . In an alkali metal the atomic cores occupy a relatively small part (-15 percent) of the total volume of the crystal, but in a noble metal (Cu, Ag, Au) the atomic cores are relatively larger and may be in contact with each other. The common crystal structure at room temperature is bcc for the alkali metals and fcc for the noble metals.


# In a theory which has given results like these, there must certainly be a great deal of truth.

H. A. Lorentz 

We can understand many physical properties of metals, and not only of the simple metals, in terms of the free electron model. According to this model, the valence electrons of the constituent atoms become conduction electrons and move about freely through the volume of the metal. Even in metals for which the free electron model works best, the charge distribution of the conduction electrons reflects the strong electrostatic potential of the ion cores. The utility of the free electron model is greatest for properties that depend essentially on the kinetic properties of the conduction electrons. The interaction of the conduction electrons with the ions of the lattice is treated in the next chapter. 

The simplest metals are the alkali metals—lithium, sodium, potassium, cesium, and rubidium. In a free atom of sodium the valence electron is in a 3s state; in the metal this electron becomes a conduction electron in the 3s conduction band. 

A monovalent crystal which contains N atoms will have N conduction electrons and N positive ion cores. The Na- ion core contains 10 electrons that occupy the 1s, 2s, and 2p shells of the free ion, with a spatial distribution that is essentially the same when in the metal as in the free ion. The ion cores fill only about 15 percent of the volume of a sodium crystal, as in Fig. 1. The radius of the free Na- ion is 0.98 Å, whereas one-half of the nearest-neighbor distance of the metal is 1.83 Å. 

The interpretation of metallic properties in terms of the motion of free electrons was developed long before the invention of quantum mechanics. The classical theory had several conspicuous successes, notably the derivation of the form of Ohm’s law and the relation between the electrical and thermal conductivity. The classical theory fails to explain the heat capacity and the magnetic susceptibility of the conduction electrons. (These are not failures of the free electron model, but failures of the classical Maxwell distribution function.) 

There is a further difficulty with the classical model. From many types of experiments it is clear that a conduction electron in a metal can move freely in a straight path over many atomic distances, undeflected by collisions with other conduction electrons or by collisions with the atom cores. In a very pure specimen at low temperatures, the mean free path may be as long as $1 0 ^ { 8 }$ interatomic spacings (more than 1 cm). 

Why is condensed matter so transparent to conduction electrons? The answer to the question contains two parts: (a) A conduction electron is not deflected by ion cores arranged on a periodic lattice because matter waves can propagate freely in a periodic structure, as a consequence of the mathematics treated in the following chapter. (b) A conduction electron is scattered only infrequently by other conduction electrons. This property is a consequence of the Pauli exclusion principle. By a free electron Fermi gas, we shall mean a gas of free electrons subject to the Pauli principle. 

# ENERGY LEVELS IN ONE DIMENSION

Consider a free electron gas in one dimension, taking account of quantum theory and of the Pauli principle. An electron of mass m is confined to a length L by infinite barriers (Fig. 2). The wavefunction $\psi _ { n } ( x )$ of the electron is a solution of the Schrödinger equation ${ \mathcal { H } } \psi = \epsilon \psi ;$ with the neglect of potential energy we have ${ \mathcal { H } } = p ^ { 2 } / 2 m$ where, $p$ is the momentum. In quantum theory p may be represented by the operator i d/dx, so that-

$$
\mathcal {H} \psi_ {n} = - \frac {\hbar^ {2}}{2 m} \frac {d ^ {2} \psi_ {n}}{d x ^ {2}} = \epsilon_ {n} \psi_ {n}, \tag {1}
$$

where $\epsilon _ { n }$ is the energy of the electron in the orbital. 

We use the term orbital to denote a solution of the wave equation for a system of only one electron. The term allows us to distinguish between an exact quantum state of the wave equation of a system of N interacting electrons and an approximate quantum state which we construct by assigning the N electrons to N different orbitals, where each orbital is a solution of a wave equation for one electron. The orbital model is exact only if there are no interactions between electrons. 

The boundary conditions are $\psi _ { n } ( 0 ) = 0 ; \psi _ { n } ( L ) = 0$ , as imposed by the infinite potential energy barriers. They are satisfied if the wavefunction is sinelike with an integral number n of half-wavelengths between 0 and L: 

$$
\psi_ {n} = A \sin \left(\frac {2 \pi}{\lambda_ {n}} x\right); \quad \frac {1}{2} n \lambda_ {n} = L, \tag {2}
$$

where A is a constant. We see that (2) is a solution of (1), because 

$$
\frac {d \psi_ {n}}{d x} = A \left(\frac {n \pi}{L}\right) \cos \left(\frac {n \pi}{L} x\right); \quad \frac {d ^ {2} \psi_ {n}}{d x ^ {2}} = - A \left(\frac {n \pi}{L}\right) ^ {2} \sin \left(\frac {n \pi}{L} x\right),
$$

whence the energy $\epsilon _ { n }$ is given by 

$$
\epsilon_ {n} = \frac {\hbar^ {2}}{2 m} \left(\frac {n \pi}{L}\right) ^ {2}. \tag {3}
$$

We want to accommodate N electrons on the line. According to the Pauli exclusion principle, no two electrons can have all their quantum numbers identical. That is, each orbital can be occupied by at most one electron. This applies to electrons in atoms, molecules, or solids. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/8e9bb26609a20a891e62f40905d4abdee6fcfc22258a2110bbc19bf8e1c793c1.jpg)



Figure 2 First three energy levels and wavefunctions of a free electron of mass m confined to a line of length L. The energy levels are labeled according to the quantum number n which gives the number of half-wavelengths in the wavefunction. The wavelengths are indicated on the wavefunctions. The energy $\epsilon _ { n }$ of the level of quantum number n is equal to $( h ^ { 2 } / 2 m ) ( n / 2 L ) ^ { 2 }$ .


In a linear solid the quantum numbers of a conduction electron orbital are n and $m _ { s } ,$ , where n is any positive integer and the magnetic quantum number $m _ { s } = \pm \frac { 1 } { 2 }$ , according to spin orientation. A pair of orbitals labeled by the quantum number n can accommodate two electrons, one with spin up and one with spin down. 

If there are six electrons, then in the ground state of the system the filled orbitals are those given in the table: 

<table><tr><td>n</td><td>ms</td><td>Electronoccupancy</td><td>n</td><td>ms</td><td>Electronoccupancy</td></tr><tr><td>1</td><td>↑</td><td>1</td><td>3</td><td>↑</td><td>1</td></tr><tr><td>1</td><td>↓</td><td>1</td><td>3</td><td>↓</td><td>1</td></tr><tr><td>2</td><td>↑</td><td>1</td><td>4</td><td>↑</td><td>0</td></tr><tr><td>2</td><td>↓</td><td>1</td><td>4</td><td>↓</td><td>0</td></tr></table>

More than one orbital may have the same energy. The number of orbitals with the same energy is called the degeneracy. 

Let $n _ { F }$ denote the topmost filled energy level, where we start filling the levels from the bottom $( n = 1 )$ and continue filling higher levels with electrons until all N electrons are accommodated. It is convenient to suppose that N is an even number. The condition $2 n _ { F } = N$ determines $n _ { F } .$ , the value of n for the uppermost filled level. 

The Fermi energy $\epsilon _ { F }$ is defined as the energy of the topmost filled level in the ground state of the N electron system. By (3) with $n = n _ { F }$ we have in one dimension: 

$$
\epsilon_ {F} = \frac {\hbar^ {2}}{2 m} \left(\frac {n _ {F} \pi}{L}\right) ^ {2} = \frac {\hbar^ {2}}{2 m} \left(\frac {N \pi}{2 L}\right) ^ {2}. \tag {4}
$$

# EFFECT OF TEMPERATURE ON THE FERMI-DIRAC DISTRIBUTION

The ground state is the state of the N electron system at absolute zero. What happens as the temperature is increased? This is a standard problem in elementary statistical mechanics, and the solution is given by the Fermi-Dirac distribution function (Appendix D and TP, Chapter 7). 

The kinetic energy of the electron gas increases as the temperature is increased: some energy levels are occupied which were vacant at absolute zero, and some levels are vacant which were occupied at absolute zero (Fig. 3). The Fermi-Dirac distribution gives the probability that an orbital at energy  will be occupied in an ideal electron gas in thermal equilibrium: 

$$
\boxed {f (\epsilon) = \frac {1}{\exp [ (\epsilon - \mu) / k _ {B} T ] + 1}.} \tag {5}
$$

The quantity $\mu$ is a function of the temperature; $\mu$ is to be chosen for the particular problem in such a way that the total number of particles in the system comes out correctly—that is, equal to N. At absolute zero $\mu = \epsilon _ { F } ,$ because in the limit $T \to 0$ the function $f ( \epsilon )$ changes discontinuously from the value 1 (filled) to the value 0 (empty) at $\epsilon = \epsilon _ { F } = \mu$ . At all temperatures $f ( \epsilon )$ is equal to $\frac { 1 } { 2 }$ when $\epsilon = \mu$ , for then the denominator of (5) has the value 2. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/1c51873514f70cb7975189bdf17e88a2c2850ed5301776aa1307f76005a0eddc.jpg)



Figure 3 Fermi-Dirac distribution function (5) at the various labelled temperatures, for $T _ { F } \equiv \epsilon _ { F } / k _ { B } = 5 0 , 0 0 0 \mathrm { \ K } .$ . The results apply to a gas in three dimensions. The total number of particles is constant, independent of temperature. The chemical potential $\mu$ at each temperature may be read off the graph as the energy at which $f = 0 . 5$ .


The quantity  is the chemical potential (TP, Chapter 5), and we see that at absolute zero the chemical potential is equal to the Fermi energy, defined as the energy of the topmost filled orbital at absolute zero. 

The high energy tail of the distribution is that part for which $\epsilon - \mu \gg k _ { B } T ;$ ; here the exponential term is dominant in the denominator of (5), so that $f ( \epsilon ) \cong \exp [ ( \mu - \epsilon ) / k _ { B } T ]$ . This limit is called the Boltzmann or Maxwell distribution. 

# FREE ELECTRON GAS IN THREE DIMENSIONS

The free-particle Schrödinger equation in three dimensions is 

$$
- \frac {\hbar^ {2}}{2 m} \left(\frac {\partial^ {2}}{\partial x ^ {2}} + \frac {\partial^ {2}}{\partial y ^ {2}} + \frac {\partial^ {2}}{\partial z ^ {2}}\right) \psi_ {\mathbf {k}} (\mathrm{r}) = \epsilon_ {\mathbf {k}} \psi_ {\mathbf {k}} (\mathbf {r}). \tag {6}
$$

If the electrons are confined to a cube of edge L, the wavefunction is the standing wave 

$$
\psi_ {n} (\mathbf {r}) = A \sin \left(\pi n _ {x} x / L\right) \sin \left(\pi n _ {y} y / L\right) \sin \left(\pi n _ {z} z / L\right), \tag {7}
$$

where $n _ { x } , n _ { y } , n _ { z }$ are positive integers. The origin is at one corner of the cube. 

It is convenient to introduce wavefunctions that satisfy periodic boundary conditions, as we did for phonons in Chapter 5. We now require the wavefunctions to be periodic in x, y, z with period L. Thus 

$$
\psi (x + L, y, z) = \psi (x, y, z), \tag {8}
$$

and similarly for the y and z coordinates. Wavefunctions satisfying the freeparticle Schrödinger equation and the periodicity condition are of the form of a traveling plane wave: 

$$
\boxed {\psi_ {\mathbf {k}} (\mathbf {r}) = \exp (i \mathbf {k} \cdot \mathbf {r}),} \tag {9}
$$

provided that the components of the wavevector k satisfy 

$$
k _ {x} = 0; \quad \pm \frac {2 \pi}{L}; \quad \pm \frac {4 \pi}{L}; \dots , \tag {10}
$$

and similarly for $k _ { y }$ and $k _ { z }$ . 

Any component of k of the form 2n/L will satisfy the periodicity condition over a length L, where n is a positive or negative integer. The components of $k$ are the quantum numbers of the problem, along with the quantum number $m _ { s }$ for the spin direction. We confirm that these values of $k _ { x }$ satisfy (8), for 

$$
\begin{array}{l} \exp \left[ i k _ {x} (x + L) \right] = \exp \left[ i 2 n \pi (x + L) / L \right] \\ = \exp (i 2 n \pi x / L) \exp (i 2 n \pi) = \exp (i 2 n \pi x / L) = \exp (i k _ {x} x). \tag {11} \\ \end{array}
$$

On substituting (9) in (6) we have the energy $\epsilon _ { \mathbf { k } }$ of the orbital with wavevector k: 

$$
\epsilon_ {\mathbf {k}} = \frac {\hbar^ {2}}{2 m} k ^ {2} = \frac {\hbar^ {2}}{2 m} \left(k _ {x} ^ {2} + k _ {y} ^ {2} + k _ {z} ^ {2}\right). \tag {12}
$$

The magnitude k of the wavevector is related to the wavelength  by $k = 2 \pi / \lambda$ 

The linear momentum p may be represented in quantum mechanics by the operator $\mathbf { p } = - i \hbar \nabla$ , whence for the orbital (9) 

$$
\mathbf {p} \psi_ {\mathbf {k}} (\mathrm{r}) = - i \hbar \nabla \psi_ {\mathbf {k}} (\mathbf {r}) = \hbar \mathbf {k} \psi_ {\mathbf {k}} (\mathbf {r}), \tag {13}
$$

so that the plane wave $\psi _ { \mathbf { k } }$ is an eigenfunction of the linear momentum with the eigenvalue . The particle velocity in the orbital k is given by-k $\mathbf { v } = \hbar \mathbf { k } / m$ . 

In the ground state of a system of N free electrons, the occupied orbitals may be represented as points inside a sphere in k space. The energy at the surface of the sphere is the Fermi energy; the wavevectors at the Fermi surface have a magnitude $k _ { F }$ such that (Fig. 4): 

$$
\epsilon_ {F} = \frac {\hbar^ {2}}{2 m} k _ {F} ^ {2}. \tag {14}
$$

From (10) we see that there is one allowed wavevector—that is, one distinct triplet of quantum numbers $k _ { x } , k _ { y } , k _ { z }$ —for the volume element $( 2 \pi / L ) ^ { 3 }$ of k space. Thus in the sphere of volume the total number of orbitals is4k3 /3 

$$
2 \cdot \frac {4 \pi k _ {F} ^ {3} / 3}{(2 \pi / L) ^ {3}} = \frac {V}{3 \pi^ {2}} k _ {F} ^ {3} = N, \tag {15}
$$

where the factor 2 on the left comes from the two allowed values of the spin quantum number for each allowed value of k. Then (15) gives 

$$
k _ {F} = \left(\frac {3 \pi^ {2} N}{V}\right) ^ {1 / 3}, \tag {16}
$$

which depends only on the particle concentration. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/47dff1bbdd7baffcb111ef649a39417ec8352bcd180f4b0e4265a3bda0babd79.jpg)



Figure 4 In the ground state of a system of N free electrons the occupied orbitals of the system fill a sphere of radius $k _ { F } ,$ where $\epsilon _ { F } = \hbar ^ { 2 } k _ { F } ^ { 2 } / 2 m$ is the energy of an electron having a wavevector $k _ { F }$ .



Table 1 Calculated free electron Fermi surface parameters for metals at room temperature ^798a84



( E xcept fo r N a, K , Rb , C s at 5 K and Li at 78 K )


<table><tr><td>Valency</td><td>Metal</td><td>Electron concentration, in cm-3</td><td>Radiusa parameter rn</td><td>Fermi wavevector, in cm-1</td><td>Fermi velocity, in cm s-1</td><td>Fermi energy, in eV</td><td>Fermi temperature TF ≡ εF/kB, in deg K</td></tr><tr><td rowspan="8">1</td><td>Li</td><td>4.70 × 1022</td><td>3.25</td><td>1.11 × 108</td><td>1.29 × 108</td><td>4.72</td><td>5.48 × 104</td></tr><tr><td>Na</td><td>2.65</td><td>3.93</td><td>0.92</td><td>1.07</td><td>3.23</td><td>3.75</td></tr><tr><td>K</td><td>1.40</td><td>4.86</td><td>0.75</td><td>0.86</td><td>2.12</td><td>2.46</td></tr><tr><td>Rb</td><td>1.15</td><td>5.20</td><td>0.70</td><td>0.81</td><td>1.85</td><td>2.15</td></tr><tr><td>Cs</td><td>0.91</td><td>5.63</td><td>0.64</td><td>0.75</td><td>1.58</td><td>1.83</td></tr><tr><td>Cu</td><td>8.45</td><td>2.67</td><td>1.36</td><td>1.57</td><td>7.00</td><td>8.12</td></tr><tr><td>Ag</td><td>5.85</td><td>3.02</td><td>1.20</td><td>1.39</td><td>5.48</td><td>6.36</td></tr><tr><td>Au</td><td>5.90</td><td>3.01</td><td>1.20</td><td>1.39</td><td>5.51</td><td>6.39</td></tr><tr><td rowspan="7">2</td><td>Be</td><td>24.2</td><td>1.88</td><td>1.93</td><td>2.23</td><td>14.14</td><td>16.41</td></tr><tr><td>Mg</td><td>8.60</td><td>2.65</td><td>1.37</td><td>1.58</td><td>7.13</td><td>8.27</td></tr><tr><td>Ca</td><td>4.60</td><td>3.27</td><td>1.11</td><td>1.28</td><td>4.68</td><td>5.43</td></tr><tr><td>Sr</td><td>3.56</td><td>3.56</td><td>1.02</td><td>1.18</td><td>3.95</td><td>4.58</td></tr><tr><td>Ba</td><td>3.20</td><td>3.69</td><td>0.98</td><td>1.13</td><td>3.65</td><td>4.24</td></tr><tr><td>Zn</td><td>13.10</td><td>2.31</td><td>1.57</td><td>1.82</td><td>9.39</td><td>10.90</td></tr><tr><td>Cd</td><td>9.28</td><td>2.59</td><td>1.40</td><td>1.62</td><td>7.46</td><td>8.66</td></tr><tr><td rowspan="3">3</td><td>Al</td><td>18.06</td><td>2.07</td><td>1.75</td><td>2.02</td><td>11.63</td><td>13.49</td></tr><tr><td>Ga</td><td>15.30</td><td>2.19</td><td>1.65</td><td>1.91</td><td>10.35</td><td>12.01</td></tr><tr><td>In</td><td>11.49</td><td>2.41</td><td>1.50</td><td>1.74</td><td>8.60</td><td>9.98</td></tr><tr><td rowspan="2">4</td><td>Pb</td><td>13.20</td><td>2.30</td><td>1.57</td><td>1.82</td><td>9.37</td><td>10.87</td></tr><tr><td>Sn(w)</td><td>14.48</td><td>2.23</td><td>1.62</td><td>1.88</td><td>10.03</td><td>11.64</td></tr></table>


aThe dimensionles s radius parameter is defined as $r _ { n } = r _ { 0 } / a _ { H } ,$ where $a _ { H }$ is the first B ohr radius and $r _ { 0 } \mathrm { i }$ is the radius of a sphe re that contains one ele ctron . 


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/5d00fef564c1facf61a0c3543bb3dc285435acc1b54086ccb29f6b75ebdbaac7.jpg)



Figure 5 Density of single-particle states as a function of energy, for a free electron gas in three dimensions. The dashed curve represents the density $f ( \epsilon , T ) D ( \epsilon )$ of filled orbitals at a finite temperature, but such that $k _ { B } T$ is small in comparison with $\epsilon _ { F } .$ The shaded area represents the filled orbitals at absolute zero. The average energy is increased when the temperature is increased from 0 to T, for electrons are thermally excited from region 1 to region 2.


Using (14) and (16), 

$$
\boxed {\epsilon_ {F} = \frac {\hbar^ {2}}{2 m} \left(\frac {3 \pi^ {2} N}{V}\right) ^ {2 / 3}.} \tag {17}
$$

This relates the Fermi energy to the electron concentration N/V. The electron velocity $v _ { F }$ at the Fermi surface is 

$$
v _ {F} = \left(\frac {\hbar k _ {F}}{m}\right) = \left(\frac {\hbar}{m}\right) \left(\frac {3 \pi^ {2} N}{V}\right) ^ {1 / 3}. \tag {18}
$$

Calculated values of $k _ { F } , v _ { F } ,$ and $\epsilon _ { F }$ are given in Table 1 for selected metals; also given are values of the quantity $T _ { F }$ which is defined as $\epsilon _ { F } / k _ { B } .$ . (The quantity $T _ { F }$ has nothing to do with the temperature of the electron gas!) 

We now find an expression for the number of orbitals per unit energy range, $D ( \epsilon )$ , called the density of states.1 We use (17) to obtain the total number of orbitals of energy $\leq \epsilon $ : 

$$
N = \frac {V}{3 \pi^ {2}} \left(\frac {2 m \epsilon}{\hbar^ {2}}\right) ^ {3 / 2}, \tag {19}
$$

so that the density of states (Fig. 5) is 

$$
\boxed {D (\epsilon) \equiv \frac {d N}{d \epsilon} = \frac {V}{2 \pi^ {2}} \cdot \left(\frac {2 m}{\hbar^ {2}}\right) ^ {3 / 2} \cdot \epsilon^ {1 / 2}.} \tag {20}
$$

1 Strictly, $D ( \epsilon )$ is the density of one-particle states, or density of orbitals. 

This result may be expressed more simply by comparing (19) and (20) to obtain at  

$$
D (\epsilon) \equiv \frac {d N}{d \epsilon} = \frac {3 N}{2 \epsilon}. \tag {21}
$$

Within a factor of the order of unity, the number of orbitals per unit energy range at the Fermi energy is the total number of conduction electrons divided by the Fermi energy, just as we would expect. 

# HEAT CAPACITY OF THE ELECTRON GAS

The question that caused the greatest difficulty in the early development of the electron theory of metals concerns the heat capacity of the conduction electrons. Classical statistical mechanics predicts that a free particle should have a heat capacity of $\mathit { \Pi } _ { \overline { { 2 } } } ^ { 3 } k _ { B } .$ , where $k _ { B }$ is the Boltzmann constant. If N atoms each give one valence electron to the electron gas, and the electrons are freely mobile, then the electronic contribution to the heat capacity should be ${ \scriptstyle { \frac { 3 } { 2 } } } N k _ { B }$ , just as for the atoms of a monatomic gas. But the observed electronic contribution at room temperature is usually less than 0.01 of this value. 

This important discrepancy distracted the early workers, such as Lorentz: How can the electrons participate in electrical conduction processes as if they were mobile, while not contributing to the heat capacity? The question was answered only upon the discovery of the Pauli exclusion principle and the Fermi distribution function. Fermi found the correct result and he wrote, “One recognizes that the specific heat vanishes at absolute zero and that at low temperatures it is proportional to the absolute temperature.” 

When we heat the specimen from absolute zero, not every electron gains an energy ${ \sim } k _ { B } T$ as expected classically, but only those electrons in orbitals within an energy range $k _ { B } T$ of the Fermi level are excited thermally, as in Fig. 5. This gives an immediate qualitative solution to the problem of the heat capacity of the conduction electron gas. If N is the total number of electrons, only a fraction of the order of $T / T _ { F }$ can be excited thermally at temperature T, because only these lie within an energy range of the order of $k _ { B } T$ of the top of the energy distribution. 

Each of these $N T / T _ { F }$ electrons has a thermal energy of the order of $k _ { B } T$ The total electronic thermal kinetic energy U is of the order of 

$$
U _ {e l} \approx (N T / T _ {F}) k _ {B} T. \tag {22}
$$

The electronic heat capacity is given by 

$$
C _ {e l} = \partial U / \partial T \approx N k _ {B} (T / T _ {F}) \tag {23}
$$

and is directly proportional to $T ,$ in agreement with the experimental results discussed in the following section. At room temperature $C _ { e l }$ is smaller than the classical value ${ \scriptstyle { \frac { 3 } { 2 } } } N k _ { B }$ by a factor of the order of 0.01 or less, for $T _ { F } \sim 5 \times 1 0 ^ { 4 } \ : \mathrm { K }$ . 

We now derive a quantitative expression for the electronic heat capacity valid at low temperatures $k _ { B } T \ll \epsilon _ { F }$ . The increase $\Delta U \equiv U ( T ) - U ( 0 )$ in the total energy (Fig. 5) of a system of N electrons when heated from 0 to T is 

$$
\Delta U = \int_ {0} ^ {\infty} d \epsilon \epsilon D (\epsilon) f (\epsilon) - \int_ {0} ^ {\epsilon_ {F}} d \epsilon \epsilon D (\epsilon). \tag {24}
$$

Here $f ( \epsilon )$ is the Fermi-Dirac function (5): 

$$
\boxed {f (\epsilon , T, \mu) = \frac {1}{\exp [ (\epsilon - \mu) / k _ {\mathrm{B}} T + 1 ]}} \tag {24a}
$$

and $D ( \epsilon )$ is the number of orbitals per unit energy range. We multiply the identity 

$$
N = \int_ {0} ^ {\infty} d \epsilon   D (\epsilon) f (\epsilon) = \int_ {0} ^ {\epsilon_ {F}} d \epsilon   D (\epsilon) \tag {25}
$$

by $\epsilon _ { F }$ to obtain 

$$
\left(\int_ {0} ^ {\epsilon_ {F}} + \int_ {\epsilon_ {F}} ^ {\infty}\right) d \epsilon \epsilon_ {F} f (\epsilon) D (\epsilon) = \int_ {0} ^ {\epsilon_ {F}} d \epsilon \epsilon_ {F} D (\epsilon). \tag {26}
$$

We use (26) to rewrite (24) as 

$$
\Delta U = \int_ {\epsilon_ {F}} ^ {\infty} d \epsilon (\epsilon - \epsilon_ {F}) f (\epsilon) D (\epsilon) + \int_ {0} ^ {\epsilon_ {F}} d \epsilon (\epsilon_ {F} - \epsilon) [ 1 - f (\epsilon) ] D (\epsilon). \tag {27}
$$

The first integral on the right-hand side of (27) gives the energy needed to take electrons from $\epsilon _ { F }$ to the orbitals of energy $\epsilon > \epsilon _ { F } .$ , and the second integral gives the energy needed to bring the electrons to $\epsilon _ { F }$ from orbitals below $\epsilon _ { F }$ . Both contributions to the energy are positive. 

The product $f ( \epsilon ) D ( \epsilon ) d \epsilon$ in the first integral of (27) is the number of electrons elevated to orbitals in the energy range d at an energy . The factor $[ 1 - f ( \epsilon ) ]$ in the second integral is the probability that an electron has been removed from an orbital . The function $\Delta U$ is plotted in Fig. 6. 

The heat capacity of the electron gas is found on differentiating $\Delta U$ with respect to T. The only temperature-dependent term in (27) is $f ( \epsilon )$ , whence we can group terms to obtain 

$$
C _ {e l} = \frac {d U}{d T} = \int_ {0} ^ {\infty} d \epsilon (\epsilon - \epsilon_ {F}) \frac {d f}{d T} D (\epsilon). \tag {28}
$$

At the temperatures of interest in metals, $\tau / \epsilon _ { F } < 0 . 0 1$ , and we see from Fig. 3 that $( \epsilon - \epsilon _ { F } )$ df/dT has large positive peaks at energies near $\epsilon _ { F } .$ It is a good approximation to evaluate the density of states $D ( \epsilon )$ at $\epsilon _ { F }$ and take it outside of the integral: 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/52f8ebb35ecfb21933b5ae8870247b4da432853b3cd8738ffbdef379d6faf1fa.jpg)



Figure 6 Temperature dependence of the energy of a noninteracting fermion gas in three dimensions. The energy is plotted in normalized form as $\Delta U / N \epsilon _ { F } ,$ where N is the number of electrons. The temperature is plotted as $k _ { B } T / \epsilon _ { F }$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/dec8fcac386c5ff71c3c09bbb6bd05e85c63dc0f898486da0a3b49ead4077767.jpg)



Figure 7 Plot of the chemical potential $\mu$ versus temperature as $k _ { B } T$ for a gas of noninteracting fermions in three dimensions. For convenience in plotting, the units of  and $\mathbf { \bar { \rho } } _ { k _ { B } T }$ are $0 . 7 6 3 \epsilon _ { F }$ .


$$
C _ {e l} \cong D (\boldsymbol {\epsilon} _ {F}) \int_ {0} ^ {\infty} d \boldsymbol {\epsilon} (\boldsymbol {\epsilon} - \boldsymbol {\epsilon} _ {F}) \frac {d f}{d T}. \tag {29}
$$

Examination of the graphs in Figs. 7 and 8 of the variation of the chemical potential $\mu$ with T suggests that when $k _ { B } T \ll \epsilon _ { F }$ we ignore the temperature dependence of the chemical potential $\mu$ in the Fermi-Dirac distribution function and replace $\mu$ by the constant $\epsilon _ { F } .$ We have then, with ${ \tau \equiv k _ { B } T }$ , 


Figure 8 Variation with temperature of the chemical potential $\mu ,$ for free electron Fermi gases in one and three dimensions. In common metals $\tau / \epsilon _ { F } \simeq 0 . 0 1$ at room temperature, so that $\mu$ is closely equal to $\epsilon _ { F } .$ These curves were calculated from series expansions of the integral for the number of particles in the system.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/299c7c4410d7c834bd53aab3bd1f9dcf30255b7c2155069b930f43ed2e4683bf.jpg)


$$
\frac {d f}{d \tau} = \frac {\epsilon - \epsilon_ {F}}{\tau^ {2}} \cdot \frac {\exp [ (\epsilon - \epsilon_ {F}) / \tau ]}{\left\{\exp [ (\epsilon - \epsilon_ {F}) / \tau ] + 1 \right\} ^ {2}}. \tag {30}
$$

We set 

$$
x \equiv (\epsilon - \epsilon_ {F}) / \tau , \tag {31}
$$

and it follows from (29) and (30) that 

$$
C _ {e l} = k _ {B} ^ {2} T D \left(\epsilon_ {F}\right) \int_ {- \epsilon_ {F} / \tau} ^ {\infty} d x x ^ {2} \frac {e ^ {x}}{\left(e ^ {x} + 1\right) ^ {2}}. \tag {32}
$$

We may safely replace the lower limit by - because the factor $e ^ { x }$ in the integrand is already negligible at $x = - \epsilon _ { F } / \tau$ if we are concerned with low temperatures such that $\epsilon _ { F } / \tau \sim 1 0 0$ or more. The integral in (32) then becomes 

$$
\int_ {- \infty} ^ {\infty} d x x ^ {2} \frac {e ^ {x}}{(e ^ {x} + 1) ^ {2}} = \frac {\pi^ {2}}{3}, \tag {33}
$$

whence the heat capacity of an electron gas is 

$$
C _ {e l} = \frac {1}{3} \pi^ {2} D (\epsilon_ {F}) k _ {B} ^ {2} T. \tag {34}
$$

From (21) we have 

$$
D (\boldsymbol {\epsilon} _ {F}) = 3 N / 2 \boldsymbol {\epsilon} _ {F} = 3 N / 2 k _ {B} T _ {F} \tag {35}
$$

for a free electron gas, with $k _ { B } T _ { F } \equiv \epsilon _ { F }$ . Thus (34) becomes 

$$
C _ {e l} = \frac {1}{2} \pi^ {2} N k _ {B} T / T _ {F}. \tag {36}
$$

Recall that although $T _ { F }$ is called the Fermi temperature, it is not the electron temperature, but only a convenient reference notation. 

# Experimental Heat Capacity of Metals

At temperatures much below both the Debye temperature  and the Fermi temperature $T _ { F } ,$ the heat capacity of metals may be written as the sum of electron and phonon contributions: $\begin{array} { r } { C = \gamma T + A T ^ { 3 } } \end{array}$ , where 	 and A are constants characteristic of the material. The electronic term is linear in T and is dominant at sufficiently low temperatures. It is convenient to exhibit the experimental values of C as a plot of C/T versus $T ^ { 2 }$ : 

$$
C / T = \gamma + A T ^ {2}, \tag {37}
$$

for then the points should lie on a straight line with slope A and intercept 	. Such a plot for potassium is shown in Fig. 9. Observed values of 	, called the Sommerfeld parameter, are given in Table 2. 

The observed values of the coefficient 	 are of the expected magnitude, but often do not agree very closely with the value calculated for free electrons of mass m by use of (17) and (34). It is common practice to express the ratio of the observed to the free electron values of the electronic heat capacity as a ratio of a thermal effective mass $m _ { \mathrm { t h } }$ to the electron mass $m ,$ , where $m _ { \mathrm { t h } }$ is defined by the relation 

$$
\frac {m _ {\mathrm{th}}}{m} \equiv \frac {\gamma (\text { observed })}{\gamma (\text { free })}. \tag {38}
$$

This form arises in a natural way because $\epsilon _ { F }$ is inversely proportional to the mass of the electron, whence $\gamma \propto m$ . Values of the ratio are given in Table 2. The departure from unity involves three separate effects: 

• The interaction of the conduction electrons with the periodic potential of the rigid crystal lattice. The effective mass of an electron in this potential is called the band effective mass. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/ce2fb7389aa903edde666b918c9e2d812d9f84a1d50746bfe3e2a81f54acaf43.jpg)



Figure 9 Experimental heat capacity values for potassium, plotted as C/T versus $T ^ { 2 } .$ (After W. H. Lien and N. E. Phillips.)


<table><tr><td rowspan="3">Li1.630.7492.18</td><td rowspan="3">Be0.170.5000.34</td><td rowspan="3" colspan="10">Table 2 Experimental and free electron values of electronic heat capacity constant γ of metals(From compilations kindly furnished by N. Phillips and N. Pearlman. The thermal effective mass is defined by Eq. (38).)</td><td>B</td><td>C</td><td>N</td></tr><tr><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td></tr><tr><td rowspan="2">Na1.381.0941.26</td><td rowspan="2">Mg1.30.9921.3</td><td rowspan="2" colspan="10">Observed γ in mJ mol-1K-2.Calculated free electron γ in mJ mol-1K-2mth/m = (observed γ)/(free electron γ).</td><td rowspan="2">Al1.350.9121.48</td><td rowspan="2">Si</td><td rowspan="2">P</td></tr><tr></tr><tr><td rowspan="2">K2.081.6681.25</td><td rowspan="2">Ca2.91.5111.9</td><td rowspan="2">Sc10.7</td><td rowspan="2">Ti3.35</td><td rowspan="2">V9.26</td><td rowspan="2">Cr1.40</td><td rowspan="2">Mn(γ)9.20</td><td rowspan="2">Fe4.98</td><td rowspan="2">Co4.73</td><td rowspan="2">Ni7.02</td><td rowspan="2">Cu0.6950.5051.38</td><td rowspan="2">Zn0.640.7530.85</td><td rowspan="2">Ga0.5961.0250.58</td><td rowspan="2">Ge</td><td rowspan="2">As0.19</td></tr><tr></tr><tr><td rowspan="2">Rb2.411.9111.26</td><td rowspan="2">Sr3.61.7902.0</td><td rowspan="2">Y10.2</td><td rowspan="2">Zr2.80</td><td rowspan="2">Nb7.79</td><td rowspan="2">Mo2.0</td><td rowspan="2">Tc—</td><td rowspan="2">Ru3.3</td><td rowspan="2">Rh4.9</td><td rowspan="2">Pd9.42</td><td rowspan="2">Ag0.6460.6451.00</td><td rowspan="2">Cd0.6880.9480.73</td><td rowspan="2">In1.691.2331.37</td><td rowspan="2">Sn (w)1.781.4101.26</td><td rowspan="2">Sb0.11</td></tr><tr></tr><tr><td rowspan="2">Cs3.202.2381.43</td><td rowspan="2">Ba2.71.9371.4</td><td rowspan="2">La10.</td><td rowspan="2">Hf2.16</td><td rowspan="2">Ta5.9</td><td rowspan="2">W1.3</td><td rowspan="2">Re2.3</td><td rowspan="2">Os2.4</td><td rowspan="2">Ir3.1</td><td rowspan="2">Pt6.8</td><td rowspan="2">Au0.7290.6421.14</td><td rowspan="2">Hg(α)1.790.9521.88</td><td rowspan="2">Tl1.471.291.14</td><td rowspan="2">Pb2.981.5091.97</td><td rowspan="2">Bi0.008</td></tr><tr></tr></table>

• The interaction of the conduction electrons with phonons. An electron tends to polarize or distort the lattice in its neighborhood, so that the moving electron tries to drag nearby ions along, thereby increasing the effective mass of the electron. 

• The interaction of the conduction electrons with themselves. A moving electron causes an inertial reaction in the surrounding electron gas, thereby increasing the effective mass of the electron. 

Heavy Fermions. Several metallic compounds have been discovered that have enormous values, two or three orders of magnitude higher than usual, of the electronic heat capacity constant 	. The heavy fermion compounds include $\mathrm { U B e _ { 1 3 } , }$ $\mathrm { C e A l _ { 3 } } .$ , and $\mathrm { C e C u _ { 2 } S i _ { 2 } } .$ . It has been suggested that f electrons in these compounds may have inertial masses as high as 1000 m, because of the weak overlap of wavefunctions of f electrons on neighboring ions (see Chapter 9, “tight binding”). 

# ELECTRICAL CONDUCTIVITY AND OHM’S LAW

The momentum of a free electron is related to the wavevector by $m \mathbf { v } = \hbar \mathbf { k }$ . In an electric field E and magnetic field B the force F on an electron of charge $- e \mathrm { i } \mathrm { s } - e [ \mathbf { E } + ( 1 / c ) \mathbf { v } \times \mathbf { B } ]$ , so that Newton’s second law of motion becomes 

$$
\boxed {\mathbf {F} = m \frac {d \mathbf {v}}{d t} = \hbar \frac {d \mathbf {k}}{d t} = - e \left(\mathbf {E} + \frac {1}{c} \mathbf {v} \times \mathbf {B}\right).} \tag {39}
$$

In the absence of collisions the Fermi sphere (Fig. 10) moves in k space at a uniform rate by a constant applied electric field. We integrate (39) with $\mathbf { B } = 0$ to obtain 

$$
\mathbf {k} (t) - \mathbf {k} (0) = - e \mathbf {E} t / \hbar . \tag {40}
$$

If the force $\mathbf { F } = - e \mathbf { E }$ is applied at time $t = 0$ to an electron gas that fills the Fermi sphere centered at the origin of k space, then at a later time t the sphere will be displaced to a new center at 

$$
\delta \mathbf {k} = - e \mathbf {E} t / \hbar . \tag {41}
$$

Notice that the Fermi sphere is displaced as a whole because every electron is displaced by the same k. 

Because of collisions of electrons with impurities, lattice imperfections, and phonons, the displaced sphere may be maintained in a steady state in an electric field. If the collision time is , the displacement of the Fermi sphere in the steady state is given by (41) with $t = \tau$ . The incremental velocity is $\mathbf { v } = \pmb { \delta } \mathbf { k } / m =$ $- e \mathbf { E } \tau / m$ . If in a constant electric field E there are n electrons of charge $q = - e$ per unit volume, the electric current density is 

$$
\mathbf {j} = n q \mathbf {v} = n e ^ {2} \boldsymbol {\tau} \mathbf {E} / m. \tag {42}
$$

This is Ohm’s law. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/7c7880ca3c6bc264ff0d3b3b82934c42a14741fb0b09ff1898e9e4d8b19e3133.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/ac48c6a17770af0bbc6217ca4345dd1ab921712310f2f149a11032499be31e98.jpg)



(b)



Figure 10 (a) The Fermi sphere encloses the occupied electron orbitals in k space in the ground state of the electron gas. The net momentum is zero, because for every orbital k there is an occupied orbital at k. (b) Under the influence of a constant force F acting for a time interval t every orbital has its k vector increased by $\delta \mathbf { k } = \mathbf { F } t / \hbar$ This is equivalent to a displacement of the whole. Fermi sphere by k. The total momentum is if there are N electrons present. The applica-N-
k, tion of the force increases the energy of the system by $N ( \hbar \delta \mathbf { k } ) ^ { 2 } / 2 m$ .


The electrical conductivity  is defined by $\mathbf { j } = \sigma \mathbf { E }$ , so by (42) 

$$
\boxed {\sigma = \frac {n e ^ {2} \tau}{m}.} \tag {43}
$$

The electrical resistivity  is defined as the reciprocal of the conductivity, so that 

$$
\rho = m / n e ^ {2} \tau . \tag {44}
$$

Values of the electrical conductivity and resistivity of the elements are given in Table 3. In Gaussian units  has the dimensions of frequency. 

It is easy to understand the result (43) for the conductivity of a Fermi gas. We expect the charge transported to be proportional to the charge density ne; the factor e/m enters (43) because the acceleration in a given electric field is proportional to e and inversely proportional to the mass m. The time  describes the free time during which the field acts on the carrier. Closely the same result for the electrical conductivity is obtained for a classical (Maxwellian) gas of electrons, as realized at low carrier concentration in many semiconductor problems. 

# Experimental Electrical Resistivity of Metals

The electrical resistivity of most metals is dominated at room temperature (300 K) by collisions of the conduction electrons with lattice phonons and at 

<table><tr><td>Li</td><td>Be</td><td rowspan="4" colspan="10">(Resistivity values as given by G. T. Meaden, Electrical resistance of metals, Plenum, 1965; residual resistivities have been subtracted.)</td><td>B</td><td>C</td><td>N</td><td>O</td><td>F</td><td>Ne</td></tr><tr><td>1.07</td><td>3.08</td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>9.32</td><td>3.25</td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Na</td><td>Mg</td><td>Al</td><td>Si</td><td>P</td><td>S</td><td>Cl</td><td>Ar</td></tr><tr><td>2.11</td><td>2.33</td><td colspan="10">Conductivity in units of <eq>10^{5}</eq> (ohm·cm)<eq>^{-1}</eq>.</td><td>3.65</td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>4.75</td><td>4.30</td><td colspan="10">Resistivity in units of <eq>10^{-6}</eq> ohm·cm.</td><td>2.74</td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>K</td><td>Ca</td><td>Sc</td><td>Ti</td><td>V</td><td>Cr</td><td>Mn</td><td>Fe</td><td>Co</td><td>Ni</td><td>Cu</td><td>Zn</td><td>Ga</td><td>Ge</td><td>As</td><td>Se</td><td>Br</td><td>Kr</td></tr><tr><td>1.39</td><td>2.78</td><td>0.21</td><td>0.23</td><td>0.50</td><td>0.78</td><td>0.072</td><td>1.02</td><td>1.72</td><td>1.43</td><td>5.88</td><td>1.69</td><td>0.67</td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>7.19</td><td>3.6</td><td>46.8</td><td>43.1</td><td>19.9</td><td>12.9</td><td>139.</td><td>9.8</td><td>5.8</td><td>7.0</td><td>1.70</td><td>5.92</td><td>14.85</td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Rb</td><td>Sr</td><td>Y</td><td>Zr</td><td>Nb</td><td>Mo</td><td>Tc</td><td>Ru</td><td>Rh</td><td>Pd</td><td>Ag</td><td>Cd</td><td>In</td><td>Sn (w)</td><td>Sb</td><td>Te</td><td>I</td><td>Xe</td></tr><tr><td>0.80</td><td>0.47</td><td>0.17</td><td>0.24</td><td>0.69</td><td>1.89</td><td>~0.7</td><td>1.35</td><td>2.08</td><td>0.95</td><td>6.21</td><td>1.38</td><td>1.14</td><td>0.91</td><td>0.24</td><td></td><td></td><td></td></tr><tr><td>12.5</td><td>21.5</td><td>58.5</td><td>42.4</td><td>14.5</td><td>5.3</td><td>~14.</td><td>7.4</td><td>4.8</td><td>10.5</td><td>1.61</td><td>7.27</td><td>8.75</td><td>11.0</td><td>41.3</td><td></td><td></td><td></td></tr><tr><td>Cs</td><td>Ba</td><td>La</td><td>Hf</td><td>Ta</td><td>W</td><td>Re</td><td>Os</td><td>Ir</td><td>Pt</td><td>Au</td><td>Hg liq.</td><td>Tl</td><td>Pb</td><td>Bi</td><td>Po</td><td>At</td><td>Rn</td></tr><tr><td>0.50</td><td>0.26</td><td>0.13</td><td>0.33</td><td>0.76</td><td>1.89</td><td>0.54</td><td>1.10</td><td>1.96</td><td>0.96</td><td>4.55</td><td>0.10</td><td>0.61</td><td>0.48</td><td>0.086</td><td>0.22</td><td></td><td></td></tr><tr><td>20.0</td><td>39.</td><td>79.</td><td>30.6</td><td>13.1</td><td>5.3</td><td>18.6</td><td>9.1</td><td>5.1</td><td>10.4</td><td>2.20</td><td>95.9</td><td>16.4</td><td>21.0</td><td>116.</td><td>46.</td><td></td><td></td></tr></table>

<table><tr><td>Ce</td><td>Pr</td><td>Nd</td><td>Pm</td><td>Sm</td><td>Eu</td><td>Gd</td><td>Tb</td><td>Dy</td><td>Ho</td><td>Er</td><td>Tm</td><td>Yb</td><td>Lu</td></tr><tr><td>0.12</td><td>0.15</td><td>0.17</td><td></td><td>0.10</td><td>0.11</td><td>0.070</td><td>0.090</td><td>0.11</td><td>0.13</td><td>0.12</td><td>0.16</td><td>0.38</td><td>0.19</td></tr><tr><td>81.</td><td>67.</td><td>59.</td><td></td><td>99.</td><td>89.</td><td>134.</td><td>111.</td><td>90.0</td><td>77.7</td><td>81.</td><td>62.</td><td>26.4</td><td>53.</td></tr><tr><td>Th</td><td>Pa</td><td>U</td><td>Np</td><td>Pu</td><td>Am</td><td>Cm</td><td>Bk</td><td>Cf</td><td>Es</td><td>Fm</td><td>Md</td><td>No</td><td>Lr</td></tr><tr><td>0.66</td><td></td><td>0.39</td><td>0.085</td><td>0.070</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>15.2</td><td></td><td>25.7</td><td>118.</td><td>143.</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></table>

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/d7e1252e203574fcac6f41b120c2118db75ed2f3ffd2bdf9a3bc77b7c3a11d24.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/0e164020b233034f698aeb678e8e131027aa261d51aba1aa45b122c3505b8f06.jpg)



(b)



Figure 11 Electrical resistivity in most metals arises from collisions of electrons with irregularities in the lattice, as in (a) by phonons and in (b) by impurities and vacant lattice sites.


liquid helium temperature (4 K) by collisions with impurity atoms and mechanical imperfections in the lattice (Fig. 11). The rates of these collisions are often independent to a good approximation, so that if the electric field were switched off the momentum distribution would relax back to its ground state with the net relaxation rate 

$$
\frac {1}{\tau} = \frac {1}{\tau_ {L}} + \frac {1}{\tau_ {i}}, \tag {45}
$$

where $\tau _ { L }$ and $\tau _ { i }$ are the collision times for scattering by phonons and by imperfections, respectively. 

The net resistivity is given by 

$$
\rho = \rho_ {L} + \rho_ {i}, \tag {46}
$$

where $\rho _ { L }$ is the resistivity caused by the thermal phonons, and $\rho _ { i }$ is the resistivity caused by scattering of the electron waves by static defects that disturb the periodicity of the lattice. Often $\rho _ { L }$ is independent of the number of defects when their concentration is small, and often $\rho _ { i }$ is independent of temperature. This empirical observation expresses Matthiessen’s rule, which is convenient in analyzing experimental data (Fig. 12). 

The residual resistivity, $\rho _ { i } ( 0 )$ , is the extrapolated resistivity at 0 K because $\rho _ { L }$ vanishes as $T \to 0$ . The lattice resistivity, $\rho _ { L } ( T ) = \rho - \rho _ { i } ( 0 )$ , is the same for different specimens of a metal, even though $\rho _ { i } ( 0 )$ may itself vary widely. The resistivity ratio of a specimen is usually defined as the ratio of its resistivity at room temperature to its residual resistivity. It is a convenient approximate indicator of sample purity: for many materials an impurity in solid solution creates a residual resistivity of about 1 ohm-cm $( 1 \bar { \times } 1 0 ^ { - 6 }$ ohm-cm) per atomic percent of impurity. A copper specimen with a resistivity ratio of 1000 will have a residual resistivity of $1 . 7 \times 1 0 ^ { - 3 }$ ohm-cm, corresponding to an impurity concentration of about 20 ppm. In exceptionally pure specimens the resistivity ratio may be as high as $1 0 ^ { 6 }$ , whereas in some alloys (e.g., manganin) it is as low as 1.1. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/330c925f0379044b40a01e121f69c20cc6f4e234a870221e1aca1e2afe44eb11.jpg)



Figure 12 Resistance of potassium below 20 K, as measured on two specimens by D. MacDonald and K. Mendelssohn. The different intercepts at 0 K are attributed to different concentrations of impurities and static imperfections in the two specimens.


It is possible to obtain crystals of copper so pure that their conductivity at liquid helium temperatures (4 K) is nearly $1 0 ^ { 5 }$ times that at room temperature; for these conditions $\tau \approx 2 \times 1 0 ^ { - 9 } \mathrm { s } \mathrm { a t } 4 \mathrm { K }$ . The mean free path of a conduc- tion electron is defined as 

$$
\ell = v _ {F} \tau , \tag {47}
$$

where ${ \bf v } _ { F }$ is the velocity at the Fermi surface, because all collisions involve only electrons near the Fermi surface. From Table 1 we have $v _ { F } = 1 . 5 7 \times 1 0 ^ { 8 } \mathrm { { c m } \ s ^ { - } }$ for Cu, thus the mean free path is $\ell ( 4 \ : \mathrm { K } ) \approx 0 . 3 \ : \mathrm { c m }$ Mean free paths as long as. 10 cm have been observed in very pure metals in the liquid helium temperature range. 

The temperature-dependent part of the electrical resistivity is proportional to the rate at which an electron collides with thermal phonons and thermal electrons. The collision rate with phonons is proportional to the concentration of thermal phonons. One simple limit is at temperatures over the Debye temperature : here the phonon concentration is proportional to the temperature T, so that $\rho \propto T$ for $T > \theta , \mathrm { A }$ sketch of the theory is given in Appendix J. 

# Umklapp Scattering

Umklapp scattering of electrons by phonons (Chapter 5) accounts for most of the electrical resistivity of metals at low temperatures. These are electron-phonon scattering processes in which a reciprocal lattice vector G is involved, so that electron momentum change in the process may be much larger than in a normal electron-phonon scattering process at low temperatures. (In an umklapp process the wavevector of one particle may be “flipped over.”) 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/9adca2515d1ddc47294d037d405a497eced2081ee8a7c61ce5be58e6d2dab9f8.jpg)



Figure 13 Two Fermi spheres in adjacent zones: a construction to show the role of phonon umklapp processes in electrical resistivity.


Consider a section perpendicular to [100] through two adjacent Brillouin zones in bcc potassium, with the equivalent Fermi spheres inscribed within each (Fig. 13). The lower half of the figure shows the normal electron-phonon collision $\mathbf { k } ^ { \prime } = \mathbf { k } + \mathbf { q }$ while the upper half shows a possible scattering process $\mathbf { k } ^ { \prime } = \mathbf { k } + \mathbf { q } + \mathbf { G }$ involving the same phonon and terminating outside the first Brillouin zone, at the point A. This point is exactly equivalent to the point $A ^ { \prime }$ inside the original zone, where $A A ^ { \prime }$ is a reciprocal lattice vector G. This scattering is an umklapp process, in analogy to phonons. Such collisions are strong scatterers because the scattering angle can be close to . 

When the Fermi surface does not intersect the zone boundary, there is some minimum phonon wavevector $q _ { 0 }$ for umklapp scattering. At low enough temperatures the number of phonons available for umklapp scattering falls as $\exp ( - \theta _ { U } / T )$ , where $\theta _ { U }$ is a characteristic temperature calculable from the geometry of the Fermi surface inside the Brillouin zone. For a spherical Fermi surface with one electron orbital per atom inside the bcc Brillouin zone, one shows by geometry that $q _ { 0 } = 0 . 2 6 7 k _ { F }$ . 

The experimental data (Fig. 12) for potassium have the expected exponential form with $\theta _ { U } = 2 3$ K compared with the Debye   91 K. At the very lowest temperatures (below about 2 K in potassium) the number of umklapp processes is negligible and the lattice resistivity is then caused only by small angle scattering, which is the normal (not umklapp) scattering. 

# MOTION IN MAGNETIC FIELDS

By the arguments of (39) and (41) we are led to the equation of motion for the displacement k of a Fermi sphere of particles acted on by a force F and by friction as represented by collisions at a rate 1/: 

$$
\hbar \left(\frac {d}{d t} + \frac {1}{\tau}\right) \delta \mathbf {k} = \mathbf {F}. \tag {48}
$$

The free particle acceleration term is $( \hbar d / d t )$ and the effect of collisions 
k (the friction) is represented by where  is the collision time.-
k/, 

Consider now the motion of the system in a uniform magnetic field B. The Lorentz force on an electron is 

$$
\mathbf {F} = - e \left(\mathbf {E} + \frac {\mathbf {1}}{c} \mathbf {v} \times \mathbf {B}\right); \tag {49}
$$

$$
\mathbf {F} = - e (\mathbf {E} + \mathbf {v} \times \mathbf {B}) \tag {SI}
$$

If $m \mathbf { v } = \hbar \delta \mathbf { k }$ then the equation of motion is, 

$$
m \left(\frac {d}{d t} + \frac {1}{\tau}\right) \mathbf {v} = - e \left(\mathbf {E} + \frac {1}{c} \mathbf {v} \times \mathbf {B}\right). \tag {50}
$$

An important situation is the following: let a static magnetic field B lie along the z axis. Then the component equations of motion are 

$$
m \left(\frac {d}{d t} + \frac {1}{\tau}\right) v _ {x} = - e \left(E _ {x} + \frac {B}{c} v _ {y}\right); \tag {CGS}
$$

$$
m \left(\frac {d}{d t} + \frac {1}{\tau}\right) v _ {y} = - e \left(E _ {y} - \frac {B}{c} v _ {x}\right); \tag {51}
$$

$$
m \left(\frac {d}{d t} + \frac {1}{\tau}\right) v _ {z} = - e E _ {z}.
$$

The results in SI are obtained by replacing c by 1. 

In the steady state in a static electric field the time derivatives are zero, so that the drift velocity is 

$$
v _ {x} = - \frac {e \tau}{m} E _ {x} - \omega_ {c} \tau v _ {y}; \quad v _ {y} = - \frac {e \tau}{m} E _ {y} + \omega_ {c} \tau v _ {x}; \quad v _ {z} = - \frac {e \tau}{m} E _ {z}, \tag {52}
$$

where $\omega _ { c } = e B / m c$ is the cyclotron frequency, as discussed in Chapter 8 for cyclotron resonance in semiconductors. 

# Hall Effect

The Hall field is the electric field developed across two faces of a conductor, in the direction j  B, when a current j flows across a magnetic field B. Consider a rod-shaped specimen in a longitudinal electric field $E _ { x }$ and a transverse magnetic field, as in Fig. 14. If current cannot flow out of the rod in the y direction we must have $\mathfrak { d } v _ { y } = 0$ . From (52) this is possible only if there is a transverse electric field 

$$
E _ {y} = - \omega_ {c} \tau E _ {x} = - \frac {e B \tau}{m c} E _ {x}; \tag {53}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-18/fd659c53-ffc1-4f0a-8d03-b239cb666537/ca247da9fff5b8b7157f7e31f22630ec33521c7296923bbcb7421200d75dd76a.jpg)



Figure 14 The standard geometry for the Hall effect: a rod-shaped specimen of rectangular cross-section is placed in a magnetic field $B _ { z }$ , as in (a). An electric field $E _ { x }$ applied across the end electrodes causes an electric current density $j _ { x }$ to flow down the rod. The drift velocity of the negatively-charged electrons immediately after the electric field is applied as shown in (b). The deflection in the $- y$ direction is caused by the magnetic field. Electrons accumulate on one face of the rod and a positive ion excess is established on the opposite face until, as in (c), the transverse electric field (Hall field) just cancels the Lorentz force due to the magnetic field.


$$
E _ {y} = - \omega_ {c} \tau E _ {x} = - \frac {e B \tau}{m} E _ {x}. \tag {SI}
$$

The quantity defined by 

$$
\boxed {R _ {H} = \frac {E _ {y}}{j _ {x} B}} \tag {54}
$$

is called the Hall coefficient. To evaluate it on our simple model we use $j _ { x } =$ $n e ^ { 2 } \tau E _ { x } / m$ and obtain 

$$
R _ {H} = - \frac {e B \tau E _ {x} / m c}{n e ^ {2} \tau E _ {x} B / m} = - \frac {1}{n e c}; \tag {55}
$$

$$
R _ {H} = - \frac {1}{n e}. \tag {SI}
$$

This is negative for free electrons, for e is positive by definition. 

Table 4 Comparison of observed Hall coefficients with free electron theory 

[The experimental values of $R _ { H }$ as obtained by conventional methods are summarized from data at room temperature presented in the Landolt-Bornstein tables. The values obtained by the helicon wave method at 4 K are by J. M. Goodman. The values of the carrier concentration n are from Table 1.4 except for Na, K, Al, In, where Goodman’s values are used. To convert the value of $R _ { H }$ in CGS units to the value in volt-cm/amp-gauss, multiply by $9 \times 1 0 ^ { 1 1 }$ ; to convert $R _ { H }$ in CGS to m3 /coulomb, multiply by $9 \times 1 0 ^ { 1 3 } .$ ] 

<table><tr><td>Metal</td><td>Method</td><td>Experimental<eq>R_H</eq>,in <eq>10^{-24}</eq> CGS units</td><td>Assumedcarriersper atom</td><td>Calculated-1/nec,in <eq>10^{-24}</eq> CGS units</td></tr><tr><td>Li</td><td>conv.</td><td>-1.89</td><td>1 electron</td><td>-1.48</td></tr><tr><td rowspan="2">Na</td><td>helicon</td><td>-2.619</td><td>1 electron</td><td>-2.603</td></tr><tr><td>conv.</td><td>-2.3</td><td></td><td></td></tr><tr><td rowspan="2">K</td><td>helicon</td><td>-4.946</td><td>1 electron</td><td>-4.944</td></tr><tr><td>conv.</td><td>-4.7</td><td></td><td></td></tr><tr><td>Rb</td><td>conv.</td><td>-5.6</td><td>1 electron</td><td>-6.04</td></tr><tr><td>Cu</td><td>conv.</td><td>-0.6</td><td>1 electron</td><td>-0.82</td></tr><tr><td>Ag</td><td>conv.</td><td>-1.0</td><td>1 electron</td><td>-1.19</td></tr><tr><td>Au</td><td>conv.</td><td>-0.8</td><td>1 electron</td><td>-1.18</td></tr><tr><td>Be</td><td>conv.</td><td>+2.7</td><td>—</td><td>—</td></tr><tr><td>Mg</td><td>conv.</td><td>-0.92</td><td>—</td><td>—</td></tr><tr><td>Al</td><td>helicon</td><td>+1.136</td><td>1 hole</td><td>+1.135</td></tr><tr><td>In</td><td>helicon</td><td>+1.774</td><td>1 hole</td><td>+1.780</td></tr><tr><td>As</td><td>conv.</td><td>+50.</td><td>—</td><td>—</td></tr><tr><td>Sb</td><td>conv.</td><td>-22.</td><td>—</td><td>—</td></tr><tr><td>Bi</td><td>conv.</td><td>-6000.</td><td>—</td><td>—</td></tr></table>

The lower the carrier concentration, the greater the magnitude of the Hall coefficient. Measuring $R _ { H }$ is an important way of measuring the carrier concentration. Note: The symbol $R _ { H }$ denotes the Hall coefficient (54), but the same symbol is sometimes used with a different meaning, that of Hall resistance in two-dimensional problems. 

The simple result (55) follows from the assumption that all relaxation times are equal, independent of the velocity of the electron. A numerical factor of order unity enters if the relaxation time is a function of the velocity. The expression becomes somewhat more complicated if both electrons and holes contribute to the conductivity. 

In Table 4 observed values of the Hall coefficient are compared with values calculated from the carrier concentration. The most accurate measurements are made by the method of helicon resonance which is treated as a problem in Chapter 14. 

The accurate values for sodium and potassium are in excellent agreement with values calculated for one conduction electron per atom, using (55). 

Notice, however, the experimental values for the trivalent elements aluminum and indium: these agree with values calculated for one positive charge carrier per atom and thus disagree in magnitude and sign with values calculated for the expected three negative charge carriers. 

The problem of an apparent positive sign for the charge carriers arises also for Be and As, as seen in the table. The anomaly of the sign was explained by Peierls (1928). The motion of carriers of apparent positive sign, which Heisenberg later called “holes,” cannot be explained by a free electron gas, but finds a natural explanation in terms of the energy band theory to be developed in Chapters 7–9. Band theory also accounts for the occurrence of very large values of the Hall coefficient, as for As, Sb, and Bi. 

# THERMAL CONDUCTIVITY OF METALS

In Chapter 5 we found an expression $\begin{array} { r } { K = \frac { 1 } { 3 } C v \ell } \end{array}$ for the thermal conductivity of particles of velocity v, heat capacity C per unit volume, and mean free path . The thermal conductivity of a Fermi gas follows from (36) for the heat capacity, and with $\begin{array} { r } { \epsilon _ { F } = \frac { 1 } { 2 } m v _ { F } ^ { 2 } } \end{array}$ : 

$$
K _ {e l} = \frac {\pi^ {2}}{3} \cdot \frac {n k _ {B} ^ {2} T}{m v _ {F} ^ {2}} \cdot v _ {F} \cdot \ell = \frac {\pi^ {2} n k _ {B} ^ {2} T \tau}{3 m}. \tag {56}
$$

Here $\ell = v _ { F } \tau ;$ the electron concentration is n, and  is the collision time. 

Do the electrons or the phonons carry the greater part of the heat current in a metal? In pure metals the electronic contribution is dominant at all temperatures. In impure metals or in disordered alloys, the electron mean free path is reduced by collisions with impurities, and the phonon contribution may be comparable with the electronic contribution. 

# Ratio of Thermal to Electrical Conductivity

The Wiedemann-Franz law states that for metals at not too low temperatures the ratio of the thermal conductivity to the electrical conductivity is directly proportional to the temperature, with the value of the constant of proportionality independent of the particular metal. This result was important in the history of the theory of metals, for it supported the picture of an electron gas as the carrier of charge and energy. It can be explained by using (43) for  and (56) for K: 

$$
\frac {K}{\sigma} = \frac {\pi^ {2} k _ {B} ^ {2} T n \tau / 3 m}{n e \tau^ {2} / m} = \frac {\pi^ {2}}{3} \left(\frac {k _ {B}}{e}\right) ^ {2} T. \tag {57}
$$


Table 5 Experimental Lorenz numbers


<table><tr><td colspan="3"><eq>L \times 10^{8}</eq> watt-ohm/<eq>deg^2</eq></td><td colspan="3"><eq>L \times 10^{8}</eq> watt-ohm/<eq>deg^2</eq></td></tr><tr><td>Metal</td><td>0°C</td><td>100°C</td><td>Metal</td><td>0°C</td><td>100°C</td></tr><tr><td>Ag</td><td>2.31</td><td>2.37</td><td>Pb</td><td>2.47</td><td>2.56</td></tr><tr><td>Au</td><td>2.35</td><td>2.40</td><td>Pt</td><td>2.51</td><td>2.60</td></tr><tr><td>Cd</td><td>2.42</td><td>2.43</td><td>Su</td><td>2.52</td><td>2.49</td></tr><tr><td>Cu</td><td>2.23</td><td>2.33</td><td>W</td><td>3.04</td><td>3.20</td></tr><tr><td>Mo</td><td>2.61</td><td>2.79</td><td>Zn</td><td>2.31</td><td>2.33</td></tr></table>

The Lorenz number L is defined as 

$$
L = K / \sigma T, \tag {58}
$$

and according to (57) should have the value 

$$
\begin{array}{l} L = \frac {\pi^ {2}}{3} \left(\frac {k _ {B}}{e}\right) ^ {2} = 2. 7 2 \times 1 0 ^ {- 1 3} (\mathrm{erg/esu-deg}) ^ {2} \\ = 2. 4 5 \times 1 0 ^ {- 8} \text {   watt - ohm / deg } ^ {2}. \tag {59} \\ \end{array}
$$

This remarkable result involves neither n nor m. Experimental values of L at $0 ^ { \circ } \mathrm { C }$ and at $1 0 0 ^ { \circ } \mathrm { C }$ as given in Table 5 are in good agreement with (59). 

# Problems

1. Kinetic energy of electron gas. Show that the kinetic energy of a three-dimensional gas of N free electrons at 0 K is 

$$
U _ {0} = \frac {3}{5} N \epsilon_ {F}. \tag {60}
$$

2. Pressure and bulk modulus of an electron gas. (a) Derive a relation connecting the pressure and volume of an electron gas at 0 K. Hint: Use the result of Problem 1 and the relation between $\epsilon _ { F }$ and electron concentration. The result may be written as $\textstyle p = { \frac { 2 } { 3 } } ( U _ { 0 } / V )$ (b) Show that the bulk modulus. $B = - V ( \partial p / \partial V )$ of an electron gas at 0 K is $B = 5 p / 3 = 1 0 U _ { 0 } / 9 V$ . (c) Estimate for potassium, using Table 1, the value of the electron gas contribution to B. 

3. Chemical potential in two dimensions. Show that the chemical potential of a Fermi gas in two dimensions is given by: 

$$
\mu (T) = k _ {B} T \ln \left[ \exp (\pi n \hbar^ {2} / m k _ {B} T) - 1 \right], \tag {61}
$$

for n electrons per unit area. Note: The density of orbitals of a free electron gas in two dimensions is independent of energy: $D ( \epsilon ) \dot { = } m / \pi \hbar ^ { 2 }$ per unit area of specimen. , 

4. Fermi gases in astrophysics. (a) Given $M _ { \odot } = 2 \times 1 0 ^ { 3 3 } \mathrm { g }$ for the mass of the Sun, estimate the number of electrons in the Sun. In a white dwarf star this number of electrons may be ionized and contained in a sphere of radius $2 \times 1 0 ^ { 9 }$ cm; find the Fermi energy of the electrons in electron volts. (b) The energy of an electron in the relativistic limit $\epsilon \gg m c ^ { 2 }$ is related to the wavevector as $\epsilon \cong p c = \hbar k c$ Show that the. Fermi energy in this limit is $\epsilon _ { F } \approx \hbar c ~ ( N / V ) ^ { 1 / 3 }$ roughly. (c) If the above number of, electrons were contained within a pulsar of radius 10 km, show that the Fermi energy would be ${ \approx } 1 0 ^ { 8 } \mathrm { e V } .$ This value explains why pulsars are believed to be composed largely of neutrons rather than of protons and electrons, for the energy release in the reaction $n  p + e ^ { - }$ is only $0 . 8 \times 1 0 ^ { 6 } \mathrm { e V } ,$ which is not large enough to enable many electrons to form a Fermi sea. The neutron decay proceeds only until the electron concentration builds up enough to create a Fermi level of $0 . 8 \times 1 0 ^ { 6 } \ \mathrm { e V } ,$ at which point the neutron, proton, and electron concentrations are in equilibrium. 

5. Liquid $H e ^ { 3 }$ . The atom $\mathrm { H e ^ { 3 } }$ has spin $\frac { 1 } { 2 }$ and is a fermion. The density of liquid $\mathrm { H e ^ { 3 } }$ is 0.081 $\mathrm { g \ c m ^ { - 3 } }$ near absolute zero. Calculate the Fermi energy $\epsilon _ { F }$ and the Fermi temperature $T _ { F } .$ 

6. Frequency dependence of the electrical conductivity. Use the equation $m ( d v / d t + v / \tau ) = - e E$ for the electron drift velocity v to show that the conductivity at frequency  is 

$$
\sigma (\omega) = \sigma (0) \left(\frac {1 + i \omega \tau}{1 + (\omega \tau) ^ {2}}\right), \tag {62}
$$

where $\sigma ( 0 ) = n e ^ { 2 } \tau / m$ . 

* 7. Dynamic magnetoconductivity tensor for free electrons. A metal with a concentration n of free electrons of charge e is in a static magnetic field B . The electriczˆ current density in the xy plane is related to the electric field by 

$$
j _ {x} = \sigma_ {x x} E _ {x} + \sigma_ {x y} E _ {y}; \quad j _ {y} = \sigma_ {y z} E _ {x} + \sigma_ {y y} E _ {y}.
$$

Assume that the frequency $\omega \gg \omega _ { c }$ and $\omega \gg 1 / \tau$ , where $\omega _ { c } = e B / m c$ and $\tau$ is the collision time. (a) Solve the drift velocity equation (51) to find the components of the magnetoconductivity tensor: 

$$
\sigma_ {x x} = \sigma_ {y y} = i \omega_ {p} ^ {2} / 4 \pi \omega ; \quad \sigma_ {x y} = - \sigma_ {y x} = \omega_ {c} \omega_ {p} ^ {2} / 4 \pi \omega^ {2},
$$

where $\omega _ { p } ^ { 2 } = 4 \pi n e ^ { 2 } / m$ (b) Note from a Maxwell equation that the dielectric func-. tion tensor of the medium is related to the conductivity tensor as $\boldsymbol { \epsilon } = \mathbf { 1 } + i ( 4 \pi / \omega ) \mathbf { \sigma }$ . Consider an electromagnetic wave with wavevector ${ \bf k } = k \hat { \bf z }$ . Show that the dispersion relation for this wave in the medium is 

$$
c ^ {2} k ^ {2} = \omega^ {2} - \omega_ {p} ^ {2} \pm \omega_ {c} \omega_ {p} ^ {2} / \omega . \tag {63}
$$

At a given frequency there are two modes of propagation with different wavevectors and different velocities. The two modes correspond to circularly polarized 

* This problem is somewhat difficult. 

waves. Because a linearly polarized wave can be decomposed into two circularly polarized waves, it follows that the plane of polarization of a linearly polarized wave will be rotated by the magnetic field. 

* 8. Cohesive energy of free electron Fermi gas. We define the dimensionless length $r _ { s } ,$ as $r _ { 0 } / a _ { H }$ , where $r _ { 0 }$ is the radius of a sphere that contains one electron, and $a _ { H }$ is the bohr radius $\hbar ^ { 2 } / e ^ { 2 } m$ (a) Show that the average kinetic energy per elec-. tron in a free electron Fermi gas at 0 K is $2 . 2 1 / r _ { s } ^ { 2 } .$ where the energy is expressed in, rydbergs, with $1 ~ \mathrm { R y } = m e ^ { 4 } / 2 \hbar ^ { 2 } .$ (b) Show that the coulomb energy of a point positive charge e interacting with the uniform electron distribution of one electron in the volume of radius $r _ { 0 }$ is $- 3 e ^ { 2 } / 2 r _ { 0 } , \mathrm { o r } - 3 / r _ { s }$ in rydbergs. (c) Show that the coulomb self-energy of the electron distribution in the sphere is $3 e ^ { 2 } / 5 r _ { 0 } , 0 \mathrm { r } 6 / 5 r _ { \mathrm { s } }$ in rydbergs. (d) The sum of (b) and (c) gives $- 1 . 8 0 / r _ { s }$ for the total coulomb energy per electron. Show that the equilibrium value of $r _ { s }$ is 2.45. Will such a metal be stable with respect to separated H atoms? 

9. Static magnetoconductivity tensor. For the drift velocity theory of (51), show that the static current density can be written in matrix form as 

$$
\left( \begin{array}{c} j _ {x} \\ j _ {y} \\ j _ {z} \end{array} \right) = \frac {\sigma_ {0}}{1 + (\omega_ {c} \tau) ^ {2}} \left( \begin{array}{c c c} 1 & - \omega_ {c} \tau & 0 \\ \omega_ {c} \tau & 1 & 0 \\ 0 & 0 & 1 + (\omega_ {c} \tau) ^ {2} \end{array} \right) \left( \begin{array}{c} E _ {x} \\ E _ {y} \\ E _ {z} \end{array} \right). \tag {64}
$$

In the high magnetic field limit of $\omega _ { c } \tau \gg 1$ , show that 

$$
\sigma_ {y x} = n e c / B = - \sigma_ {x y}. \tag {65}
$$

In this limit $\sigma _ { x x } = 0$ , to order $1 / \omega _ { c } \tau$ . The quantity $\sigma _ { y x }$ is called the Hall conductivity. 

10. Maximum surface resistance. Consider a square sheet of side L, thickness d, and electrical resistivity $\rho .$ The resistance measured between opposite edges of the sheet is called the surface resistance: $R _ { \mathrm { s q } } = \rho L / L d = \rho / d$ , which is independent of the area $L ^ { 2 }$ of the sheet. $( R _ { \mathrm { s q } }$ is called the resistance per square and is expressed in ohms per square, because $\rho / d$ has the dimensions of ohms.) If we express $\rho$ by (44), then $R _ { \mathrm { s q } } = m / n d e ^ { 2 } \tau$ . Suppose now that the minimum value of the collision time is determined by scattering from the surfaces of the sheet, so that $\tau \approx d / v _ { F } ,$ , where $v _ { F }$ is the Fermi velocity. Thus the maximum surface resistivity is $R _ { \mathrm { s q } } \approx m v _ { F } / n d ^ { 2 } e ^ { 2 }$ . Show for a monatomic metal sheet one atom in thickness that $R _ { \mathrm { s q } } \approx \dot { \hbar } / e ^ { 2 } = 4 . 1 \mathrm { k } \Omega$ . 