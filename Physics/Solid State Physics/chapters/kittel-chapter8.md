# 8

# Semiconductor Crystals

BAND GAP 187 

EQUATIONS OF MOTION 191 

Physical derivation of -k - F 193 

Holes 194 

Effective mass 197 

Physical interpretation of the effective mass 198 

Effective masses in semiconductors 200 

Silicon and germanium 202 

INTRINSIC CARRIER CONCENTRATION 205 

Intrinsic mobility 208 

IMPURITY CONDUCTIVITY 209 

Donor states 209 

Acceptor states 211 

Thermal ionization of donors and acceptors 213 

THERMOELECTRIC EFFECTS 214 

SEMIMETALS 215 

SUPERLATTICES 216 

Bloch oscillator 217 

Zener tunneling 217 

SUMMARY 217 

PROBLEMS 218 

1. Impurity orbits 218 

2. Ionization of donors 218 

NOTE: The discussion of carrier orbits in applied fields is continued in Chapter 9. 

3. Hall effect with two carrier types 218 

4. Cyclotron resonance for a spheroidal energy surface 219 

5. Magnetoresistance with two carrier types 219 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/e7dee2a803e28e0f0e852b73dfb6e9530e3fd6c2029f02f22479ba36b51cc9d5.jpg)



Figure 1 Carrier concentrations for metals, semimetals, and semiconductors. The semiconductor range may be extended upward by increasing the impurity concentration, and the range can be extended downward to merge eventually with the insulator range.


Carrier concentrations representative of metals, semimetals, and semiconductors are shown in Fig. 1. Semiconductors are generally classified by their electrical resistivity at room temperature, with values in the range of $1 0 ^ { - 2 }$ to $1 0 ^ { 9 }$ ohm-cm, and strongly dependent on temperature. At absolute zero a pure, perfect crystal of most semiconductors will be an insulator, if we arbitrarily define an insulator as having a resistivity above $1 0 ^ { 1 4 }$ ohm-cm. 

Devices based on semiconductors include transistors, switches, diodes, photovoltaic cells, detectors, and thermistors. These may be used as single circuit elements or as components of integrated circuits. We discuss in this chapter the central physical features of the classical semiconductor crystals, particularly silicon, germanium, and gallium arsenide. 

Some useful nomenclature: the semiconductor compounds of chemical formula AB, where A is a trivalent element and B is a pentavalent element, are called III-V (three-five) compounds. Examples are indium antimonide and gallium arsenide. Where A is divalent and B is hexavalent, the compound is called a II-VI compound; examples are zinc sulfide and cadmium sulfide. Silicon and germanium are sometimes called diamond-type semiconductors, because they have the crystal structure of diamond. Diamond itself is more an insulator rather than a semiconductor. Silicon carbide SiC is a IV-IV compound. 

A highly purified semiconductor exhibits intrinsic conductivity, as distinguished from the impurity conductivity of less pure specimens. In the intrinsic temperature range the electrical properties of a semiconductor are not essentially modified by impurities in the crystal. An electronic band scheme leading to intrinsic conductivity is indicated in Fig. 2. The conduction band is vacant at absolute zero and is separated by an energy gap $E _ { \mathrm { g } }$ from the filled valence band. 

The band gap is the difference in energy between the lowest point of the conduction band and the highest point of the valence band. The lowest point in the conduction band is called the conduction band edge; the highest point in the valence band is called the valence band edge. 

As the temperature is increased, electrons are thermally excited from the valence band to the conduction band (Fig. 3). Both the electrons in the conduction band and the vacant orbitals or holes left behind in the valence band contribute to the electrical conductivity. 

# BAND GAP

The intrinsic conductivity and intrinsic carrier concentrations are largely controlled by $E _ { \mathrm { g } } / k _ { B } T$ , the ratio of the band gap to the temperature. When this ratio is large, the concentration of intrinsic carriers will be low and the conductivity will be low. Band gaps of representative semiconductors are given in Table 1. The best values of the band gap are obtained by optical absorption. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/ecea33d957b0305e4fd60e7761ef1de86e458a7249aeea0a5abe3ee64db976cd.jpg)



Figure 2 Band scheme for intrinsic conductivity in a semiconductor. At 0 K the conductivity is zero because all states in the valence band are filled and all states in the conduction band are vacant. As the temperature is increased, electrons are thermally excited from the valence band to the conduction band, where they become mobile. Such carriers are called “intrinsic.”


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/1597ebd2373d5ccbcd8168af47f88ca762c75d188713898ddf791406718c6178.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/76fb9114eeab55e490b8649858e6eca509f8b212ba2f1109b9a29a1ce5cb1d9b.jpg)



(b)



Figure 3 Intrinsic electron concentration as a function of temperature for (a) germanium and (b) silicon. Under intrinsic conditions the hole concentration is equal to the electron concentration. The intrinsic concentration at a given temperature is higher in Ge than in Si because the energy gap is narrower in Ge (0.66 eV) than in Si (1.11 eV). (After W. C. Dunlap.)


In a direct absorption process the threshold of continuous optical absorption at frequency $\omega _ { \mathrm { g } }$ measures the band gap $E _ { \mathrm { g } } = \hbar \omega _ { \mathrm { g } }$ as shown in Figs. 4a and 5a. A photon is absorbed by the crystal with the creation of an electron and a hole. 

In the indirect absorption process in Figs. 4b and 5b the minimum energy gap of the band structure involves electrons and holes separated by a 


CRYSTAL WITH DIRECT GAP


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/987350f6eb16b29f971f9d82556f7aba92ce512a8acd56be970f9a88252e5c00.jpg)



CRYSTAL WITH INDIRECT GAP


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/0e59b0f6add16f792e2fabbc9fb7cdd4a8b36be63c74df2e07d9047005a525a0.jpg)



(b)



Figure 4 Optical absorption in pure insulators at absolute zero. In (a) the threshold determines the energy gap as $E _ { \mathrm { g } } = \hbar \omega _ { \mathrm { g } }$ In (b) the optical absorption is weaker near the threshold: at. $\hbar \omega = E _ { \mathrm { g } } + \hbar \Omega$ a photon is absorbed with the creation of three particles: a free electron, a free hole, and a phonon of energy . In (b) the energy- $E _ { \mathrm { v e r t } }$ marks the threshold for the creation of a free electron and a free hole, with no phonon involved. Such a transition is called vertical; it is similar to the direct transition in (a). These plots do not show absorption lines that sometimes are seen lying just to the low energy side of the threshold. Such lines are due to the creation of a bound electron-hole pair, called an exciton.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/104eee46a58ad3170e9422c84155f4d527936bde319dbbafeb3ea5f9c7373ba7.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/5dec13c72b65ef81ab97d26c9f1cf974d90b11e9a8bd329d16e6fb04ac5b827b.jpg)



(b)



Figure 5 In (a) the lowest point of the conduction band occurs at the same value of k as the highest point of the valence band. A direct optical transition is drawn vertically with no significant change of k, because the absorbed photon has a very small wavevector. The threshold frequency $\omega _ { \mathrm { g } }$ for absorption by the direct transition determines the energy gap $E _ { \mathrm { g } } = \hbar \omega _ { \mathrm { g } }$ The indirect transition in (b) in-. volves both a photon and a phonon because the band edges of the conduction and valence bands are widely separated in k space. The threshold energy for the indirect process in (b) is greater than the true band gap. The absorption threshold for the indirect transition between the band edges is at $\hbar \omega = E _ { \mathrm { g } } + \hbar \Omega$ , where  is the frequency of an emitted phonon of wavevector $\mathbf { K } \cong - \mathbf { k } _ { \mathrm { g } } . \mathbf { A } \mathbf { t }$ higher temperatures phonons are already present; if a phonon is absorbed along with a photon, the threshold energy is $\hbar \omega = E _ { \mathrm { g } } - \hbar \Omega$ . Note: The figure shows only the threshold transitions. Transitions occur generally between almost all points of the two bands for which the wavevectors and energy can be conserved.



Table 1 Energy gap between the valence and conduction bands (i - indirect gap; d - direct gap)


<table><tr><td rowspan="2">Crystal</td><td rowspan="2">Gap</td><td colspan="2"><eq>E_g</eq>, eV</td><td rowspan="2">Crystal</td><td rowspan="2">Gap</td><td colspan="2"><eq>E_g</eq>, eV</td></tr><tr><td>0 K</td><td>300 K</td><td>0 K</td><td>300 K</td></tr><tr><td>Diamond</td><td>i</td><td>5.4</td><td></td><td>SiC(hex)</td><td>i</td><td>3.0</td><td>—</td></tr><tr><td>Si</td><td>i</td><td>1.17</td><td>1.11</td><td>Tc</td><td>d</td><td>0.33</td><td>—</td></tr><tr><td>Ge</td><td>i</td><td>0.744</td><td>0.66</td><td>HgTea</td><td>d</td><td>-0.30</td><td></td></tr><tr><td>αSn</td><td>d</td><td>0.00</td><td>0.00</td><td>PbS</td><td>d</td><td>0.286</td><td>0.34–0.37</td></tr><tr><td>InSb</td><td>d</td><td>0.23</td><td>0.17</td><td>PbSe</td><td>i</td><td>0.165</td><td>0.27</td></tr><tr><td>InAs</td><td>d</td><td>0.43</td><td>0.36</td><td>PbTe</td><td>i</td><td>0.190</td><td>0.29</td></tr><tr><td>InP</td><td>d</td><td>1.42</td><td>1.27</td><td>CdS</td><td>d</td><td>2.582</td><td>2.42</td></tr><tr><td>GaP</td><td>i</td><td>2.32</td><td>2.25</td><td>CdSe</td><td>d</td><td>1.840</td><td>1.74</td></tr><tr><td>GaAs</td><td>d</td><td>1.52</td><td>1.43</td><td>CdTe</td><td>d</td><td>1.607</td><td>1.44</td></tr><tr><td>GaSb</td><td>d</td><td>0.81</td><td>0.68</td><td>SnTe</td><td>d</td><td>0.3</td><td>0.18</td></tr><tr><td>AlSb</td><td>i</td><td>1.65</td><td>1.6</td><td>Cu2O</td><td>d</td><td>2.172</td><td>—</td></tr></table>


a HgTe is a semimetal; the bands overlap. 


substantial wavevector $\mathbf { k } _ { c } .$ Here a direct photon transition at the energy of the minimum gap cannot satisfy the requirement of conservation of wavevector, because photon wavevectors are negligible at the energy range of interest. But if a phonon of wavevector K and frequency  is created in the process, then we can have 

$$
\mathbf {k} (\mathrm{photon}) = \mathbf {k} _ {c} + \mathbf {K} \cong \mathbf {0}; \qquad \hbar \omega = E _ {g} + \hbar \Omega ,
$$

as required by the conservation laws. The phonon energy will generally be- much less than $E _ { \mathrm { g } } \mathrm { : }$ a phonon even of high wavevector is an easily accessible source of crystal momentum because the phonon energies are characteristically small (0.01 to 0.03 eV) in comparison with the energy gap. If the temperature is high enough that the necessary phonon is already thermally excited in the crystal, it is possible also to have a photon absorption process in which the phonon is absorbed. 

The band gap may also be deduced from the temperature dependence of the conductivity or of the carrier concentration in the intrinsic range. The carrier concentration is obtained from measurements of the Hall voltage (Chapter 6), sometimes supplemented by conductivity measurements. Optical measurements determine whether the gap is direct or indirect. The band edges in Ge and in Si are connected by indirect transitions; the band edges in InSb and GaAs are connected by a direct transition (Fig. 6). The gap in Sn is direct and is exactly zero; HgTe and HgSe are semimetals and have negative gaps—the conduction and valence bands overlap. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/f46130f5eb5298709d7f2cbf1957115a885512d5f0d0f2a173711717817cfdb2.jpg)



Figure 6 Optical absorption in pure indium antimonide, InSb. The transition is direct because both conduction and valence band edges are at the center of the Brillouin zone, k - 0. Notice the sharp threshold. (After G. W. Gobeli and H. Y. Fan.)


# EQUATIONS OF MOTION

We derive the equation of motion of an electron in an energy band. We look at the motion of a wave packet in an applied electric field. Suppose that the wave packet is made up of wavefunctions assembled near a particular wavevector k. The group velocity by definition is $v _ { \mathrm { g } } = d \omega / d k$ . The frequency associated with a wavefunction of energy  by quantum theory is $\omega = \epsilon / \hbar$ , and so 

$$
v _ {g} = \hbar^ {- 1} d \epsilon / d k \quad \text { or } \quad \mathbf {v} = \hbar^ {- 1} \nabla_ {\mathbf {k}} \epsilon (\mathbf {k}) . \tag {1}
$$

The effects of the crystal on the electron motion are contained in the dispersion relation (k). 

The work  done on the electron by the electric field E in the time interval t is 

$$
\delta \epsilon = - e E v _ {g} \delta t. \tag {2}
$$

We observe that 

$$
\delta \epsilon = (d \epsilon / d k) \delta k = \hbar v _ {g} \delta k, \tag {3}
$$

using (1). On comparing (2) with (3) we have 

$$
\delta k = - (e E / \hbar) \delta t, \tag {4}
$$

whence  -dk/dt - eE. 

We may write (4) in terms of the external force F as 

$$
\hbar \frac {d \mathbf {k}}{d t} = \mathbf {F}. \tag {5}
$$

This is an important relation: in a crystal is equal to the external force-dk/dt on the electron. In free space d(mv)/dt is equal to the force. We have not overthrown Newton’s second law of motion: the electron in the crystal is subject to forces from the crystal lattice as well as from external sources. 

The force term in (5) also includes the electric field and the Lorentz force on an electron in a magnetic field, under ordinary conditions where the magnetic field is not so strong that it breaks down the band structure. Thus the equation of motion of an electron of group velocity v in a constant magnetic field B is 

$$
\hbar \frac {d \mathbf {k}}{d t} = - \frac {e}{c} \mathbf {v} \times \mathbf {B}; \tag {CGS}
$$

$$
\hbar \frac {d \mathbf {k}}{d t} = - e \mathbf {v} \times \mathbf {B} \tag {6}
$$

where the right-hand side of each equation is the Lorentz force on the electron. With the group velocity $\mathbf { v } = \hbar ^ { - 1 } \mathrm { g r a d } _ { \mathbf { k } } \epsilon$ the rate of change of the wavevector is, 

$$
\text {(CGS)} \quad \frac {d \mathbf {k}}{d t} = - \frac {e}{\hbar^ {2} c} \nabla_ {\mathbf {k}} \boldsymbol {\epsilon} \times \mathbf {B};
$$

$$
\text {(SI)} \frac {d \mathbf {k}}{d t} = - \frac {e}{\hbar^ {2}} \nabla_ {\mathbf {k}} \boldsymbol {\epsilon} \times \mathbf {B} \tag {7}
$$

where now both sides of the equation refer to the coordinates in k space. 

We see from the vector cross-product in (7) that in a magnetic field an electron moves in k space in a direction normal to the direction of the gradient of the energy , so that the electron moves on a surface of constant energy. The value of the projection $k _ { \mathbf { B } }$ of k on B is constant during the motion. The motion in k space is on a plane normal to the direction of B, and the orbit is defined by the intersection of this plane with a surface of constant energy. 

## Physical Derivation of $\hbar \dot { \bf k } = { \bf F }$

We consider the Bloch eigenfunction $\psi _ { \mathbf { k } }$ belonging to the energy eigenvalue $\epsilon _ { \mathbf { k } }$ and wavevector k: 

$$
\psi_ {\mathbf {k}} = \sum_ {\mathbf {G}} C (\mathbf {k} + \mathbf {G}) \exp [ i (\mathbf {k} + \mathbf {G}) \cdot \mathbf {r} ] . \tag {8}
$$

The expectation value of the momentum of an electron in the Bloch state k is 

$$
\mathbf {P} _ {\mathrm{el}} = (\mathbf {k} | - i \hbar \nabla | \mathbf {k}) = \sum_ {\mathbf {G}} \hbar (\mathbf {k} + \mathbf {G}) | C (\mathbf {k} + \mathbf {G}) | ^ {2} = \hbar (\mathbf {k} + \sum_ {\mathbf {G}} \mathbf {G} | C (\mathbf {k} + \mathbf {G}) | ^ {2}), \tag {9}
$$

using $\Sigma | C ( \mathbf { k + G } ) | ^ { 2 } = 1$ . 

We examine the transfer of momentum between the electron and the lattice when the state k of the electron is changed to k  
k by the application of an external force. We imagine an insulating crystal electrostatically neutral except for a single electron in the state k of an otherwise empty band. 

We suppose that a weak external force is applied for a time interval such that the total impulse given to the entire crystal system is $\mathbf { J } = \scriptstyle \int \mathbf { F }$ dt. If the conduction electron were free $( m ^ { * } = m )$ , the total momentum imparted to the crystal system by the impulse would appear in the change of momentum of the conduction electron: 

$$
\mathbf {J} = \Delta \mathbf {p} _ {\text { tot }} = \Delta \mathbf {p} _ {\text { el }} = \hbar \Delta \mathbf {k}. \tag {10}
$$

The neutral crystal suffers no net interaction with the electric field, either directly or indirectly through the free electron. 

If the conduction electron interacts with the periodic potential of the crystal lattice, we must have 

$$
\mathbf {J} = \Delta \mathbf {p} _ {\text { tot }} = \Delta \mathbf {p} _ {\text { lat }} + \Delta \mathbf {p} _ {\text { el }}. \tag {11}
$$

From the result (9) for $\bf { p } _ { \mathrm { e l } }$ l we have 

$$
\Delta \mathbf {p} _ {\mathrm{el}} = \hbar \Delta \mathbf {k} + \sum_ {\mathbf {G}} \hbar \mathbf {G} [ (\nabla_ {\mathbf {k}} | C (\mathbf {k} + \mathbf {G}) | ^ {2}) \cdot \Delta \mathbf {k} ]. \tag {12}
$$

The change $\Delta \mathbf { p } _ { \mathrm { l a t } }$ in the lattice momentum resulting from the change of state of the electron may be derived by an elementary physical consideration. An electron reflected by the lattice transfers momentum to the lattice. If an incident electron with plane wave component of momentum is reflected-k with momentum $\hbar ( { \bf k } + { \bf G } )$ the lattice acquires the momentum , $- \hbar \mathbf { G }$ as re-, quired by momentum conservation. The momentum transfer to the lattice when the state $\psi _ { \mathbf { k } }$ goes over to $\psi _ { { \bf k } + \Delta { \bf k } }$ is 

$$
\Delta \mathbf {p} _ {\text { lat }} = - \hbar \sum_ {\mathbf {G}} \mathbf {G} [ (\nabla_ {\mathbf {k}} | C (\mathbf {k} + \mathbf {G}) | ^ {2} \cdot \Delta \mathbf {k} ] , \tag {13}
$$

because the portion 

$$
\nabla_ {\mathbf {k}} \left| C (\mathbf {k} + \mathbf {G}) \right| ^ {2} \cdot \Delta \mathbf {k} \tag {14}
$$

of each individual component of the initial state is reflected during the state change 
k. 

The total momentum change is therefore 

$$
\Delta \mathbf {p} _ {\mathrm{el}} + \Delta \mathbf {p} _ {\mathrm{lat}} = \mathbf {J} = \hbar \Delta \mathbf {k}, \tag {15}
$$

exactly as for free electrons, Eq. (10). Thus from the definition of J, we have 

$$
\hbar d \mathbf {k} / d t = \mathbf {F}, \tag {16}
$$

derived in (5) by a different method. A rigorous derivation of (16) by an entirely different method is given in Appendix E. 


## Holes

The properties of vacant orbitals in an otherwise filled band are important in semiconductor physics and in solid state electronics. Vacant orbitals in a band are commonly called holes, and without holes there would be no transistors. A hole acts in applied electric and magnetic fields as if it has a positive charge e. The reason is given in five steps in the boxes that follow. 

$$
\mathbf {k} _ {h} = - \mathbf {k} _ {e}. \tag {17}
$$

The total wavevector of the electrons in a filled band is zero: $\Sigma \mathbf { k } = 0 ;$ , where the sum is over all states in a Brillouin zone. This result follows from the geometrical symmetry of the Brillouin zone: every fundamental lattice type has symmetry under the inversion operation r→ r about any lattice point; it follows that the Brillouin zone of the lattice also has inversion symmetry. If the band is filled all pairs of orbitals k and k are filled, and the total wavevector is zero. 

If an electron is missing from an orbital of wavevector $\mathbf { k } _ { e } ,$ the total wavevector of the system is $- \mathbf { k } _ { e }$ and is attributed to the hole. This result is surprising: the electron is missing from ${ \bf k } _ { e }$ and the position of the hole is usually indicated graphically as situated at $\mathbf { k } _ { e } ,$ as in Fig. 7. But the true wavevector $\mathbf { k } _ { h }$ of the hole is $- \mathbf { k } _ { e } ,$ which is the wavevector of the point G if the hole is at E. The wavevector $- \mathbf { k } _ { e }$ enters into selection rules for photon absorption. 

The hole is an alternate description of a band with one missing electron, and we either say that the hole has wavevector $- \mathbf { k } _ { e }$ or that the band with one missing electron has total wavevector $- \mathbf { k } _ { e }$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/0f6dbc1655fe1e38ccb00f6160bcf5e77cc20014c0e67e72c61554c5cf49b3ff.jpg)



Figure 7 Absorption of a photon of energy and negligible wavevector takes an electron from-- E in the filled valence band to $Q$ in the conduction band. If $\mathbf { k } _ { e }$ was the wavevector of the electron at $E ,$ it becomes the wavevector of the electron at Q. The total wavevector of the valence band after the absorption is $- \mathbf { k } _ { e } ,$ and this is the wavevector we must ascribe to the hole if we describe the valence band as occupied by one hole. Thus $\mathbf { k } _ { h } = - \mathbf { k } _ { e } ;$ the wavevector of the hole is the same as the wavevector of the electron which remains at G. For the entire system the total wavevector after the absorption of the photon is $\mathbf { k } _ { e } + \mathbf { k } _ { h } = 0 ,$ so that the total wavevector is unchanged by the absorption of the photon and the creation of a free electron and free hole.


$$
\boldsymbol {\epsilon} _ {h} (\mathbf {k} _ {h}) = - \boldsymbol {\epsilon} _ {e} (\mathbf {k} _ {\mathrm{e}}) . \tag {18}
$$

Here the zero of energy of the valence band is at the top of the band. The lower in the band the missing electron lies, the higher the energy of the system. The energy of the hole is opposite in sign to the energy of the missing electron, because it takes more work to remove an electron from a low orbital than from a high orbital. Thus if the band is symmetric $\mathbf { \xi } _ { , } ^ { 1 } \ \epsilon _ { e } ( \mathbf { k } _ { e } ) = \epsilon _ { e } ( - \mathbf { k } _ { e } ) = \ - \epsilon _ { h } ( - \mathbf { k } _ { e } ) = \ - \epsilon _ { h } ( \mathbf { k } _ { h } )$ . We construct in Fig. 8 a band scheme to represent the properties of a hole. This hole band is a helpful representation because it appears right side up. 

$$
\mathbf {v} _ {h} = \mathbf {v} _ {e}. \tag {19}
$$

The velocity of the hole is equal to the velocity of the missing electron. From Fig. 8 we see that $\nabla \epsilon _ { h } ( { \pmb k } _ { h } ) = \nabla \epsilon _ { e } ( { \pmb k } _ { e } )$ so that, ${ \pmb v } _ { h } ( { \pmb k } _ { h } ) = { \pmb v } _ { e } ( { \pmb k } _ { e } )$ . 

1 Bands are always symmetric under the inversion k → k if the spin-orbit interaction is neglected. Even with spin-orbit interaction, bands are always symmetric if the crystal structure permits the inversion operation. Without a center of symmetry, but with spin-orbit interaction, the bands are symmetric if we compare subbands for which the spin direction is reversed: (k, ↑) - (k, ↓). See QTS, Chapter 9. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/d3a033f7b66966af57bd996dd5b33f21d8aa8a2b851ccefbe6a71a36212f6438.jpg)



Figure 8 The upper half of the figure shows the hole band that simulates the dynamics of a hole, constructed by inversion of the valence band in the origin. The wavevector and energy of the hole are equal, but opposite in sign, to the wavevector and energy of the empty electron orbital in the valence band. We do not show the disposition of the electron removed from the valence band at $\mathbf { k } _ { e } .$ .


4. $m _ { h } = - m _ { e } ~ .$ (20) 

We show below that the effective mass is inversely proportional to the curvature $d ^ { 2 } { \epsilon } / d k ^ { 2 } .$ and for the hole band this has the opposite sign to that for an electron in the valence band. Near the top of the valence band $m _ { e }$ is negative, so that $m _ { h }$ is positive. 

5. $\hbar { \frac { d \mathbf { k } _ { h } } { d t } } = e ( \mathbf { E } + { \frac { 1 } { c } } \mathbf { v } _ { h } \times \mathbf { B } ) \ .$ (21) 

This comes from the equation of motion 

(CGS) $\hbar \frac { d \mathbf { k } _ { e } } { d t } = - e ( \mathbf { E _ { \alpha } } + \frac { 1 } { c } \mathbf { v _ { e } } \times \mathbf { B } )$ (22) 

that applies to the missing electron when we substitute $- \mathbf { k } _ { h }$ for ${ \bf k } _ { e }$ and $\mathbf { v } _ { h }$ for $\mathbf { v } _ { e } .$ The equation of motion for a hole is that of a particle of positive charge e. The positive charge is consistent with the electric current carried by the valence band of Fig. 9: the current is carried by the unpaired electron in the orbital G: 

$$
\mathbf {j} = (- e) \mathbf {v} (G) = (- e) [ - \mathbf {v} (E) ] = e \mathbf {v} (E), \tag {23}
$$

which is just the current of a positive charge moving with the velocity ascribed to the missing electron at E. The current is shown in Fig. 10. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/b9084ed3bac1f43565caeac11fa20d7451bb213e1390c2d0f4a275835440e875.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/b76f977025abcc4f35a73ce98fde4385caf5a5b4cf2bd1eefcc64faa2a510252.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/8a88d8e296338c934d118049d46dce5f3078c9168864f7386940592e303f2481.jpg)



Figure 9 (a) $\mathbf { A } \mathbf { t } t = 0$ all states are filled except F at the top of the band; the velocity $v _ { x }$ is zero at F because $d \epsilon / d k _ { x } = 0 .$ (b) An electric field $E _ { x }$ is applied in the x direction. The force on the electrons is in the kx direction and all electrons make transitions together in the $- k _ { x }$ x direction, moving the hole to the state E. (c) After a further interval the electrons move farther along in k space and the hole is now at D.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/418679354c2ceb18d99210241b2dc0ae6b16ea3caa7b1d21233e75a43056db90.jpg)



Figure 10 Motion of electrons in the conduction band and holes in the valence band in the electric field E. The hole and electron drift velocities are in opposite directions, but their electric currents are in the same direction, the direction of the electric field.


## Effective Mass

When we look at the energy-wavevector relation $\epsilon = ( \hbar ^ { 2 } / 2 m ) k ^ { 2 }$ for free electrons, we see that the coefficient of $k ^ { 2 }$ determines the curvature of  versus k. Turned about, we can say that 1/m, the reciprocal mass, determines the curvature. For electrons in a band there can be regions of unusually high curvature near the band gap at the zone boundary, as we see from the solutions in Chapter 7 of the wave equation near the zone boundary. If the energy gap is small in comparison with the free electron energy  at the boundary, the curvature is enhanced by the factor $\lambda / E _ { \mathrm { g } } .$ . 

In semiconductors the band width, which is like the free electron energy, is of the order of 20 eV, while the band gap is of the order of 0.2 to $2 \ \mathrm { e V } .$ Thus the reciprocal mass is enhanced by a factor 10 to 100, and the effective mass is reduced to 0.1–0.01 of the free electron mass. These values apply near the band gap; as we go away from the gap the curvatures and the masses are likely to approach those of free electrons. 

To summarize the solutions of Chapter 7 for U positive, an electron near the lower edge of the second band has an energy that may be written as 

$$
\epsilon (K) = \epsilon_ {c} + (\hbar^ {2} / 2 m _ {e}) K ^ {2}; \quad m _ {e} / m = 1 / [ (2 \lambda / U) - 1 ]. \tag {24}
$$

Here K is the wavevector measured from the zone boundary, and $m _ { e }$ denotes the effective mass of the electron near the edge of the second band. An electron near the top of the first band has the energy 

$$
\epsilon (K) = \epsilon_ {v} - (\hbar^ {2} / 2 m _ {h}) K ^ {2}; \quad m _ {h} / m = 1 / [ (2 \lambda / U) + 1 ]. \tag {25}
$$

The curvature and hence the mass will be negative near the top of the first band, but we have introduced a minus sign into (25) in order that the symbol $m _ { h }$ for the hole mass will have a positive value—see (20) above. 

The crystal does not weigh any less if the effective mass of a carrier is less than the free electron mass, nor is Newton’s second law violated for the crystal taken as a whole, ions plus carriers. The important point is that an electron in a periodic potential is accelerated relative to the lattice in an applied electric or magnetic field as if the mass of the electron were equal to an effective mass which we now define. 

We differentiate the result (1) for the group velocity to obtain 

$$
\frac {d v _ {g}}{d t} = \hbar^ {- 1} \frac {d ^ {2} \epsilon}{d k d t} = \hbar^ {- 1} \left(\frac {d ^ {2} \epsilon}{d k ^ {2}} \frac {d k}{d t}\right). \tag {26}
$$

We know from (5) that $d k / d t = F / \hbar$ whence, 

$$
\frac {d v _ {g}}{d t} = \left(\frac {1}{\hbar^ {2}} \frac {d ^ {2} \epsilon}{d k ^ {2}}\right) F; \quad \text { or } \quad F = \frac {\hbar^ {2}}{d ^ {2} \epsilon / d k ^ {2}} \frac {d v _ {g}}{d t}. \tag {27}
$$

If we identify $\hbar ^ { 2 } / ( d ^ { 2 } \epsilon / d k ^ { 2 } )$ as a mass, then (27) assumes the form of Newton’s second law. We define the effective mass $m ^ { * }$ by 

$$
\boxed {\frac {1}{m ^ {*}} = \frac {1}{\hbar^ {2}} \frac {d ^ {2} \epsilon}{d k ^ {2}}.} \tag {28}
$$

It is easy to generalize this to take account of an anisotropic electron energy surface, as for electrons in Si or Ge. We introduce the components of the reciprocal effective mass tensor 

$$
\left(\frac {1}{m ^ {*}}\right) _ {\mu \nu} = \frac {1}{\hbar^ {2}} \frac {d ^ {2} \epsilon_ {k}}{d k _ {\mu} d k _ {\nu}}; \quad \frac {d v _ {\mu}}{d t} = \left(\frac {1}{m ^ {*}}\right) _ {\mu \nu} F _ {\nu}, \tag {29}
$$

where , 	 are Cartesian coordinates. 

## Physical Interpretation of the Effective Mass

How can an electron of mass m when put into a crystal respond to applied fields as if the mass were $m ^ { * } ?$ It is helpful to think of the process of Bragg reflection of electron waves in a lattice. Consider the weak interaction approximation treated in Chapter 7. Near the bottom of the lower band the orbital is represented quite adequately by a plane wave exp(ikx) with momentum  -k; the wave component $\exp [ i ( k - G ) x ]$ with momentum $\hbar ( k { - } G )$ is small and increases only slowly as $k$ is increased, and in this region $m ^ { * } \simeq m$ . An increase in the reflected component $\exp [ i ( k - G ) x ]$ as $k$ is increased represents momentum transfer to the electron from the lattice. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/35e224d23e9033bd9778f973f5743d4235e7edf74936097b72fae52f15c481f8.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/bdef987e2dabcc5ef2a7243a1f579892a0e4c08e37f72f29b17201659df4b685.jpg)



Figure 11 Explanation of negative effective masses which occur near, but below, a Brillouin zone boundary. In (a) the energy of the electron beam incident on a thin crystal is slightly too low to satisfy the condition for Bragg reflection and the beam is transmitted through the crystal. The application of a small voltage across the grid may, as in (b), cause the Bragg condition to be satisfied, and the electron beam will then be reflected from the appropriate set of crystal planes.


Near the boundary the reflected component is quite large; at the boundary it becomes equal in amplitude to the forward component, at which point the eigenfunctions are standing waves, rather than running waves. Here the momentum component $\textstyle \hbar ( - { \frac { 1 } { 2 } } G )$ cancels the momentum component $\hbar ( { \frac { 1 } { 2 } } G )$ . 

A single electron in an energy band may have positive or negative effective mass: the states of positive effective mass occur near the bottom of a band because positive effective mass means that the band has upward curvature $( d ^ { 2 } \epsilon / d k ^ { 2 }$ is positive). States of negative effective mass occur near the top of the band. A negative effective mass means that on going from state $k$ to state $k + \Delta k$ , the momentum transfer to the lattice from the electron is larger than the momentum transfer from the applied force to the electron. Although k is increased by $\Delta k$ by the applied electric field, the approach to Bragg reflection can give an overall decrease in the forward momentum of the electron; when this happens the effective mass is negative (Fig. 11). 

As we proceed in the second band away from the boundary, the amplitude of $\exp [ i ( k - G ) x ]$ decreases rapidly and $m ^ { * }$ assumes a small positive value. Here the increase in electron velocity resulting from a given external impulse is larger than that which a free electron would experience. The lattice makes up the difference through the reduced recoil it experiences when the amplitude of $\exp [ i ( k - G ) x ]$ is diminished. 

If the energy in a band depends only slightly on $k ,$ then the effective mass will be very large. That is, $m ^ { * } / m \gg 1$ when $d ^ { 2 } { \epsilon } / d k ^ { 2 }$ is very small. The tightbinding approximation discussed in Chapter 9 gives quick insight into the formation of narrow bands. If the wavefunctions centered on neighboring atoms overlap very little, then the overlap integral is small; the width of the band narrow, and the effective mass large. The overlap of wavefunctions centered on neighboring atoms is small for the inner or core electrons. The 4f electrons of the rare earth metals, for example, overlap very little. 

## Effective Masses in Semiconductors

In many semiconductors it has been possible to determine by cyclotron resonance the effective masses of carriers in the conduction and valence bands near the band edges. The determination of the energy surface is equivalent to a determination of the effective mass tensor (29). Cyclotron resonance in a semiconductor is carried out with centimeter wave or millimeter wave radiation at low carrier concentration. 

The current carriers are accelerated in helical orbits about the axis of a static magnetic field. The angular rotation frequency $\omega _ { c }$ is 

$$
\text {(CGS)} \quad \omega_ {c} = \frac {e B}{m ^ {*} c}, \quad \boxed {\text {(SI)} \quad \omega_ {c} = \frac {e B}{m ^ {*}}} \tag {30}
$$

where $m ^ { * }$ is the appropriate cyclotron effective mass. Resonant absorption of energy from an rf electric field perpendicular to the static magnetic field (Fig. 12) occurs when the rf frequency is equal to the cyclotron frequency. Holes and electrons rotate in opposite senses in a magnetic field. 

We consider the experiment for $m ^ { * } / m = 0 . 1$ . At $f _ { c } = 2 4$ GHz, or $\omega _ { c } =$ $1 . 5 \times 1 0 ^ { 1 1 } \mathrm { s ^ { - 1 } }$ , we have $B = 8 6 0 \mathrm { ~ G ~ }$ at resonance. The line width is determined by the collision relaxation time 
, and to obtain a distinctive resonance it is necessary that $\omega _ { c } \tau \geq 1$ . The mean free path must be long enough to permit the average carrier to get one radian around a circle between collisions. The requirements are met with the use of higher frequency radiation and higher magnetic fields, with high purity crystals in liquid helium. 

In direct-gap semiconductors with band edges at the center of the Brillouin zone, the bands have the structure shown in Fig. 13. The conduction band edge is spherical with the effective mass $m _ { 0 } { : }$ 

$$
\epsilon_ {c} = E _ {g} + \hbar^ {2} k ^ {2} / 2 m _ {e}, \tag {31}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/f40e78e451db5a71c57dd3b7aebce129615ba0ee4777b45239fd11c4e24a0071.jpg)



Figure 12 Arrangement of fields in a cyclotron resonance experiment in a semiconductor. The sense of the circulation is opposite for electrons and holes.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/8b74c9d6e5065a7eaac741c10d31e001c5c77ce9e3b54128e9521b42884451af.jpg)



Figure 13 Simplified view of the band edge structure of a direct-gap semiconductor.



Table 2 Effective masses of electrons and holes in direct-gap semiconductors


<table><tr><td>Crystal</td><td>Electron <eq>m_e/m</eq></td><td>Heavy hole <eq>m_{hh}/m</eq></td><td>Light hole <eq>m_{lh}/m</eq></td><td>Split-off hole <eq>m_{soh}/m</eq></td><td>Spin-orbit <eq>\Delta</eq>, eV</td></tr><tr><td>InSb</td><td>0.015</td><td>0.39</td><td>0.021</td><td>(0.11)</td><td>0.82</td></tr><tr><td>InAs</td><td>0.026</td><td>0.41</td><td>0.025</td><td>0.08</td><td>0.43</td></tr><tr><td>InP</td><td>0.073</td><td>0.4</td><td>(0.078)</td><td>(0.15)</td><td>0.11</td></tr><tr><td>GaSb</td><td>0.047</td><td>0.3</td><td>0.06</td><td>(0.14)</td><td>0.80</td></tr><tr><td>GaAs</td><td>0.066</td><td>0.5</td><td>0.082</td><td>0.17</td><td>0.34</td></tr><tr><td><eq>Cu_2O</eq></td><td>0.99</td><td>—</td><td>0.58</td><td>0.69</td><td>0.13</td></tr></table>

referred to the valence band edge. The valence bands are characteristically threefold near the edge, with the heavy hole hh and light hole lh bands degenerate at the center, and a band soh split off by the spin-orbit splitting 
: 

$$
\begin{array}{l} \epsilon_ {v} (h h) \cong - \hbar^ {2} k ^ {2} / 2 m _ {h h}; \quad \epsilon_ {v} (l h) \cong - \hbar^ {2} k ^ {2} / 2 m _ {l h}; \\ \epsilon_ {v} (s o h) \cong - \Delta - \hbar^ {2} k ^ {2} / 2 m _ {s o h}. \tag {32} \\ \end{array}
$$

Values of the mass parameters are given in Table 2. The forms (32) are only approximate, because even close to $k = 0$ the heavy and light hole bands are not spherical—see the discussion below for Ge and Si. 

The perturbation theory of band edges (Problem 9.8) suggests that the electron effective mass should be proportional to the band gap, approximately, for a direct gap crystal. We use Tables 1 and 2 to find the fairly constant values $m _ { e } / ( m E _ { g } ) = 0 . 0 6 3 , \ 0 . 0 6 0$ , and 0.051 in $( \mathrm { e V } ) ^ { - 1 }$ for the series InSb, InAs, and InP, in agreement with this suggestion. 

## Silicon and Germanium

The conduction and valence bands of germanium are shown in Fig. 14, based on a combination of theoretical and experimental results. The valence band edge in both Si and Ge is at $\mathbf k = 0$ and is derived from $p _ { 3 / 2 }$ and $p _ { 1 / 2 }$ states of the free atoms, as is clear from the tight-binding approximation (Chapter 9) to the wavefunctions. 

The $p _ { 3 / 2 }$ level is fourfold degenerate as in the atom; the four states correspond to $m _ { J }$ values $\pm \ : \frac { 3 } { 2 }$ and $\pm { \frac { 1 } { 2 } } .$ The. $p _ { 1 / 2 }$ level is doubly degenerate, with $\begin{array} { r } { m _ { J } = \pm \frac { 1 } { 2 } . } \end{array}$ The. $p _ { 3 / 2 }$ states are higher in energy than the $p _ { 1 / 2 }$ states; the energy difference 
 is a measure of the spin-orbit interaction. 

The valence band edges are not simple. Holes near the band edge are characterized by two effective masses, light and heavy. These arise from the two bands formed from the $p _ { 3 / 2 }$ level of the atom. There is also a band formed from the $p _ { 1 / 2 }$ level, split off from the $p _ { 3 / 2 }$ level by the spin-orbit interaction. The energy surfaces are not spherical, but warped (QTS, p. 271): 

$$
\epsilon (\mathbf {k}) = A k ^ {2} \pm \left[ B ^ {2} k ^ {4} + C ^ {2} (k _ {x} ^ {2} k _ {y} ^ {2} + k _ {y} ^ {2} k _ {z} ^ {2} + k _ {z} ^ {2} k _ {x} ^ {2}) \right] ^ {1 / 2} \tag {33}
$$

The choice of sign distinguishes the two masses. The split-off band has $\epsilon ( k ) = - \Delta + A k ^ { 2 }$ . The experiments give, in units $\hbar ^ { 2 } / 2 m$ , 

Roughly, the light and heavy holes in germanium have masses 0.043 m and 0.34 m; in silicon 0.16 m and 0.52 m; in diamond 0.7 m and 2.12 m. 

The conduction band edges in Ge are at the equivalent points L of the Brillouin zone, Fig. 15a. Each band edge has a spheroidal energy surface oriented along a 111 crystal axis, with a longitudinal mass $m _ { l } = 1 . 5 9$ m and a transverse mass $m _ { t } = 0 . 0 8 2 \ m$ . For a static magnetic field at an angle  with the longitudinal axis of a spheroid, the effective cyclotron mass $m _ { c }$ is 

$$
\frac {1}{m _ {c} ^ {2}} = \frac {\cos^ {2} \theta}{m _ {t} ^ {2}} + \frac {\sin^ {2} \theta}{m _ {t} m _ {l}} \tag {34}
$$

Results for Ge are shown in Fig. 16. 

In silicon the conduction band edges are spheroids oriented along the equivalent 100 directions in the Brillouin zone, with mass parameters $m _ { l } = 0 . 9 2$ m and $m _ { t } = 0 . 1 9 m$ , as in Fig. 17a. The band edges lie along the lines labeled 
 in the zone of Fig. 15a, a little way in from the boundary points X. 

In GaAs we have $A = - 6 . 9 8 , \ B = - 4 . 5 , \ | C | = 6 . 2 , \ \Delta = 0 . 3 4 1 \ \mathrm { e V } .$ The band structure is shown in Fig. 17b. It has a direct band gap with an isotropic conduction electron mass of 0.067 m. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/38533df85c3350a2d7284f841f96f51e55ee99e597faed36f4fc352d96301f2e.jpg)



Figure 14 Calculated band structure of germanium, after C. Y. Fong. The general features are in good agreement with experiment. The four valence bands are shown in gray. The fine structure of the valence band edge is caused by spin-orbit splitting. The energy gap is indirect; the conduction band edge is at the point The constant energy surfaces around this point are ellipsoidal. (2a)(12 12 12).


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/b1872c9dc21663d57124d8f413089834060e80feb4e5bcc873ae72f70014cf2a.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/9855d1947be7dec18284e5b65d945303bf6e05112534bb633657e1270fec25d0.jpg)



Figure 15 Standard labels of the symmetry points and axes of the Brillouin zones of the fcc and bcc lattices. The zone centers are . In (a) the boundary point at (2/a)(100) is X; the boundary point at is L; the line 
 runs between  and X. In (b) the corresponding symbols are(2/a)(12 12 12) H, P, and 
.



Figure 16 Effective cyclotron mass of electrons in germanium at 4 K for magnetic field directions in a (110) plane. There are four independent mass spheroids in Ge, one along each [111] axis, but viewed in the (110) plane two spheroids always appear equivalent. (After Dresselhaus, Kip, and Kittel.)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/098e74ae16b397dd96d87025377ccc08b6c4efac3b773a4d45d283144cc5b30f.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/91ae8946ec75b97ccbb81212f3d1d1d291573c2d22bc1734cdc4c5256292f441.jpg)



Figure 17a Constant energy ellipsoids for electrons in silicon, drawn for $m _ { l } / \bar { m } _ { t } = 5$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/31f8947eb86cfbe2f98a4d263d95c6e694ae0cd9ba06d01f7f93da71a9d2e291.jpg)



Figure 17b Band structure of GaAs, after S. G. Louie.


# INTRINSIC CARRIER CONCENTRATION

We want the concentration of intrinsic carriers as a function of temperature, in terms of the band gap. We do the calculation for simple parabolic band edges. We first calculate in terms of the chemical potential $\mu$ the number of electrons excited to the conduction band at temperature $T .$ In semiconductor physics $\mu$ is called the Fermi level. At the temperatures of interest we may suppose for the conduction band of a semiconductor that $\epsilon - \mu \gg k _ { B } T$ , so that the Fermi-Dirac distribution function reduces to 

$$
f _ {e} \simeq \exp [ (\mu - \epsilon) / k _ {B} T ]. \tag {35}
$$

This is the probability that a conduction electron orbital is occupied, in an approximation valid when $f _ { e } \ll 1$ . 

The energy of an electron in the conduction band is 

$$
\epsilon_ {k} = E _ {c} + \hbar^ {2} k ^ {2} / 2 m _ {e}, \tag {36}
$$

where $E _ { c }$ is the energy at the conduction band edge, as in Fig. 18. Here $m _ { e }$ is the effective mass of an electron. Thus from (6.20) the density of states at  is 

$$
D _ {e} (\epsilon) = \frac {1}{2 \pi^ {2}} \left(\frac {2 m _ {e}}{\hbar^ {2}}\right) ^ {3 / 2} (\epsilon - E _ {c}) ^ {1 / 2}. \tag {37}
$$

The concentration of electrons in the conduction band is 

$$
\begin{array}{l} n = \int_ {E _ {c}} ^ {\infty} D _ {e} (\epsilon) f _ {e} (\epsilon) d \epsilon = \frac {1}{2 \pi^ {2}} \left(\frac {2 m _ {e}}{\hbar^ {2}}\right) ^ {3 / 2} \exp \left(\mu / k _ {B} T\right) \times \tag {38} \\ \int_ {E _ {c}} ^ {\infty} (\epsilon - E _ {c}) ^ {1 / 2} \exp (- \epsilon / k _ {B} T) d \epsilon , \\ \end{array}
$$

which integrates to give 

$$
n = 2 \left(\frac {m _ {e} k _ {B} T}{2 \pi \hbar^ {2}}\right) ^ {3 / 2} \exp [ (\mu - E _ {c}) / k _ {B} T ]. \tag {39}
$$

The problem is solved for n when $\mu$ is known. It is useful to calculate the equilibrium concentration of holes $p .$ The distribution function $f _ { h }$ for holes is related to the electron distribution function $f _ { e }$ by $f _ { h } = 1 - f _ { e } ,$ because a hole is the absence of an electron. We have 

$$
f _ {h} = 1 - \frac {1}{\exp [ (\epsilon - \mu) / k _ {B} T ] + 1} = \frac {1}{\exp [ (\mu - \epsilon) / k _ {B} T ] + 1} \tag {40}
$$

$$
\cong \exp [ (\epsilon - \mu) / k _ {B} T ],
$$

provided $( \mu - \epsilon ) \gg k _ { B } T .$ . 

If the holes near the top of the valence band behave as particles with effective mass $m _ { h } .$ the density of hole states is given by 

$$
D _ {h} (\epsilon) = \frac {1}{2 \pi^ {2}} \left(\frac {2 m _ {h}}{\hbar^ {2}}\right) ^ {3 / 2} (E _ {v} - \epsilon) ^ {1 / 2}, \tag {41}
$$

where $E _ { \upsilon }$ is the energy at the valence band edge. Proceeding as in (38) we obtain 

$$
p = \int_ {- \infty} ^ {E _ {c}} D _ {h} (\epsilon) f _ {h} (\epsilon) d \epsilon = 2 \left(\frac {m _ {h} k _ {B} T}{2 \pi \hbar^ {2}}\right) ^ {3 / 2} \exp [ (E _ {c} - \mu) / k _ {B} T ] \tag {42}
$$

for the concentration p of holes in the valence band. 

We multiply together the expressions for n and $p$ to obtain the equilibrium relation, with the energy gap $E _ { \mathrm { g } } = E _ { c } - E _ { v }$ as in Fig. 18, 

$$
n p = 4 \left(\frac {k _ {B} T}{2 \pi \hbar^ {2}}\right) ^ {3} (m _ {c} m _ {h}) ^ {3 / 2} \exp (- E _ {\mathrm{g}} / k _ {B} T). \tag {43}
$$

This useful result does not involve the Fermi level . At 300 K the value of np is $\mathrm { 2 . 1 0 \times 1 0 ^ { 1 9 } ~ c m ^ { - 6 } , ~ 2 . 8 9 \times 1 0 ^ { 2 6 } ~ c m ^ { - 6 } }$ , and $6 . 5 5 \times 1 0 ^ { 1 2 } ~ \mathrm { { c m } ^ { - 6 } }$ , for the actual band structures of Si, Ge, and GaAs, respectively. 

We have nowhere assumed in the derivation that the material is intrinsic: the result holds for impurity ionization as well. The only assumption made is that the distance of the Fermi level from the edge of both bands is large in comparison with $k _ { B } T$ . 

A simple kinetic argument shows why the product np is constant at a given temperature. Suppose that the equilibrium population of electrons and holes is maintained by black-body photon radiation at temperature T. The photons generate electron-hole pairs at a rate $A ( T )$ , while $B ( T ) n p$ is the rate of the recombination reaction $e + h = \mathrm { p h o t o n }$ . Then 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/362658ce315c2ce5a34596ff810c1374db79086dc317932ab94689585ed19fce.jpg)



Figure 18 Energy scale for statistical calculations. The Fermi distribution function is shown on the same scale, for a temperature $k _ { B } T \ll E _ { \mathrm { g } } .$ The Fermi level $\mu$ is taken to lie well within the band gap, as for an intrinsic semiconductor. If $\epsilon = \mu ,$ , then $\begin{array} { r } { f = \frac { 1 } { 2 } } \end{array}$ .


$$
d n / d t = A (T) - B (T) n p = d p / d t \quad . \tag {44}
$$

In equilibrium ${ d n } / { d t } = 0 , { d p } / { d t } = 0$ , whence $n p = A ( T ) / B ( T )$ . 

Because the product of the electron and hole concentrations is a constant independent of impurity concentration at a given temperature, the introduction of a small proportion of a suitable impurity to increase n, say, must decrease p. This result is important in practice—we can reduce the total carrier concentration $n + p$ in an impure crystal, sometimes enormously, by the controlled introduction of suitable impurities. Such a reduction is called compensation. 

In an intrinsic semiconductor the number of electrons is equal to the number of holes, because the thermal excitation of an electron leaves behind a hole in the valence band. Thus from (43) we have, letting the subscript i denote intrinsic and $E _ { \mathrm { g } } = E _ { c } - E _ { v }$ , 

$$
n _ {i} = p _ {i} = 2 \left(\frac {k _ {B} T}{2 \pi \hbar^ {2}}\right) ^ {3 / 2} (m _ {e} m _ {h}) ^ {3 / 4} \exp (- E _ {g} / 2 k _ {B} T). \tag {45}
$$

The intrinsic carrier concentration depends exponentially on $E _ { \mathrm { g } } / 2 k _ { B } T$ , where $E _ { \mathrm { g } }$ is the energy gap. We set (39) equal to (42) to obtain, for the Fermi level as measured from the top of the valence band, 

$$
\exp (2 \mu / k _ {B} T) = (m _ {h} / m _ {e}) ^ {3 / 2} \exp (E _ {g} / k _ {B} T); \tag {46}
$$

$$
\mu = \frac {1}{2} E _ {g} + \frac {3}{4} k _ {B} T \ln \left(m _ {h} / m _ {e}\right). \tag {47}
$$

If $m _ { h } = m _ { e } ,$ then $\begin{array} { r } { \mu = \frac { 1 } { 2 } E _ { \mathrm { g } } } \end{array}$ and the Fermi level is in the middle of the forbidden gap. 

## Intrinsic Mobility

The mobility is the magnitude of the drift velocity of a charge carrier per unit electric field: 

$$
\mu = | v | / E. \tag {48}
$$

The mobility is defined to be positive for both electrons and holes, although their drift velocities are opposite in a given field. By writing $\mu _ { e }$ or $\mu _ { h }$ with subscripts for the electron or hole mobility we can avoid any confusion between $\mu$ as the chemical potential and as the mobility. 

The electrical conductivity is the sum of the electron and hole contributions: 

$$
\sigma = \left(n e \mu_ {e} + p e \mu_ {h}\right), \tag {49}
$$

where n and $p$ are the concentrations of electrons and holes. In Chapter 6 the drift velocity of a charge q was found to be $v = q \tau E / m .$ , whence 

$$
\mu_ {e} = e \tau_ {e} / m _ {e}; \quad \mu_ {h} = e \tau_ {h} / m _ {h}, \tag {50}
$$

where 
 is the collision time. 

The mobilities depend on temperature as a modest power law. The temperature dependence of the conductivity in the intrinsic region will be dominated by the exponential dependence exp $\ d _ { \mathrm { \Omega } } ( - E _ { \mathrm { g } } / 2 k _ { B } T )$ of the carrier concentration, Eq. (45). 

Table 3 gives experimental values of the mobility at room temperature. The mobility in SI units is expressed in m $^ 2 / \mathrm { V } { - } \mathrm { S }$ and is $1 0 ^ { - 4 }$ of the mobility in practical units. For most substances the values quoted are limited by the scattering of carriers by thermal phonons. The hole mobilities typically are smaller than the electron mobilities because of the occurrence of band degeneracy at the valence band edge at the zone center, thereby making possible interband scattering processes that reduce the mobility considerably. 


Table 3 Carrier mobilities at room temperature, in $\mathbf { c m ^ { 2 } / V { - } s }$


<table><tr><td>Crystal</td><td>Electrons</td><td>Holes</td><td>Crystal</td><td>Electrons</td><td>Holes</td></tr><tr><td>Diamond</td><td>1800</td><td>1200</td><td>GaAs</td><td>8000</td><td>300</td></tr><tr><td>Si</td><td>1350</td><td>480</td><td>GaSb</td><td>5000</td><td>1000</td></tr><tr><td>Ge</td><td>3600</td><td>1800</td><td>PbS</td><td>550</td><td>600</td></tr><tr><td>InSb</td><td>800</td><td>450</td><td>PbSe</td><td>1020</td><td>930</td></tr><tr><td>InAs</td><td>30000</td><td>450</td><td>PbTe</td><td>2500</td><td>1000</td></tr><tr><td>InP</td><td>4500</td><td>100</td><td>AgCl</td><td>50</td><td>—</td></tr><tr><td>AlAs</td><td>280</td><td>—</td><td>KBr (100 K)</td><td>100</td><td>—</td></tr><tr><td>AlSb</td><td>900</td><td>400</td><td>SiC</td><td>100</td><td>10–20</td></tr></table>

In some crystals, particularly in ionic crystals, the holes are essentially immobile and get about only by thermally-activated hopping from ion to ion. The principal cause of this “self-trapping” is the lattice distortion associated with the Jahn-Teller effect of degenerate states. The orbital degeneracy necessary for self-trapping is much more frequent for holes than for electrons. 

There is a tendency for crystals with small energy gaps at direct band edges to have high values of the electron mobility. Small gaps lead to small effective masses, which favor high mobilities. The highest mobility observed in a bulk semiconductor is $5 \times 1 0 ^ { 6 } \mathrm { c m ^ { 2 } / V { - } s }$ in PbTe at 4 K, where the gap is 0.19 eV. 

# IMPURITY CONDUCTIVITY

Certain impurities and imperfections drastically affect the electrical properties of a semiconductor. The addition of boron to silicon in the proportion of 1 boron atom to $1 0 ^ { 5 }$ silicon atoms increases the conductivity of pure silicon at room temperature by a factor of $1 0 ^ { 3 }$ . In a compound semiconductor a stoichiometric deficiency of one constituent will act as an impurity; such semiconductors are known as deficit semiconductors. The deliberate addition of impurities to a semiconductor is called doping. 

We consider the effect of impurities in silicon and germanium. These elements crystallize in the diamond structure. Each atom forms four covalent bonds, one with each of its nearest neighbors, corresponding to the chemical valence four. If an impurity atom of valence five, such as phosphorus, arsenic, or antimony, is substituted in the lattice in place of a normal atom, there will be one valence electron from the impurity atom left over after the four covalent bonds are established with the nearest neighbors, that is, after the impurity atom has been accommodated in the structure with as little disturbance as possible. Impurity atoms that can give up an electron are called donors. 

Donor States. The structure in Fig. 19 has a positive charge on the impurity atom (which has lost one electron). Lattice constant studies have verified that the pentavalent impurities enter the lattice by substitution for normal atoms, and not in interstitial positions. The crystal as a whole remains neutral because the electron remains in the crystal. 

The extra electron moves in the coulomb potential e/r of the impurity ion, where  in a covalent crystal is the static dielectric constant of the medium. The factor 1/ takes account of the reduction in the coulomb force between charges caused by the electronic polarization of the medium. This treatment is valid for orbits large in comparison with the distance between atoms, and for slow motions of the electron such that the orbital frequency is low in comparison with the frequency $\omega _ { \mathrm { g } }$ corresponding to the energy gap. These conditions are satisfied quite well in Ge and Si by the donor electron of P, As, or Sb. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/e56d9ab753fa8ba06d41abba5517d5560a3a925a7f7e0748a85888599c811e11.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/368e6f5d141adb5b200d57a7fd23ff7e857b429bc26a0e80d2a54d65cb121e3e.jpg)



Figure 19 Charges associated with an arsenic impurity atom in silicon. Arsenic has five valence electrons, but silicon has only four valence electrons. Thus four electrons on the arsenic form tetrahedral covalent bonds similar to silicon, and the fifth electron is available for conduction. The arsenic atom is called a donor because when ionized it donates an electron to the conduction band.


We estimate the ionization energy of the donor impurity. The Bohr theory of the hydrogen atom may be modified to take into account the dielectric constant of the medium and the effective mass of an electron in the periodic potential of the crystal. The ionization energy of atomic hydrogen is $- e ^ { 4 } m / 2 \hbar ^ { 2 }$ in CGS and $- e ^ { 4 } m / 2 ( 4 \pi \epsilon _ { 0 } \hbar ) ^ { 2 }$ in SI. 

In the semiconductor with dielectric constant  we replace $e ^ { 2 }$ by $e ^ { 2 } / \epsilon$ and m by the effective mass $m _ { e }$ to obtain 

$$
\text {(CGS)} \quad E _ {d} = \frac {e ^ {4} m _ {e}}{2 \epsilon^ {2} \hbar^ {2}} = \left(\frac {1 3 . 6}{\epsilon^ {2}} \frac {m _ {e}}{m}\right) e V; \quad \text {(SI)} E _ {d} = \frac {e ^ {4} m _ {e}}{2 (4 \pi \epsilon \epsilon_ {0} \hbar) ^ {2}} \tag {51}
$$

as the donor ionization energy of the semiconductor. 

The Bohr radius of the ground state of hydrogen is $\hbar ^ { 2 } / m e ^ { 2 }$ in CGS or $4 \pi \epsilon _ { 0 } \hbar ^ { 2 } / m e ^ { 2 }$ in SI. Thus the Bohr radius of the donor is 

$$
\text {(CGS)} a _ {d} = \frac {\epsilon \hbar^ {2}}{m _ {e} e ^ {2}} = \left(\frac {0 . 5 3 \epsilon}{m _ {e} / m}\right) \mathring {\mathrm{A}}; \quad \text {(SI)} a _ {d} = \frac {4 \pi \epsilon \epsilon_ {0} \hbar^ {2}}{m _ {e} e ^ {2}} \tag {52}
$$

The application of impurity state theory to germanium and silicon is complicated by the anisotropic effective mass of the conduction electrons. But the dielectric constant has the more important effect on the donor energy because it enters as the square, whereas the effective mass enters only as the first power. 

To obtain a general impression of the impurity levels we use $m _ { e } \approx 0 . 1$ m for electrons in germanium and $m _ { e } \approx 0 . 2$ m in silicon. The static dielectric constant is given in Table 4. The ionization energy of the free hydrogen atom is 13.6 eV. For germanium the donor ionization energy $E _ { d }$ on our model is 5 meV, reduced with respect to hydrogen by the factor $m _ { e } / m \epsilon ^ { 2 } = 4 \times 1 0 ^ { - 4 }$ . The corresponding result for silicon is 20 meV. Calculations using the correct anisotropic mass tensor predict 9.05 meV for germanium and 29.8 meV for silicon. Observed values of donor ionization energies in Si and Ge are given in Table 5. In GaAs donors have $E _ { d } \approx 6$ meV. 


Table 4 Static relative dielectric constant of semiconductors


<table><tr><td>Crystal</td><td><eq>\epsilon</eq></td><td>Crystal</td><td><eq>\epsilon</eq></td></tr><tr><td>Diamond</td><td>5.5</td><td>GaSb</td><td>15.69</td></tr><tr><td>Si</td><td>11.7</td><td>GaAs</td><td>13.13</td></tr><tr><td>Ge</td><td>15.8</td><td>AlAs</td><td>10.1</td></tr><tr><td>InSb</td><td>17.88</td><td>AlSb</td><td>10.3</td></tr><tr><td>InAs</td><td>14.55</td><td>SiC</td><td>10.2</td></tr><tr><td>InP</td><td>12.37</td><td><eq>Cu_{2}O</eq></td><td>7.1</td></tr></table>


Table 5 Donor ionization energies $E _ { d }$ of pentavalent impurities in germanium and silicon, in meV


<table><tr><td></td><td>P</td><td>As</td><td>Sb</td></tr><tr><td>Si</td><td>45.</td><td>49.</td><td>39.</td></tr><tr><td>Ge</td><td>12.0</td><td>12.7</td><td>9.6</td></tr></table>

The radius of the first Bohr orbit is increased by $\epsilon m / m _ { e }$ over the value 0.53 Å for the free hydrogen atom. The corresponding radius is (160)(0.53) 80 Å in germanium and $( 6 0 ) ( 0 . 5 3 ) \simeq 3 0 \mathrm { ~ \AA ~ }$ in silicon. These are large radii, so that donor orbits overlap at relatively low donor concentrations, compared to the number of host atoms. With appreciable orbit overlap, an “impurity band” is formed from the donor states: see the discussion of the metal-insulator transition in Chapter 14. 

The semiconductor can conduct in the impurity band by electrons hopping from donor to donor. The process of impurity band conduction sets in at lower donor concentration levels if there are also some acceptor atoms present, so that some of the donors are always ionized. It is easier for a donor electron to hop to an ionized (unoccupied) donor than to an occupied donor atom, in order that two electrons will not have to occupy the same site during charge transport. 

Acceptor States. A hole may be bound to a trivalent impurity in germanium or silicon (Fig. 20), just as an electron is bound to a pentavalent impurity. Trivalent impurities such as B, Al, Ga, and In are called acceptors because they accept electrons from the valence band in order to complete the covalent bonds with neighbor atoms, leaving holes in the band. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/59f593acc46e01cd5130e1f3f10ec74c304c3107aea52e556f9ff2ff074123e7.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/f605d6109dc0e2bd419576a5f321dead691891740eebc6a4414ad5d4d2be55c1.jpg)



Figure 20 Boron has only three valence electrons; it can complete its tetrahedral bonds only by taking an electron from a Si-Si bond, leaving behind a hole in the silicon valence band. The positive hole is then available for conduction. The boron atom is called an acceptor because when ionized it accepts an electron from the valence band. At 0 K the hole is bound.



Table 6 Acceptor ionization energies $E _ { a }$ of trivalent impurities in germanium and silicon, in meV


<table><tr><td></td><td>B</td><td>Al</td><td>Ga</td><td>In</td></tr><tr><td>Si</td><td>45.</td><td>57.</td><td>65.</td><td>157.</td></tr><tr><td>Ge</td><td>10.4</td><td>10.2</td><td>10.8</td><td>11.2</td></tr></table>

When an acceptor is ionized a hole is freed, which requires an input of energy. On the usual energy band diagram, an electron rises when it gains energy, whereas a hole sinks in gaining energy. 

Experimental ionization energies of acceptors in germanium and silicon are given in Table 6. The Bohr model applies qualitatively for holes just as for electrons, but the degeneracy at the top of the valence band complicates the effective mass problem. 

The tables show that donor and acceptor ionization energies in Si are comparable with $k _ { B } T$ at room temperature (26 meV), so that the thermal ionization of donors and acceptors is important in the electrical conductivity of silicon at room temperature. If donor atoms are present in considerably greater numbers than acceptors, the thermal ionization of donors will release electrons into the conduction band. The conductivity of the specimen then will be controlled by electrons (negative charges), and the material is said to be n type. 

If acceptors are dominant, holes will be released into the valence band and the conductivity will be controlled by holes (positive charges): the material is p type. The sign of the Hall voltage (6.53) is a rough test for n or p type. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/9b220d40aebd06410e66151045710c8ed1a55ac227bef2862691873eb4fb7229.jpg)



Figure 21 Temperature dependence of the free carrier concentration in ultrapure ${ \mathrm { G e } } ,$ , after R. N. Hall. The net concentration of electrically active impurities is $2 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 3 } ,$ as determined by Hall coefficient measurements. The rapid onset of intrinsic excitation as the temperature is increased is evident at low values of 1/T. The carrier concentration is closely constant between 20 K and 200 K.


Another handy laboratory test is the sign of the thermoelectric potential, discussed below. 

The numbers of holes and electrons are equal in the intrinsic regime. The intrinsic electron concentration $n _ { i }$ at 300 K is $\mathrm { 1 . 7 \times 1 0 ^ { 1 3 } ~ c m ^ { - 3 } }$ in germanium and $4 . 6 \times 1 0 ^ { 9 } \mathrm { ~ c m } ^ { - 3 }$ in silicon. The electrical resistivity of intrinsic material is 43 ohm-cm for germanium and $2 . 6 \times 1 0 ^ { 5 }$ ohm-cm for silicon. 

Germanium has $4 . 4 2 \times 1 0 ^ { 2 2 }$ atoms per $\mathrm { c m ^ { 3 } }$ . The purification of Ge has been carried further than any other element. The concentration of the common electrically active impurities—the shallow donor and acceptor impurities—has been reduced below 1 impurity atom in $1 0 ^ { 1 1 }$ Ge atoms (Fig. 21). For example, the concentration of P in Ge can be reduced below $4 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 3 }$ . There are impurities (H, O, Si, C) whose concentrations in Ge cannot usually be reduced below $1 0 ^ { 1 2 } { - } 1 0 ^ { 1 4 } \mathrm { ~ c m ^ { - 3 } }$ , but these do not affect electrical measurements and therefore may be hard to detect. 

## Thermal Ionization of Donors and Acceptors

The calculation of the equilibrium concentration of conduction electrons from ionized donors is identical with the standard calculation in statistical mechanics of the thermal ionization of hydrogen atoms (TP, p. 369). If there are no acceptors present, the result in the low temperature limit $k _ { B } T \ll E _ { d }$ is 

$$
n \cong (n _ {0} N _ {d}) ^ {1 / 2} \exp (- E _ {d} / 2 k _ {B} T), \tag {53}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/095edc57be2f06d44caad73a9a97a9011efeb784d3e9ea8b3f33a88f68a9fdc2.jpg)



Figure 22 Electrical conductivity and hole concentration $p$ calculated as a function of electron concentration n for a semiconductor at a temperature such that $n p = 1 0 ^ { 2 0 } \mathrm { c m } ^ { - 6 }$ . The conductivity is symmetrical about $n = 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 3 }$ . For $n > \bar { 1 } 0 ^ { 1 0 }$ , the specimen is n type; for $n < 1 0 ^ { 1 0 }$ , it is p type. We have taken $\mu _ { e } = \mu _ { h } ,$ , for the mobilities.


with $n _ { 0 } \equiv 2 ( m _ { e } k _ { B } T / 2 \pi \hbar ^ { 2 } ) ^ { 3 / 2 }$ here ; $N _ { d }$ is the concentration of donors. To obtain (53) we apply the laws of chemical equilibria to the concentration ratio $[ e ] [ N _ { d } ^ { + } ] / [ N _ { d } ]$ and then set , $[ N _ { d } ^ { + } ] = [ e ] = n$ Identical results hold for acceptors,. under the assumption of no donor atoms. 

If the donor and acceptor concentrations are comparable, affairs are complicated and the equations are solved by numerical methods. However, the law of mass action (43) requires the np product to be constant at a given temperature. An excess of donors will increase the electron concentration and decrease the hole concentration; the sum $n + p$ will increase. The conductivity will increase as $n + p$ if the mobilities are equal, as in Fig. 22. 

# THERMOELECTRIC EFFECTS

Consider a semiconductor maintained at a constant temperature while an electric field drives through it an electric current density $j _ { q } .$ . If the current is carried only by electrons, the charge flux is 

$$
j _ {q} = n (- e) \left(- \mu_ {e}\right) E = n e \mu_ {e} E, \tag {54}
$$

where $\mu _ { e }$ is the electron mobility. The average energy transported by an electron is referred to the Fermi level $\mu _ { i }$ , 

$$
(E _ {c} - \mu) + \frac {3}{2} k _ {B} T,
$$

where $E _ { c }$ is the energy at the conduction band edge. We refer the energy to the Fermi level because different conductors in contact have the same Fermi level. The energy flux that accompanies the charge flux is 

$$
j _ {U} = n (E _ {c} - \mu + \frac {3}{2} k _ {B} T) (- \mu_ {e}) E. \tag {55}
$$

The Peltier coefficient  is defined by $j _ { U } = \Pi j _ { q } ;$ or the energy carried per unit charge. For electrons, 

$$
\Pi_ {e} = - (E _ {c} - \mu + \frac {3}{2} k _ {B} T) / e \tag {56}
$$

and is negative because the energy flux is opposite to the charge flux. For holes 

$$
j _ {q} = p e \mu_ {h} E; \quad j _ {U} = p (\mu - E _ {v} + \frac {3}{2} k _ {B} T) \mu_ {h} E, \tag {57}
$$

where $E _ { v }$ is the energy at the valence band edge. Thus 

$$
\Pi_ {h} = \left(\mu - E _ {v} + \frac {3}{2} k _ {B} T\right) / e \tag {58}
$$

and is positive. Equations (56) and (58) are the result of our simple drift velocity theory; a treatment by the Boltzmann transport equation gives minor numerical differences.2 

The absolute thermoelectric power Q is defined from the open circuit electric field created by a temperature gradient: 

$$
E = Q \operatorname{grad} T. \tag {59}
$$

The Peltier coefficient  is related to the thermoelectric power Q by 

$$
\Pi = Q T. \tag {60}
$$

This is the famous Kelvin relation of irreversible thermodynamics. A measurement of the sign of the voltage across a semiconductor specimen, one end of which is heated, is a rough and ready way to tell if the specimen is n type or p type (Fig. 23). 

# SEMIMETALS

In semimetals the conduction band edge is very slightly lower in energy than the valence band edge. A small overlap in energy of the conduction and valence bands leads to small concentration of holes in the valence band and of electrons in the conduction band (Table 7). Three of the semimetals, arsenic, antimony, and bismuth, are in group V of the periodic table. 

Their atoms associate in pairs in the crystal lattice, with two ions and ten valence electrons per primitive cell. The even number of valence electrons could allow these elements to be insulators. Like semiconductors, the semimetals may be doped with suitable impurities to vary the relative numbers of holes and electrons. Their concentrations may also be varied with pressure, for the band edge overlap varies with pressure. 


Figure 23 Peltier coefficient of n and p silicon as a function of temperature. Above 600 K the specimens act as intrinsic semiconductors. The curves are calculated and the points are experimental. (After T. H. Geballe and G. W. Hull.)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/cb2b8880-de0d-46c9-86bc-a8ed5d76e463/5023971b3ff3a3f0602be2d43888f5deb80ea50deb1062da277cdabe29052558.jpg)



Table 7 Electron and hole concentrations in semimetals


<table><tr><td>Semimetal</td><td><eq>n_e</eq>, in cm<eq>^{-3}</eq></td><td><eq>n_h</eq>, in cm<eq>^{-3}</eq></td></tr><tr><td>Arsenic</td><td>(2.12 ± 0.01) × 10<eq>^{20}</eq></td><td>(2.12 ± 0.01) × 10<eq>^{20}</eq></td></tr><tr><td>Antimony</td><td>(5.54 ± 0.05) × 10<eq>^{19}</eq></td><td>(5.49 ± 0.03) × 10<eq>^{19}</eq></td></tr><tr><td>Bismuth</td><td>2.88 × 10<eq>^{17}</eq></td><td>3.00 × 10<eq>^{17}</eq></td></tr><tr><td>Graphite</td><td>2.72 × 10<eq>^{18}</eq></td><td>2.04 × 10<eq>^{18}</eq></td></tr></table>

# SUPERLATTICES

Consider a multilayer crystal of alternating thin layers of different compositions. Coherent layers on a nanometer thickness scale may be deposited by molecular-beam epitaxy or metal-organic vapor deposition, thus building up a superperiodic structure on a large scale. Systems of alternate layers of GaAs and GaAlAs have been studied to 50 periods or more, with lattice spacing A of perhaps 5 nm (50 Å). A superperiodic crystal potential arises from the superperiodic structure and acts on the conduction electrons and holes to create new (small) Brillouin zones and mini energy bands superposed on the band structures of the constituent layers. Here we treat the motion of an electron in a superlattice in an applied electric field. 

## Bloch Oscillator

Consider a collisionless electron in a periodic lattice in one dimension, with motion normal to the planes of the superlattice. The equation of motion in a constant electric field parallel to k is $\hbar d k / d t = - e E$ or, for motion across a Brillouin zone with reciprocal lattice vector $G = 2 \pi / A$ , we have $\hbar G = \hbar 2 \pi / A = e E T$ where T is the period of the motion. The Bloch, frequency of the motion is $\omega _ { B } = 2 \pi / T = e E A / \hbar$ The electron accelerates from. $k = 0$ toward the zone boundary; when it reaches $k = \pi / A$ it reappears (as by an Umklapp process) at the zone boundary at the identical point $- \pi / A$ , using the argument of Chapter 2. 

We consider the motion in a model system in real space. We suppose that the electron lies in a simple energy band of width $\epsilon _ { \mathrm { 0 } } \mathrm { : }$ 

$$
\epsilon = \epsilon_ {0} (1 - \cos k A). \tag {61}
$$

The velocity in k-space (momentum space) is 

$$
\boldsymbol {v} = \hbar^ {- 1} d \epsilon / d k = \left(A \epsilon_ {0} / \hbar\right) \sin k A, \tag {62}
$$

and the position of the electron in real space, with the initial condition $z = 0$ at $t = 0$ , is given by 

$$
\begin{array}{l} z = \int v d t = \int d k v (k) (d t / d k) = \left(A \epsilon_ {0} / \hbar\right) \int d k (- \hbar / e E) \sin k A \\ = (- \epsilon_ {0} / e E) (\cos k A - 1) = (- \epsilon_ {0} / e E) (\cos (- e E A t / \hbar) - 1). \tag {63} \\ \end{array}
$$

This confirms that the Bloch oscillation frequency in real space is $\omega _ { B } = e E A / \hbar$ . The motion in the periodic lattice is quite different from the motion in free space, for which the acceleration is constant. 

## Zener Tunneling

Thus far we have considered the effect of the electrostatic potential eEz $( \mathrm { o r } - e E n A )$ on one energy band; the potential tilts the whole band. Higher bands will also be tilted similarly, creating the possibility of crossing between ladder levels of different bands. The interaction between different band levels at the same energy opens the possibility for an electron in one band at n to cross to another band at $n ^ { \prime }$ . This field-induced interband tunneling is an example of Zener breakdown, met most often at a single junction as in the Zener diode. 

# SUMMARY

• The motion of a wave packet centered at wavevector k is described by $\mathbf { F } = \hbar d \mathbf { k } / d t$ where F is the applied force. The motion in real space is ob-, tained from the group velocity $\mathbf { v } _ { \mathrm { g } } = \hbar ^ { - 1 } \nabla _ { \mathbf { k } } \epsilon ( \mathbf { k } )$ . 

• The smaller the energy gap, the smaller is the effective mass |m*| near the gap. 

• A crystal with one hole has one empty electron state in an otherwise filled band. The properties of the hole are those of the N  1 electrons in this band. 

(a) If the electron is missing from the state of wavevector $\mathbf { k } _ { e } ,$ then the wavevector of the hole is ${ \bf k } _ { h } = - { \bf k } _ { e }$ . 

(b) The rate of change of $\mathbf { k } _ { h }$ in an applied field requires the assignment of a positive charge to the hole: $e _ { h } = e = - e _ { e }$ . 

(c) If ${ \pmb v } _ { e }$ is the velocity an electron would have in the state $\mathbf { k } _ { e } ,$ , then the velocity to be ascribed to the hole of wavevector ${ \bf k } _ { h } = - { \bf k } _ { e }$ is ${ \pmb v } _ { h } = { \pmb v } _ { e }$ . 

(d) The energy of the hole referred to zero for a filled band is positive and is $\epsilon _ { h } ( { \bf k } _ { h } ) = - \epsilon ( { \bf k } _ { e } )$ . 

(e) The effective mass of a hole is opposite to the effective mass of an electron at the same point on the energy band: $m _ { h } = - m _ { e }$ . 

# Problems

1. Impurity orbits. Indium antimonide has $E _ { \mathrm { g } } = 0 . 2 3 \ : \mathrm { e V } ;$ dielectric constant $\epsilon = 1 8 ;$ electron effective mass $m _ { e } = 0 . 0 1 5 ~ m$ . Calculate (a) the donor ionization energy; (b) the radius of the ground state orbit. (c) At what minimum donor concentration will appreciable overlap effects between the orbits of adjacent impurity atoms occur? This overlap tends to produce an impurity band—a band of energy levels which permit conductivity presumably by a hopping mechanism in which electrons move from one impurity site to a neighboring ionized impurity site. 

2. Ionization of donors. In a particular semiconductor there are $1 0 ^ { 1 3 }$ donors/cm3 with an ionization energy $E _ { d }$ of 1 meV and an effective mass 0.01 m. (a) Estimate the concentration of conduction electrons at 4 K. (b) What is the value of the Hall coefficent? Assume no acceptor atoms are present and that $E _ { \mathrm { g } } \gg k _ { B } T$ . 

3. Hall effect with two carrier types. Assuming concentration n, p; relaxation times $\tau _ { e } , \tau _ { h } ;$ and masses $m _ { e } , m _ { h }$ show that the Hall coefficient in the drift velocity approximation is 

$$
R _ {H} = \frac {1}{e c} \cdot \frac {p - n b ^ {2}}{(p + n b) ^ {2}}, \tag {CGS}
$$

where $b = \mu _ { e } / \mu _ { h }$ is the mobility ratio. In the derivation neglect terms of order $B ^ { 2 } .$ In SI we drop the c. Hint: In the presence of a longitudinal electric field, find the transverse electric field such that the transverse current vanishes. The algebra may seem tedious, but the result is worth the trouble. Use (6.64), but for two carrier types; neglect $( \omega _ { c } \tau ) ^ { 2 }$ in comparison with $\omega _ { c } \tau .$ . 

4. Cyclotron resonance for a spheroidal energy surface. Consider the energy surface 

$$
\epsilon (\mathbf {k}) = \hbar^ {2} \biggl (\frac {k _ {x} ^ {2} + k _ {y} ^ {2}}{2 m _ {t}} + \frac {k _ {z} ^ {2}}{2 m _ {l}} \biggr) ,
$$

where $m _ { t }$ is the transverse mass parameter and $m _ { l }$ is the longitudinal mass parameter. A surface on which (k) is constant will be a spheroid. Use the equation of motion (6), with ${ \bf v } = \hbar ^ { - 1 } \nabla _ { \mathrm { k } } \epsilon$ to show that, $\omega _ { c } = e B / ( m _ { l } m _ { t } ) ^ { 1 / 2 } c$ when the static magnetic field B lies in the xy plane. This result agrees with (34) when $\theta = \pi / 2$ . The result is in CGS; to obtain SI, omit the c. 

5. Magnetoresistance with two carrier types. Problem 6.9 shows that in the drift velocity approximation the motion of charge carriers in electric and magnetic fields does not lead to transverse magnetoresistance. The result is different with two carrier types. Consider a conductor with a concentration n of electrons of effective mass $m _ { e }$ and relaxation time $\tau _ { e } ;$ and a concentration $p$ of holes of effective mass $m _ { h }$ and relaxation time $\tau _ { h } .$ . Treat the limit of very strong magnetic fields, $\omega _ { c } \tau \gg 1$ . (a) Show in this limit that $\sigma _ { y x } = ( n - p ) e c / B$ . (b) Show that the Hall field is given by, with $Q \equiv \omega _ { c } \tau$ , 

$$
E _ {y} = - (n - p) \left(\frac {n}{Q _ {e}} + \frac {p}{Q _ {h}}\right) ^ {- 1} E _ {x},
$$

which vanishes if $n = p , \left( \mathrm { c } \right)$ Show that the effective conductivity in the x direction is 

$$
\sigma_ {\text { eff }} = \frac {e c}{B} \left[ \left(\frac {n}{Q _ {e}} + \frac {p}{Q _ {h}}\right) + (n - p) ^ {2} \left(\frac {n}{Q _ {e}} + \frac {p}{Q _ {h}}\right) ^ {- 1} \right].
$$

If $n = p , \sigma \propto B ^ { - 2 }$ . If $n \neq p$ ,  saturates in strong fields; that is, it approaches a limit independent of B as $B  \infty$ . 