# Metal–Semiconductor and Semiconductor Heterojunctions

n the preceding two chapters, we have considered the pn junction and assumed that the semiconductor material was the same throughout the structure. This type of junction is referred to as a homojunction. We developed the electrostatics of the junction and derived the current–voltage relationship. In this chapter, we consider the metal–semiconductor junction and the semiconductor heterojunction, in which the material on each side of the junction is not the same. These junctions can also produce diodes. 

Semiconductor devices, or integrated circuits, must make contact with the outside world. This contact is made through nonrectifying metal–semiconductor junctions, or ohmic contacts. An ohmic contact is a low-resistance junction providing current conduction in both directions. We examine in this chapter the conditions that yield metal–semiconductor ohmic contacts. ■ 

# 9.0 | PREVIEW

In this chapter, we will: 

■ Determine the energy-band diagram of a metal–semiconductor junction. 

Investigate the electrostatics of the rectifying metal–semiconductor junction, which is known as the Schottky barrier diode. 

■ Derive the ideal current–voltage relation of the Schottky barrier diode. 

■ Discuss differences in the current transport mechanism between the Schottky barrier diode and pn junction diode, and discuss differences in turn-on voltage and switching times. 

■ Discuss ohmic contacts, which are low-resistance, nonrectifying metal– semiconductor junctions. 

■ Investigate the characteristics of a semiconductor heterojunction. 

# 9.1 | THE SCHOTTKY BARRIER DIODE

One of the fi rst practical semiconductor devices used in the early 1900s was the metal–semiconductor diode. This diode, also called a point contact diode, was made by touching a metallic whisker to an exposed semiconductor surface. These metal– semiconductor diodes were not easily reproduced or mechanically reliable and were replaced by the pn junction in the 1950s. However, semiconductor and vacuum technology is now used to fabricate reproducible and reliable metal–semiconductor contacts. In this section, we consider the metal–semiconductor rectifying contact, or Schottky barrier diode. In most cases, the rectifying contacts are made on n-type semiconductors; for this reason, we concentrate on this type of diode. 

# 9.1.1 Qualitative Characteristics

The ideal energy-band diagram for a particular metal and n-type semiconductor before making contact is shown in Figure 9.1a. The vacuum level is used as a reference level. The parameter $\phi _ { m }$ is the metal work function (measured in volts), $\phi _ { s }$ is the semiconductor work function, and $\chi$ is known as the electron affi nity. The work functions of various metals are given in Table 9.1 and the electron affi nities of several semiconductors are given in Table 9.2. In Figure 9.1a, we have assumed that $\phi _ { m } > \phi _ { : }$ s . The ideal thermal-equilibrium metal–semiconductor energy-band diagram, for this situation, is shown in Figure 9.1b. Before contact, the Fermi level in the semiconductor was above that in the metal. In order for the Fermi level to become a constant through the system in thermal equilibrium, electrons from the semiconductor fl ow into the lower energy states in the metal. Positively charged donor atoms remain in the semiconductor, creating a space charge region. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/3382b9205aae7d38c022722f1f75ab8e7cb803f037c9cd3c7cc8e0393abc3ef6.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/2ebab67c21b78d35f698568854492a39d51824f5628c20702fd86670f4758c53.jpg)



(b)



Figure 9.1 | (a) Energy-band diagram of a metal and semi conductor before contact; (b) ideal energy-band diagram of a metal–n-semiconductor junction for $\phi _ { m } > \phi _ { s }$



Table 9.1 | Work functions of some elements


<table><tr><td>Element</td><td>Work function, <eq>\phi_m</eq></td></tr><tr><td>Ag, silver</td><td>4.26</td></tr><tr><td>Al, aluminum</td><td>4.28</td></tr><tr><td>Au, gold</td><td>5.1</td></tr><tr><td>Cr, chromium</td><td>4.5</td></tr><tr><td>Mo, molybdenum</td><td>4.6</td></tr><tr><td>Ni, nickel</td><td>5.15</td></tr><tr><td>Pd, palladium</td><td>5.12</td></tr><tr><td>Pt, platinum</td><td>5.65</td></tr><tr><td>Ti, titanium</td><td>4.33</td></tr><tr><td>W, tungsten</td><td>4.55</td></tr></table>


Table 9.2 | Electron affi nity of some semiconductors


<table><tr><td>Element</td><td>Electron affinity, <eq>\chi</eq></td></tr><tr><td>Ge, germanium</td><td>4.13</td></tr><tr><td>Si, silicon</td><td>4.01</td></tr><tr><td>GaAs, gallium arsenide</td><td>4.07</td></tr><tr><td>AlAs, aluminum arsenide</td><td>3.5</td></tr></table>

The parameter $\phi _ { B 0 }$ is the ideal barrier height of the semiconductor contact, the potential barrier seen by electrons in the metal trying to move into the semiconductor. This barrier is known as the Schottky barrier and is given, ideally, by 

$$
\phi_ {B 0} = \left(\phi_ {m} - \chi\right) \tag {9.1}
$$

On the semiconductor side, $V _ { b i }$ is the built-in potential barrier. This barrier, similar to the case of the pn junction, is the barrier seen by electrons in the conduction band trying to move into the metal. The built-in potential barrier is given by 

$$
V _ {b i} = \phi_ {B 0} - \phi_ {n} \tag {9.2}
$$

which makes $V _ { b i }$ a slight function of the semiconductor doping, as is the case in a pn junction. 

If we apply a positive voltage to the semiconductor with respect to the metal, the semiconductor-to-metal barrier height increases, while $\phi _ { B 0 }$ remains constant in this idealized case. This bias condition is the reverse bias. If a positive voltage is applied to the metal with respect to the semiconductor, the semiconductor-to-metal barrier $V _ { b i }$ is reduced while $\phi _ { B 0 }$ again remains essentially constant. In this situation, electrons can more easily fl ow from the semiconductor into the metal since the barrier has been reduced. This bias condition is the forward bias. The energy-band diagrams for the reverse and forward bias are shown in Figures 9.2a,b where $V _ { R }$ is the magnitude of the reverse-biased voltage and $V _ { a }$ is the magnitude of the forward-bias voltage. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/db94843d97dbf33877e1bf6771cf4bd3464d83c29ac11ec7f3010fc6cf645f6d.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/23b32d006aae9572a8c347df13843be873a7c8d4af320812c1ee010275eb5a99.jpg)



(b)



Figure 9.2 | Ideal energy-band diagram of a metal–semiconductor junction (a) under reverse bias and (b) under forward bias.


The energy-band diagrams versus voltage for the metal–semiconductor junction shown in Figure 9.2 are very similar to those of the pn junction given in the previous chapter. Because of this similarity, we expect the current–voltage characteristics of the Schottky barrier junction to be similar to the exponential behavior of the pn junction diode. The current mechanism here, however, is due to the fl ow of majority carrier electrons. In forward bias, the barrier seen by the electrons in the semiconductor is reduced, so majority carrier electrons fl ow more easily from the semiconductor into the metal. The forward-bias current is in the direction from metal to semiconductor: It is an exponential function of the forward-bias voltage $V _ { a }$ . 

# 9.1.2 Ideal Junction Properties

We can determine the electrostatic properties of the junction in the same way as we do for the pn junction. The electric fi eld in the space charge region is determined from Poisson’s equation. We have that 

$$
\frac {d \mathrm{E}}{d x} = \frac {\rho (x)}{\epsilon_ {s}} \tag {9.3}
$$

where $\rho ( x )$ is the space charge volume density and s is the permittivity of the semiconductor. If we assume that the semiconductor doping is uniform, then by integrating Equation (9.3), we obtain 

$$
\mathrm{E} = \int \frac {e N _ {d}}{\epsilon_ {s}} d x = \frac {e N _ {d} x}{\epsilon_ {s}} + C _ {1} \tag {9.4}
$$

where $C _ { 1 }$ is a constant of integration. The electric fi eld is zero at the space charge edge in the semiconductor, so the constant of integration can be found as 

$$
C _ {1} = - \frac {e N _ {d} x _ {n}}{\epsilon_ {s}} \tag {9.5}
$$

The electric fi eld can then be written as 

$$
\mathrm{E} = - \frac {e N _ {d}}{\epsilon_ {s}} (x _ {n} - x) \tag {9.6}
$$

which is a linear function of distance, for the uniformly doped semiconductor, and reaches a peak value at the metal–semiconductor interface. Since the E-fi eld is zero inside the metal, a negative surface charge must exist in the metal at the metal– semiconductor junction. 

The space charge region width, W, may be calculated as we do for the pn junction. The result is identical to that of a one-sided pn junction. For the uniformly doped semiconductor, we have 

$$
W = x _ {n} = \left[ \frac {2 \epsilon_ {s} (V _ {b i} + V _ {R})}{e N _ {d}} \right] ^ {1 / 2} \tag {9.7}
$$

where $V _ { R }$ is the magnitude of the applied reverse-biased voltage. We are again assuming an abrupt junction approximation. 

Objective: Determine the theoretical barrier height, built-in potential barrier, and maximum electric fi eld in a metal–semiconductor diode for zero applied bias. 

Consider a contact between tungsten and n-type silicon doped to $N _ { d } = 1 0 ^ { 1 6 } ~ \mathrm { c m } ^ { - 3 }$ at $T = 3 0 0 \mathrm { K } .$ 

EXAMPLE 9.1 

# Solution

The metal work function for tungsten (W) from Table 9.1 is $\phi _ { m } = 4 . 5 5 \ : \mathrm { V }$ and the electron affi nity for silicon from Table 9.2 is $\chi = 4 . 0 1 \ : \mathrm { V }$ . The barrier height is then 

$$
\phi_ {B 0} = \phi_ {m} - \chi = 4. 5 5 - 4. 0 1 = 0. 5 4 \mathrm{V}
$$

where $\phi _ { B 0 }$ is the ideal Schottky barrier height. We can calculate $\phi _ { n }$ as 

$$
\phi_ {n} = \frac {k T}{e} \ln \left(\frac {N _ {c}}{N _ {d}}\right) = 0. 0 2 5 9 \ln \left(\frac {2 . 8 \times 1 0 ^ {1 9}}{1 0 ^ {1 6}}\right) = 0. 2 0 6 \mathrm{V}
$$

Then 

$$
V _ {b i} = \phi_ {B 0} - \phi_ {n} = 0. 5 4 - 0. 2 0 6 = 0. 3 3 4 \mathrm{V}
$$

The space charge width at zero bias is 

$$
x _ {n} = \left[ \frac {2 \epsilon_ {s} V _ {b i}}{e N _ {d}} \right] ^ {1 / 2} = \left[ \frac {2 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 3 3 4)}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 6})} \right] ^ {1 / 2}
$$

or 

$$
x _ {n} = 0. 2 0 8 \times 1 0 ^ {- 4} \mathrm{cm}
$$

Then the maximum electric fi eld is 

$$
\left| \mathrm{E} _ {\max} \right| = \frac {e N _ {d} x _ {n}}{\epsilon_ {s}} = \frac {(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 6}) (0 . 2 0 8 \times 1 0 ^ {- 4})}{(1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4})}
$$

or fi nally 

$$
\left| \mathrm{E} _ {\max} \right| = 3. 2 1 \times 1 0 ^ {4} \mathrm{V/cm}
$$

# ■ Comment

The values of space charge width and electric fi eld are very similar to those obtained for a pn junction. 

# ■ EXERCISE PROBLEM

Ex 9.1 Consider an ideal tungsten-to-n-type GaAs junction. Assume the GaAs is doped to a concentration of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Determine the theoretical barrier height, the built-in potential barrier, and maximum electric fi eld for the case of zero applied bias. 

$$
\left(\text { Ans. } \phi_ {B 0} = 0. 4 8 \mathrm{V}, \mathrm{V} _ {b i} = 0. 3 6 2 3 \mathrm{V}, \mathrm{E} _ {\max} = 2. 2 4 \times 1 0 ^ {4} \mathrm{V/cm}\right)
$$

A junction capacitance can also be determined in the same way as we do for the pn junction. We have that 

$$
C ^ {\prime} = e N _ {d} \frac {d x _ {n}}{d V _ {R}} = \left[ \frac {e \epsilon_ {s} N _ {d}}{2 (V _ {b i} + V _ {R})} \right] ^ {1 / 2} \tag {9.8}
$$

where $C ^ { \prime }$ is the capacitance per unit area. If we square the reciprocal of Equation (9.8), we obtain 

$$
\left(\frac {1}{C ^ {\prime}}\right) ^ {2} = \frac {2 (V _ {b i} + V _ {R})}{e \epsilon_ {s} N _ {d}} \tag {9.9}
$$

We can use Equation (9.9) to obtain, to a fi rst approximation, the built-in potential barrier $V _ { b i }$ , and the slope of the curve from Equation (9.9) to yield the semiconductor doping $N _ { d } .$ . We can calculate the potential $\phi _ { n }$ and then determine the Schottky barrier $\phi _ { B 0 }$ from Equation (9.2). 

# EXAMPLE 9.2

Objective: To calculate the semiconductor doping concentration and Schottky barrier height from the silicon diode experimental capacitance data shown in Figure 9.3. Assume $T = 3 0 0 \mathrm { K }$ . 

# ■ Solution

The intercept of the tungsten–silicon curve is approximately at $V _ { b i } = 0 . 4 0 \mathrm { ~ V ~ }$ . From Equation (9.9), we can write 

$$
\frac {d \left(1 / C ^ {\prime}\right) ^ {2}}{d V _ {R}} \approx \frac {\Delta \left(1 / C ^ {\prime}\right) ^ {2}}{\Delta V _ {R}} = \frac {2}{e \epsilon_ {s} N _ {d}}
$$

Then, from the fi gure, we have 

$$
\frac {\Delta (1 / C ^ {\prime}) ^ {2}}{\Delta V _ {R}} \approx 4. 4 \times 1 0 ^ {1 3}
$$

so that 

$$
N _ {d} = \frac {2}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (4 . 4 \times 1 0 ^ {1 3})} = 2. 7 \times 1 0 ^ {1 7} \mathrm{cm} ^ {- 3}
$$

We can calculate 

$$
\phi_ {n} = \frac {k T}{e} \ln \left(\frac {N _ {c}}{N _ {d}}\right) = (0. 0 2 5 9) \ln \left(\frac {2 . 8 \times 1 0 ^ {1 9}}{2 . 7 \times 1 0 ^ {1 7}}\right) = 0. 1 2 \mathrm{V}
$$

so that 

$$
\phi_ {B n} = V _ {b i} + \phi_ {n} = 0. 4 0 + 0. 1 2 = 0. 5 2 \mathrm{V}
$$

where $\phi _ { B n }$ is the actual Schottky barrier height. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/4527f0a0d2f31d5a3532a45451b9c8358e905a9112012e2a5007052d9c4fb498.jpg)



Figure 9.3 | $1 / C ^ { 2 }$ versus $V _ { R }$ for W–Si and W–GaAs



Schottky barrier diodes.



(From Sze and $N g$ [15].)


# ■ Comment

The experimental value of 0.52 V can be compared with the ideal barrier height of $\phi _ { B 0 } = 0 . 5 4$ V found in Example 9.1. These results agree fairly well. For other metals, the discrepancy between experiment and theory is larger. 

# ■ EXERCISE PROBLEM

Ex 9.2 Repeat Example 9.2 for the GaAs diode capacitance data shown in Figure 9.3. 

$$
(\text { Ans. } \mathrm{V} _ {b i} \equiv 0. 6 4 \mathrm{V}, N _ {d} = 4. 6 2 \times 1 0 ^ {1 8} \mathrm{cm} ^ {- 3})
$$

We can see that the built-in potential barrier of the gallium arsenide Schottky diode is larger than that of the silicon diode. This experimental result is normally observed for all types of metal contacts. 

# TEST YOUR UNDERSTANDING

TYU 9.1 Consider an ideal chromium-to-n-type silicon Schottky diode at $T = 3 0 0 \mathrm { K } .$ 

Assume the semiconductor is doped at a concentration of $N _ { d } = 3 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ 

Determine the (a) ideal Schottky barrier height, (b) built-in potential barrier, 

(c) peak electric fi eld with an applied reverse-biased voltage of $V _ { R } = 5 \mathrm { \ V } ,$ , and (d) 

junction capacitance per unit area for VR  5 V.  10  6.88   C ) d(9  ] 2 F/cm $V _ { R } = 5 \mathrm { \bf ~ V } . \quad \left[ \mathrm { \tt { \Psi } } [ \mathrm { \bf { u } } \mathrm { \bf { 3 / 4 } } _ { 6 - } 0 \mathrm { \bf { l } } \mathrm { \bf { \Psi } } \times 8 8 \mathrm { \bf { \dot { 9 } } } = \mathrm { \bf { \Psi } } . \mathrm { \bf { \Psi } } ) \right.$ 

${ } ^ { \mathrm { { ' } } } \{ \mathrm { u } \mathfrak { o } / \Lambda \ _ { \mathfrak { p } } 0 [ \ \times \ 8 6 ^ { \circ } \mathfrak { p } = \left| ^ { \mathrm { { x e u } } } \Xi \right| \ ( \mathfrak { o } ) \ ^ { \cdot } \Lambda \ \mathfrak { C } \ \varsigma \overline { { \varsigma } } ^ { \cdot } 0 = { } ^ { \varkappa } \Lambda \ ( q ) : \Lambda \ 6 { \dot { \gamma } } ^ { \cdot } 0 = { } ^ { \circ q } \phi \ ( \mathfrak { o } ) \ ^ { \cdot } \mathrm { s u } \vee \}$ 

TYU 9.2 Repeat TYU 9.1 for an ideal palladium-to-n-type GaAs Schottky diode with the same impurity concentration. $\mathsf { \Pi } _ { \left[ \mathsf { \mathfrak { z } } ^ { \mathrm { U U } 3 } / \mathsf { d } _ { \mathsf { \theta } 6 - } \mathsf { 0 } \mathsf { I } \times 9 \bar { 8 } ^ { \cdot } \mathsf { 9 } = \mathsf { \Omega } _ { \mathcal { S } } ( p ) \right. }$ 

$$
\left. \left[ \text {Ans.} (a) \phi_ {B o} = 1. 0 5 \mathrm{V}; (b) \mathrm{V} _ {b i} = 0. 9 1 9 \mathrm{V}; (c) \mid \mathrm{E} _ {\max} \right| = 7 \times 1 0 ^ {4} \mathrm{V/cm}; \right.
$$

# 9.1.3 Nonideal Effects on the Barrier Height

Schottky Barrier Lowering Several effects alter the actual Schottky barrier height from the theoretical value given by Equation (9.1). The fi rst such effect that we consider is the Schottky effect, or image-force-induced lowering of the potential barrier. 

An electron in a dielectric material at a distance x from the metal will create an electric fi eld. The electric fi eld can be determined by adding an image charge, $+ e ,$ inside the metal located at the same distance, x , from the interface. This image effect is shown in Figure 9.4a. Note that the E–fi eld lines are perpendicular to the metal surface as we expect. The force on the electron, due to the coulomb attraction with the image force, is 

$$
F = \frac {- e ^ {2}}{4 \pi \epsilon_ {s} (2 x) ^ {2}} = - e \mathrm{E} \tag {9.10}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/c013f4396626a85a413f758f3754fd097689648f991ea36407e7638dbfad3c10.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/32f39ec87a1fbc7665f3783b20fb2b75053cd2b60a2654521d89819857bc875a.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/2e1bcca786b9d67cace7082420b3bf4464406a9d9f8082126bf3fcf9bce0c171.jpg)



Figure 9.4 | (a) Image charge and electric fi eld lines at a metal–dielectric interface. (b) Distortion of the potential barrier due to image forces with zero electric fi eld and (c) with a constant electric fi eld.


The potential can then be found as 

$$
- \phi (x) = + \int_ {x} ^ {\infty} \mathrm{E} d x ^ {\prime} = + \int_ {x} ^ {\infty} \frac {e}{4 \pi \epsilon_ {s} \cdot 4 (x ^ {\prime}) ^ {2}} d x ^ {\prime} = \frac {- e}{1 6 \pi \epsilon_ {s} x} \tag {9.11}
$$

where $x ^ { \prime }$ is the integration variable and where we have assumed that the potential is zero at $x = \infty .$ . 

The potential energy of the electron is e-(x): Figure 9.4b is a plot of the potential energy assuming that no other electric fi elds exist. With an electric fi eld present in the dielectric, the potential is modifi ed and can be written as 

$$
- \phi (x) = \frac {- e}{1 6 \pi \epsilon_ {s} x} - \mathrm{E} x \tag {9.12}
$$

The potential energy of the electron, including the effect of a constant electric fi eld, is plotted in Figure 9.4c. The peak potential barrier is now lowered. This lowering of the potential barrier is the Schottky effect, or image force–induced lowering. 

We can fi nd the Schottky barrier lowering, $\Delta \phi ,$ , and the position of the maximum barrier, $x _ { m }$ , from the condition that 

$$
\frac {d [ e \phi (x) ]}{d x} = 0 \tag {9.13}
$$

We fi nd that 

$$
x _ {m} = \sqrt {\frac {e}{1 6 \pi \epsilon_ {s} E}} \tag {9.14}
$$

and 

$$
\Delta \phi = \sqrt {\frac {e E}{4 \pi \epsilon_ {s}}} \tag {9.15}
$$

Objective: Calculate the Schottky barrier lowering and the position of the maximum barrier height. 

Consider a gallium arsenide metal–semiconductor contact in which the electric fi eld in the semiconductor is assumed to be $\mathrm { E } = 6 . 8 \times 1 0 ^ { 4 } \mathrm { V / c m }$ . 

# Solution

The Schottky barrier lowering is given by Equation (9.15), which in this case yields 

$$
\Delta \phi = \sqrt {\frac {e E}{4 \pi \epsilon_ {s}}} = \sqrt {\frac {(1 . 6 \times 1 0 ^ {- 1 9}) (6 . 8 \times 1 0 ^ {4})}{4 \pi (1 3 . 1) (8 . 8 5 \times 1 0 ^ {- 1 4})}} = 0. 0 2 7 3 \mathrm{V}
$$

The position of the maximum barrier height is 

$$
x _ {m} = \sqrt {\frac {e}{1 6 \pi \epsilon_ {s} E}} = \sqrt {\frac {(1 . 6 \times 1 0 ^ {- 1 9})}{1 6 \pi (1 3 . 1) (8 . 8 5 \times 1 0 ^ {- 1 4}) (6 . 8 \times 1 0 ^ {4})}}
$$

or 

$$
x _ {m} = 2 \times 1 0 ^ {- 7} \mathrm{cm} = 2 0 \mathrm{A}
$$

# ■ Comment

Although the Schottky barrier lowering may seem like a small value, the barrier height and the barrier lowering will appear in exponential terms in the current–voltage relationship. A small change in the barrier height can thus have a signifi cant effect on the current in a Schottky barrier diode. 

# ■ EXERCISE PROBLEM

Ex 9.3 Consider the Schottky diode described in Example 9.1. Calculate the Schottky barrier lowering for a reverse-biased voltage of (a) $V _ { R } = 1 \mathrm { ~ V ~ }$ and (b) $V _ { R } = 5 \mathrm { V }$ . 

$$
[ \Lambda \angle 0. 0 = \phi \nabla (q); \Lambda 1 8 2 0. 0 = \phi \nabla (a) \cdot \mathrm{su} ]
$$

Interface States Figure 9.5 shows the measured barrier heights in gallium arsenide and silicon Schottky diodes as a function of metal work functions. There is a monotonic relation between the measured barrier height and the metal work function, but the curves do not fi t the simple relation given in Equation (9.1). The barrier height of the metal–semiconductor junction is determined by both the metal work function and the semi conductor surface or interface states. 

A more detailed energy-band diagram of a metal to n-type semiconductor contact in thermal equilibrium is shown in Figure 9.6. We assume that a narrow interfacial layer of insulator exists between the metal and semiconductor. The interfacial layer can support a potential difference, but will be transparent to the fl ow of electrons between the metal and semiconductor. The semiconductor also shows a distribution of surface states at the metal–semiconductor interface. We assume that all states below the surface potential $\phi _ { 0 }$ are donor states, which will be neutral if the state contains an electron and positively charged if the state does not contain an electron. We also assume that all states above $\phi _ { 0 }$ are acceptor states, which will be neutral if the state does not contain an electron and negatively charged if the state contains an electron. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/e30842e92f49f717a590b634bfc476cb6cd47b2800ebbfb7594f7a94dcc2c738.jpg)



Figure 9.5 | Experimental barrier heights as a function of metal work functions for GaAs and Si.



(From Crowley and Sze [2].)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/970141b8b2691c658dcb8ddeb04113354c192dfad5b32a4580b7adf3c0d21c6a.jpg)



Figure 9.6 | Energy-band diagram of a metal–semiconductor junction with an interfacial layer and interface states.


The diagram in Figure 9.6 shows some acceptor states above $\phi _ { 0 }$ and below $E _ { F }$ . These states tend to contain electrons and are negatively charged. We may assume that the surface state density is constant and equal to $D _ { i t }$ states /cm2-eV. The relation between the surface potential, surface state density, and other semiconductor parameters is found to be 

$$
\left(E _ {g} - e \phi_ {0} - e \phi_ {B n}\right) = \frac {1}{e D _ {i t}} \sqrt {2 e \epsilon_ {s} N _ {d} \left(\phi_ {B n} - \phi_ {n}\right)} - \frac {\epsilon_ {i}}{e D _ {i t} \delta} \left[ \phi_ {m} - (\chi + \phi_ {B n}) \right] \tag {9.16}
$$

We consider two limiting cases. 

Case 1 Let $D _ { i t } \to \infty .$ In this case, the right side of Equation (9.16) goes to zero. We then have 

$$
\phi_ {B n} = \frac {1}{e} (E _ {g} - e \phi_ {0}) \tag {9.17}
$$

The barrier height is now fi xed by the bandgap energy and the potential $\phi _ { 0 } .$ The barrier height is totally independent of the metal work function and the semiconductor electron affi nity. The Fermi level becomes “pinned” at the surface, at the surface potential $\phi _ { 0 } .$ 

Case 2 Let $D _ { i t } \delta \to 0$ . Equation (9.16) reduces to 

$$
\phi_ {B n} = (\phi_ {m} - \chi)
$$

which is the original ideal expression. 

The Schottky barrier height is a function of the electric fi eld in the semiconductor through the barrier lowering effect. The barrier height is also a function of the surface states in the semiconductor. The barrier height, then, is modifi ed from the ideal theoretical value. Since the surface state density is not predictable with any degree of certainty, the barrier height must be an experimentally determined parameter. 

# TEST YOUR UNDERSTANDING

TYU 9.3 Determine the Schottky barrier lowering and the position of the maximum barrier height for the junction described in TYU 9.1. Use the value of the electric fi eld found in TYU 9.1. Å) $\mathsf { I } \mathsf { Z } = \mathsf { \Omega } ^ { u } x \cdot \mathsf { \Omega } \mathsf { \Omega } \mathsf { S } 6 \mathsf { Z } 0 ^ { \cdot } 0 = \phi \nabla \cdot \mathsf { S } \mathsf { U } \mathsf { V } )$ 

# 9.1.4 Current–Voltage Relationship

The current transport in a metal–semiconductor junction is due mainly to majority carriers as opposed to minority carriers in a pn junction. The basic process in the rectifying contact with an n-type semiconductor is by transport of electrons over the potential barrier, which can be described by the thermionic emission theory. 

The thermionic emission characteristics are derived by assuming that the barrier height is much larger than kT, so that the Maxwell–Boltzmann approximation applies and that thermal equilibrium is not affected by this process. Figure 9.7 shows the one-dimensional barrier with an applied forward-bias voltage $V _ { a }$ and two electron current density components. The current $J _ { s \to m }$ is the electron current density due to the fl ow of electrons from the semiconductor into the metal, and the current $J _ { m  s }$ is the electron current density due to the fl ow of electrons from the metal into the semiconductor. The subscripts of the currents indicate the direction of electron fl ow. The conventional current direction is opposite to electron fl ow. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/fa2a3391033c33fe432d7b48f13aea4e7e4d7feb0853c7ee10627fce923b904d.jpg)



Figure 9.7 | Energy-band diagram of a forward-biased metal– semiconductor junction including the image lowering effect.


The current density $J _ { s \to m }$ is a function of the concentration of electrons which have x-directed velocities suffi cient to overcome the barrier. We may write 

$$
J _ {s \rightarrow m} = e \int_ {E _ {c} ^ {\prime}} ^ {\infty} v _ {x} d n \tag {9.18}
$$

where $E _ { c } ^ { \prime }$ is the minimum energy required for thermionic emission into the metal, $v _ { x }$ is the carrier velocity in the direction of transport, and e is the magnitude of the electronic charge. The incremental electron concentration is given by 

$$
d n = g _ {c} (E) f _ {F} (E) d E \tag {9.19}
$$

where $g _ { c } ( E )$ is the density of states in the conduction band and $f _ { F } ( E )$ is the Fermi– Dirac probability function. Assuming that the Maxwell–Boltzmann approximation applies, we may write 

$$
d n = \frac {4 \pi (2 m _ {n} ^ {*}) ^ {3 / 2}}{h ^ {3}} \sqrt {E - E _ {c}} \exp \left[ \frac {- (E - E _ {F})}{k T} \right] d E \tag {9.20}
$$

If all of the electron energy above $E _ { c }$ is assumed to be kinetic energy, then we have 

$$
\frac {1}{2} m _ {n} ^ {*} v ^ {2} = E - E _ {c} \tag {9.21}
$$

The net current density in the metal-to-semiconductor junction can be written as 

$$
J = J _ {s \rightarrow m} - J _ {m \rightarrow s} \tag {9.22}
$$

which is defi ned to be positive in the direction from the metal to the semiconductor. We fi nd that 

$$
J = \left[ A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right) \right] \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {9.23}
$$

where 

$$
A ^ {*} \equiv \frac {4 \pi e m _ {n} ^ {*} k ^ {2}}{h ^ {3}} \tag {9.24}
$$

The parameter $A ^ { * }$ is called the effective Richardson constant for thermionic emission. 

Equation (9.23) can be written in the usual diode form as 

$$
J = J _ {s T} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {9.25}
$$

where $J _ { s T }$ is the reverse-saturation current density and is given by 

$$
J _ {s T} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right) \tag {9.26}
$$

We may recall that the Schottky barrier height $\phi _ { B n }$ changes because of the image-force lowering. We have that $\phi _ { B n } = \phi _ { B 0 } - \Delta \phi$ . Then we can write Equation (9.26) as 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/8b4fc3b353ed220cea5d7fe73fcdd086ad79e8afbe1192efcabcb1e16c2c5c77.jpg)



Figure 9.8 | Experimental and theoretical reverse-biased currents in a PtSi–Si diode. (From Sze and Ng [15].)


$$
J _ {s T} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B 0}}{k T}\right) \exp \left(\frac {e \Delta \phi}{k T}\right) \tag {9.27}
$$

The change in barrier height, $\Delta \phi .$ , will increase with an increase in the electric fi eld, or with an increase in the applied reverse-biased voltage. Figure 9.8 shows a typical reverse-biased current–voltage characteristic of a Schottky barrier diode. The reversebiased current increases with reverse-biased voltage because of the barrier lowering effect. This fi gure also shows the Schottky barrier diode going into breakdown. 

# EXAMPLE 9.4

Objective: Determine the effective Richardson constant from the current–voltage characteristics. 

Consider the tungsten–silicon diode curve in Figure 9.9 and assume a barrier height of $\phi _ { B n } = 0 . 6 7 ~ \mathrm { V } .$ From the fi gure, $J _ { s T } \approx 6 \times 1 0 ^ { - 5 } \mathrm { A / c m ^ { 2 } } .$ . 

# ■ Solution

We have that 

$$
J _ {s T} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right)
$$

so that 

$$
A ^ {*} = \frac {J _ {s T}}{T ^ {2}} \exp \left(\frac {+ e \phi_ {B n}}{k T}\right)
$$

Then 

$$
A ^ {*} = \frac {6 \times 1 0 ^ {- 5}}{(3 0 0) ^ {2}} \exp \left(\frac {0 . 6 7}{0 . 0 2 5 9}\right) = 1 1 4 \mathrm{A} / \mathrm{K} ^ {2} - \mathrm{cm} ^ {2}
$$

# ■ Comment

The experimentally determined value of $A ^ { * }$ is a very strong function of $\phi _ { B n }$ , since $\phi _ { B n }$ is in the exponential term. A small change in $\phi _ { B n }$ will change the value of the Richardson constant substantially. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/41dadc624d6491dde6db515aa4729039c3697c8a02dbec84caac550f4b7d5546.jpg)



Figure 9.9 | Forward-bias current density $J _ { F }$ versus $V _ { a }$ for Wi–Si and W–GaAs diodes. (From Sze and Ng [15].)


# ■ EXERCISE PROBLEM

Ex 9.4 Calculate the ideal Richardson constant for a free electron. 

$$
(\text { Ans. } A ^ {*} = 1 2 0 \mathrm{A} / \mathrm{K} ^ {2} - \mathrm{cm} ^ {2})
$$

We may note that the reverse-saturation current densities of the tungsten–silicon and tungsten–gallium arsenide diodes in Figure 9.9 differ by approximately two orders of magnitude. This two order of magnitude difference will be refl ected in the effective Richardson constant, assuming the barrier heights in the two diodes are essentially the same. The defi nition of the effective Richardson constant, given by Equa tion (9.24), contains the electron effective mass, which differs substantially between silicon and gallium arsenide. The fact that the effective mass is in the expression for the Richardson constant is a direct result of using the effective density of states function in the thermionic emission theory. The net result is that $A ^ { * }$ and $J _ { s T }$ will vary widely between silicon and gallium arsenide. 

# 9.1.5 Comparison of the Schottky Barrier Diode and the pn Junction Diode

Although the ideal current–voltage relationship of the Schottky barrier diode given by Equation (9.25) is of the same form as that of the pn junction diode, there are two important differences between a Schottky diode and a pn junction diode: The fi rst is in the magnitudes of the reverse-saturation current densities and the second is in the switching characteristics. 

The reverse-saturation current density of the Schottky barrier diode was given by Equation (9.26) and is 

$$
J _ {s T} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right)
$$

The ideal reverse-saturation current density of the pn junction diode can be written as 

$$
J _ {s} = \frac {e D _ {n} n _ {p o}}{L _ {n}} + \frac {e D _ {p} p _ {n o}}{L _ {p}} \tag {9.28}
$$

The form of the two equations is vastly different, and the current mechanism in the two devices is different. The current in a pn junction is determined by the diffusion of minority carriers while the current in a Schottky barrier diode is determined by thermionic emission of majority carriers over a potential barrier. 

# EXAMPLE 9.5

Objective: Calculate the ideal reverse-saturation current densities of a Schottky barrier diode and a pn junction diode. 

Consider a tungsten barrier on silicon with a measured barrier height of $e \phi _ { B n } = 0 . 6 7 \mathrm { e V } .$ The effective Richardson constant is $A ^ { * } = 1 1 4 \mathrm { A } / \mathrm { K } ^ { 2 } \mathrm { - } \mathrm { c m } ^ { 2 } . \mathrm { L e t } T = 3 0 0 \mathrm { K } .$ 

# ■ Solution

If we neglect the barrier lowering effect, we have for the Schottky barrier diode 

$$
J _ {s T} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right) = (1 1 4) (3 0 0) ^ {2} \exp \left(\frac {- 0 . 6 7}{0 . 0 2 5 9}\right) = 5. 9 8 \times 1 0 ^ {- 5} \mathrm{A} / \mathrm{cm} ^ {2}
$$

Consider a silicon pn junction with the following parameters at $T = 3 0 0 \mathrm { K } .$ . 

$$
N _ {a} = 1 0 ^ {1 8} \mathrm{cm} ^ {- 3} \quad N _ {d} = 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}
$$

$$
D _ {p} = 1 0 \mathrm{cm} ^ {2} / \mathrm{s} \quad D _ {n} = 2 5 \mathrm{cm} ^ {2} / \mathrm{s}
$$

$$
\tau_ {p o} = 1 0 ^ {- 7} \mathrm{s} \quad \tau_ {n o} = 1 0 ^ {- 7} \mathrm{s}
$$

We can then calculate the following parameters: 

$$
L _ {p} = 1. 0 \times 1 0 ^ {- 3} \mathrm{cm} \quad L _ {n} = 1. 5 8 \times 1 0 ^ {- 3} \mathrm{cm}
$$

$$
p _ {n o} = 2. 2 5 \times 1 0 ^ {4} \mathrm{cm} ^ {- 3} \quad n _ {p o} = 2. 2 5 \times 1 0 ^ {2} \mathrm{cm} ^ {- 3}
$$

The ideal reverse-saturation current density of the pn junction diode can be determined from Equation (9.28) as 

$$
J _ {s} = \frac {(1 . 6 \times 1 0 ^ {- 1 9}) (2 5) (2 . 2 5 \times 1 0 ^ {2})}{(1 . 5 8 \times 1 0 ^ {- 3})} + \frac {(1 . 6 \times 1 0 ^ {- 1 9}) (1 0) (2 . 2 5 \times 1 0 ^ {4})}{(1 . 0 \times 1 0 ^ {- 3})}
$$

$$
= 5. 7 \times 1 0 ^ {- 1 3} + 3. 6 \times 1 0 ^ {- 1 1} = 3. 6 6 \times 1 0 ^ {- 1 1} \mathrm{A} / \mathrm{cm} ^ {2}
$$

# ■ Comment

The ideal reverse-saturation current density of the Schottky barrier junction is orders of magnitude larger than that of the ideal pn junction diode. 

# ■ EXERCISE PROBLEM

Ex 9.5 Using the results of Example 9.5, determine the forward-bias voltages required to produce a current of $1 0 \mu \mathrm { A }$ in each diode. Assume each cross-sectional area is $1 0 ^ { - 4 } \mathrm { c m } ^ { 2 } .$ . 

$$
(\text { Ans.   pn   junction }, \mathrm{V} _ {a} = 0. 5 6 2 8 \mathrm{V}; \text { Society   function }, \mathrm{V} _ {a} = 0. 1 9 2 2 \mathrm{V})
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/f3b7dcec4d672884a1fb5faddd878a5d537529d494c4c4f173db52350738a229.jpg)



Figure 9.10 | Comparison of forwardbias I–V characteristics between a Schottky diode and a pn junction diode.


Recall that the reverse-biased current in a silicon pn junction diode is dominated by the generation current. A typical generation current density is approximately $1 0 ^ { - 7 } \mathrm { \ A } / \mathrm { c m } ^ { 2 } ,$ , which is still two to three orders of magnitude less than the reversesaturation current density of the Schottky barrier diode. A generation current also exists in the reverse-biased Schottky barrier diode; however, the generation current is negligible compared with the $J _ { s T }$ value. 

Since $J _ { s T } \gg J _ { s }$ , the forward-bias characteristics of the two types of diodes will also be different. Figure 9.10 shows typical I–V characteristics of a Schottky barrier diode and a pn junction diode. The effective turn-on voltage of the Schottky diode is less than that of the pn junction diode. 

Objective: Calculate the forward-bias voltage required to induce a forward-bias current density of 10 A/cm2 in a Schottky barrier diode and a pn junction diode. 

Consider diodes with the parameters given in Example 9.5. We can assume that the pn junction diode will be suffi ciently forward biased so that the ideal diffusion current will dominate. Let $T = 3 0 0 \mathrm { K } .$ . 

# Solution

For the Schottky barrier diode, we have 

$$
J = J _ {s T} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right]
$$

Neglecting the (1) term, we can solve for the forward-bias voltage. We fi nd 

$$
V _ {a} = \left(\frac {k T}{e}\right) \ln \left(\frac {J}{J _ {s T}}\right) = V _ {t} \ln \left(\frac {J}{J _ {s T}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0}{5 . 9 8 \times 1 0 ^ {- 5}}\right) = 0. 3 1 2 \mathrm{V}
$$

For the pn junction diode, we have 

$$
V _ {a} = V _ {t} \ln \left(\frac {J}{J _ {s}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0}{3 . 6 6 \times 1 0 ^ {- 1 1}}\right) = 0. 6 8 2 \mathrm{V}
$$

# ■ Comment

A comparison of the two forward-bias voltages shows that the Schottky barrier diode has a turn-on voltage that, in this case, is approximately 0.37 V smaller than the turn-on voltage of the pn junction diode. 

# ■ EXERCISE PROBLEM

Ex 9.6 A pn junction diode and a Schottky diode have equal cross-sectional areas and have forward-bias currents of 0.5 mA. The reverse-saturation current of the Schottky diode is $5 \times 1 0 ^ { - 7 } \mathrm { A }$ . The difference in forward-bias voltage between the two diodes is 0.30 V. Determine the reverse-saturation current of the pn junction diode. 

$$
(\mathrm{Ans.} 4. 6 6 \times 1 0 ^ {- 1 2} \mathrm{A})
$$

The actual difference between the turn-on voltages will be a function of the barrier height of the metal–semiconductor contact and the doping concentrations in the pn junction, but the relatively large difference will always be realized. We will consider one application that utilizes the difference in turn-on voltage in Chapter 12, in what is referred to as a Schottky clamped transistor. 

The second major difference between a Schottky barrier diode and a pn junction diode is in the frequency response, or switching characteristics. In our discussion, we have considered the current in a Schottky diode as being due to the injection of majority carriers over a potential barrier. The energy-band diagram of Figure 9.1, for example, shows that there can be electrons in the metal directly adjacent to empty states in the semiconductor. If an electron from the valence band of the semiconductor were to fl ow into the metal, this effect would be equivalent to holes being injected into the semiconductor. This injection of holes would create excess minority carrier holes in the n region. However, calculations as well as measurements have shown that the ratio of the minority carrier hole current to the total current is extremely low in most cases. 

The Schottky barrier diode, then, is a majority carrier device. This fact means that there is no diffusion capacitance associated with a forward-biased Schottky diode. The elimination of the diffusion capacitance makes the Schottky diode a higherfrequency device than the pn junction diode. Also, when switching a Schottky diode from forward to reverse bias, there is no minority carrier stored charge to remove, as is the case in the pn junction diode. Since there is no minority carrier storage time, the Schottky diodes can be used in fast-switching applications. A typical switching time for a Schottky diode is in the picosecond range, while for a pn junction it is normally in the nanosecond range. 

# TEST YOUR UNDERSTANDING

TYU 9.4 (a) The reverse-saturation currents of a pn junction and a Schottky diode are $1 0 ^ { - 1 4 } \mathrm { \ A }$ and $1 0 ^ { - 9 } \mathrm { A } .$ , respectively. Determine the required forward-bias voltages in the pn junction diode and Schottky diode to produce a current of 100 $\mu \mathrm { A }$ in each diode. (b) Repeat part (a) for forward bias currents of 1 mA. ) 0.656 V, 0.358 V] b ) 0.596 V, 0.298 V; ( a [Ans. ( 

# 9.2 | METAL–SEMICONDUCTOR OHMIC CONTACTS

Contacts must be made between any semiconductor device, or integrated circuit, and the outside world. These contacts are made via ohmic contacts. Ohmic contacts are metal-to-semiconductor contacts, but in this case they are not rectifying contacts. An ohmic contact is a low-resistance junction providing conduction in both directions between the metal and the semiconductor. Ideally, the current through the ohmic contact is a linear function of applied voltage, and the applied voltage should be very small. Two general types of ohmic contacts are possible: The fi rst type is the ideal nonrectifying barrier, and the second is the tunneling barrier. We defi ne in this section a specifi c contact resistance that is used to characterize ohmic contacts. 

# 9.2.1 Ideal Nonrectifying Barrier

We have considered an ideal metal-n-type semiconductor contact in Figure 9.1 for the case when $\phi _ { m } > \phi _ { s }$ . Figure 9.11 shows the same ideal contact for the opposite case of $\phi _ { m } < \phi _ { s }$ . In Figure 9.11a we see the energy levels before contact, and in Figure 9.11b, the barrier after contact for thermal equilibrium. To achieve thermal equilibrium in this junction, electrons fl ow from the metal into the lower energy states in the semiconductor, which makes the surface of the semiconductor more n type. The excess electron charge in the n-type semiconductor exists essentially as a surface charge density. If a positive voltage is applied to the metal, there is no barrier to electrons fl owing from the semiconductor into the metal. If a positive voltage is applied to the semiconductor, the effective barrier height for electrons fl owing from the metal into the semiconductor will be approximately $\phi _ { B n } = \phi _ { n } .$ which is fairly small for a moderately to heavily doped semiconductor. For this bias condition, electrons can easily fl ow from the metal into the semiconductor. 

Figure 9.12a shows the energy-band diagram when a positive voltage is applied to the metal with respect to the semiconductor. Electrons can easily fl ow “downhill” 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/07b4df31fa9877d5e16b353169a54ddcd5af013004a2fa26e463cbfffcef3f37.jpg)



Figure 9.11 | Ideal energy-band diagram (a) before contact and (b) after contact for a metal-n-type semiconductor junction for $\phi _ { m } < \phi _ { s }$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/e21fc1b09243d2d0c287d5ae50d9ea370c18ec887314d04513b7d6ea033203de.jpg)



Figure 9.12 | Ideal energy-band diagram of a metal-n-type semiconductor ohmic contact (a) with a positive voltage applied to the metal and (b) with a positive voltage applied to the semiconductor.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/8a51e7668309a3508a26923f5a5f9c266c00a2215dce7302d847058fe0324305.jpg)



Figure 9.13 | Ideal energy-band diagram (a) before contact and (b) after contact for a metal–p-type semiconductor junction for $\phi _ { m } < \phi _ { s }$ .


from the semiconductor into the metal. Figure 9.12b shows the case when a positive voltage is applied to the semiconductor with respect to the metal. Electrons can easily fl ow over the barrier from the metal into the semiconductor. This junction, then, is an ohmic contact. 

Figure 9.13 shows an ideal nonrectifying contact between a metal and a p-type semiconductor. Figure 9.13a shows the energy levels before contact for the case when $\phi _ { m } > \phi _ { s }$ s. When contact is made, electrons from the semiconductor fl ow into the metal to achieve thermal equilibrium, leaving behind more empty states, or holes. The excess concentration of holes at the surface makes the surface of the semiconductor more p type. Electrons from the metal can readily move into the empty states in the semiconductor. This charge movement corresponds to holes fl owing from the semiconductor into the metal. We can also visualize holes in the metal fl owing into the semiconductor. This junction is also an ohmic contact. 

The ideal energy bands shown in Figures 9.11 and 9.13 do not take into account the effect of surface states. If we assume that acceptor surface states exist in the upper half of the semiconductor bandgap, then, since all the acceptor states are below $E _ { F }$ for the case shown in Figure 9.11b, these surface states will be negatively charged and will alter the energy-band diagram. Similarly, if we assume that donor surface states exist in the lower half of the bandgap, then all of the donor states will be positively charged for the case shown in Figure 9.13b; the positively charged surface states will also alter this energy-band diagram. Therefore, if $\phi _ { m } < \phi _ { : }$ s for the metal-n-type semiconductor contact, and if $\phi _ { m } > \phi _ { : }$ s for the metal–p-type semiconductor contact, we may not necessarily form a good ohmic contact. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/9f2d9d8ea9eb03518a7a69010df3a90e2474fc266e5835eba520aadafbb9b0d0.jpg)



Figure 9.14 | Energy-band diagram of a heavily doped n-semiconductor-tometal junction.


# 9.2.2 Tunneling Barrier

The space charge width in a rectifying metal–semiconductor contact is inversely proportional to the square root of the semiconductor doping. The width of the depletion region decreases as the doping concentration in the semiconductor increases; thus, as the doping concentration increases, the probability of tunneling through the barrier increases. Figure 9.14 shows a junction in which the metal is in contact with a heavily doped n-type epitaxial layer. 

Objective: Calculate the space charge width for a Schottky barrier on a heavily doped semiconductor. 

Consider silicon at T  300 K doped at $N _ { d } = 7 \times 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 } .$ . Assume a Shottky barrier with $\phi _ { B n } = 0 . 6 7 ~ \mathrm { V } .$ . For this case, we can assume that $V _ { b i } \approx \phi _ { B 0 }$ . Neglect the barrier lowering effect. 

# Solution

From Equation (9.7), we have for zero applied bias 

$$
x _ {n} = \left[ \frac {2 \epsilon_ {s} V _ {b i}}{e N _ {d}} \right] ^ {1 / 2} = \left[ \frac {2 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 6 7)}{(1 . 6 \times 1 0 ^ {- 1 9}) (7 \times 1 0 ^ {1 8})} \right] ^ {1 / 2}
$$

or 

$$
x _ {n} = 1. 1 \times 1 0 ^ {- 6} \mathrm{cm} = 1 1 0 \mathrm{A}
$$

EXAMPLE 9.7 

# ■ Comment

In a heavily doped semiconductor, the depletion width is on the order of angstroms, so that tunneling is now a distinct possibility. For these types of barrier widths, tunneling may become the dominant current mechanism. 

# ■ EXERCISE PROBLEM

Ex 9.7 Calculate the space charge width of a rectifying metal–GaAs–semiconductor junction. Assume the n-type doping concentration is $N _ { d } = 7 \times 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ and the built-in potential barrier is $V _ { b i } = 0 . 8 0 \mathrm { V } .$ . 

$$
(\text { Ans. } x _ {n} = 1 2 8. 7 \text {   A })
$$

The tunneling current has the form 

$$
J _ {t} \propto \exp \left(\frac {- e \phi_ {B n}}{\mathrm{E} _ {o o}}\right) \tag {9.29}
$$

where 

$$
\mathrm{E} _ {o o} = \frac {e \hbar}{2} \sqrt {\frac {N _ {d}}{\epsilon_ {s} m _ {n} ^ {*}}} \tag {9.30}
$$

The tunneling current increases exponentially with doping concentration. 

# 9.2.3 Specifi c Contact Resistance

A fi gure of merit of ohmic contacts is the specifi c contact resistance, Rc. This parameter is defi ned as the reciprocal of the derivative of current density with respect to voltage evaluated at zero bias. We may write 

$$
R _ {c} = \left. \left(\frac {\partial J}{\partial V}\right) ^ {- 1} \right| _ {V = 0} \quad \Omega - \mathrm{cm} ^ {2} \tag {9.31}
$$

We want Rc to be as small as possible for an ohmic contact. 

For a rectifying contact with a low to moderate semiconductor doping concentration, the current–voltage relation is given by Equation (9.23) as 

$$
J _ {n} = A ^ {*} T ^ {2} \exp \left(\frac {- e \phi_ {B n}}{k T}\right) \left[ \exp \left(\frac {e V}{k T}\right) - 1 \right]
$$

The thermionic emission current is dominant in this junction. The specifi c contact resistance for this case is then 

$$
R _ {c} = \frac {\left(\frac {k T}{e}\right) \exp \left(\frac {+ e \phi_ {B n}}{k T}\right)}{A ^ {*} T ^ {2}} \tag {9.32}
$$

The specifi c contact resistance decreases rapidly as the barrier height decreases. 

For a metal–semiconductor junction with a high impurity doping concentration, the tunneling process will dominate. From Equations (9.29) and (9.30), the specifi c contact resistance is found to be 

$$
R _ {c} \propto \exp \left(\frac {+ 2 \sqrt {\epsilon_ {s} m _ {n} ^ {*}}}{\hbar} \cdot \frac {\phi_ {B n}}{\sqrt {N _ {d}}}\right) \tag {9.33}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/af3b164d83ca9f3f84ad16bd739cacfcaf47da7781daf105cdb89b9e2ff67565.jpg)



Figure 9.15 | Theoretical and experimental specifi c contact resistance as a function of doping.



(From Sze and Ng [15].)


which shows that the specifi c contact resistance is a very strong function of semiconductor doping. 

Figure 9.15 shows a plot of the theoretical values of $R _ { c }$ as a function of semiconductor doping. For doping concentrations greater than approximately $1 0 ^ { 1 9 } \mathrm { c m } ^ { - 3 }$ , the tunneling process dominates and $R _ { c }$ shows the exponential dependence on $N _ { d } .$ For lower doping concentrations, the $R _ { c }$ values are dependent on the barrier heights and become almost independent of the doping. Also shown in the fi gure are experimental data for platinum silicide–silicon and aluminum–silicon junctions. 

Equation (9.33) is the specifi c contact resistance of the tunneling junction, which corresponds to the metal–n contact shown in Figure 9.14. However, the $\mathfrak { n } ^ { + } \mathfrak { n }$ junction also has a specifi c contact resistance, since there is a barrier associated with this junction. For a fairly low doped n region, this contact resistance may actually dominate the total resistance of the junction. 

The theory of forming ohmic contacts is straightforward. To form a good ohmic contact, we need to create a low barrier and use a highly doped semiconductor at the surface. However, the actual technology of fabricating good, reliable ohmic contacts is not as easy in practice as in theory. It is also more diffi cult to fabricate good ohmic contacts on wide-bandgap materials. In general, low barriers are not possible on these materials, so a heavily doped semiconductor at the surface must be used to form a tunneling contact. The formation of a tunneling junction requires diffusion, ion implantation, or perhaps epitaxial growth. The surface doping concentration in the semiconductor may be limited to the impurity solubility, which is approximately $5 \times 1 0 ^ { 1 9 } \mathrm { c m } ^ { - 3 }$ for n-type GaAs. Nonuniformities in the surface doping concentration may also prevent the theoretical limit of the specifi c contact resistance from being reached. In practice, a good deal of empirical processing is usually required before a good ohmic contact is obtained. 

# 9.3 | HETEROJUNCTIONS

In the discussion of pn junctions in the previous chapters, we assumed that the semiconductor material is homogeneous throughout the structure. This type of junction is called a homojunction. When two different semiconductor materials are used to form a junction, the junction is called a semiconductor heterojunction. 

As with many topics in this text, our goal is to provide the basic concepts concerning the heterojunction. The complete analysis of heterojunction structures involves quantum mechanics and detailed calculations that are beyond the scope of this text. The discussion of heterojunctions will, then, be limited to the introduction of some basic concepts. 

# 9.3.1 Heterojunction Materials

Since the two materials used to form a heterojunction will have different energy bandgaps, the energy band will have a discontinuity at the junction interface. We may have an abrupt junction in which the semiconductor changes abruptly from a narrow-bandgap material to a wide-bandgap material. On the other hand, if we have $\mathrm { a } \operatorname { G a A s - A l } _ { x } \mathrm { G a } _ { 1 - x } \mathrm { A s }$ system, for example, the value of x may continuously vary over a distance of several nanometers to form a graded heterojunction. Changing the value of x in the $\mathbf { A l } _ { x } \mathbf { G a } _ { 1 - x } \mathbf { A } \mathbf { s }$ s system allows us to engineer, or design, the bandgap energy. 

In order to have a useful heterojunction, the lattice constants of the two mate rials must be well matched. The lattice match is important because any lattice mismatch can introduce dislocations resulting in interface states. For example, germanium and gallium arsenide have lattice constants matched to within approximately 0.13 percent. Germanium–gallium arsenide heterojunctions have been studied quite extensively. More recently, gallium arsenide–aluminum gallium arsenide (GaAs–AlGaAs) junctions have been investigated quite thoroughly, since the lattice constants of GaAs and the AlGaAs system vary by no more than 0.14 percent. 

# 9.3.2 Energy-Band Diagrams

In the formation of a heterojunction with a narrow-bandgap material and a widebandgap material, the alignment of the bandgap energies is important in determining the characteristics of the junction. Figure 9.16 shows three possible situations. In Figure 9.16a, we see the case when the forbidden bandgap of the wide-gap material completely overlaps the bandgap of the narrow-gap material. This case, called straddling, applies to most heterojunctions. We consider only this case here. The other possibilities are called staggered and broken gap and are shown in Figure 9.16b,c. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/f972d1d0633eced78a728f330ee04a9694216b42147bbb414e33dd81dc5119e3.jpg)



Figure 9.16 | Relation between narrow-bandgap and wide-bandgap energies: (a) straddling, (b) staggered, and (c) broken gap.


There are four basic types of heterojunction. Those in which the dopant type changes at the junction are called anisotype. We can form nP or Np junctions, where the capital letter indicates the larger-bandgap material. Heterojunctions with the same dopant type on either side of the junction are called isotype. We can form nN and pP isotype heterojunctions. 

Figure 9.17 shows the energy-band diagrams of isolated n-type and P-type materials, with the vacuum level used as a reference. The electron affi nity of the wide-bandgap material is less than that of the narrow-bandgap material. The difference between the two conduction band energies is denoted by $\Delta E _ { c }$ , and the difference between the two valence band energies is denoted by $\Delta E _ { v }$ . From Figure 9.17, we can see that 

$$
\Delta E _ {c} = e (\chi_ {n} - \chi_ {P}) \tag {9.34a}
$$

and 

$$
\Delta E _ {c} + \Delta E _ {v} = E _ {g P} - E _ {g n} = \Delta E _ {g} \tag {9.34b}
$$

In the ideal abrupt heterojunction using nondegenerately doped semiconductors, the vacuum level is parallel to both conduction bands and valence bands. If the vacuum level is continuous, then the same $\Delta E _ { c }$ and $\Delta E _ { v }$ discontinuities will exist at the heterojunction interface. This ideal situation is known as the electron affi nity rule. There is still some uncertainty about the applicability of this rule, but it provides a good starting point for the discussion of heterojunctions. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/4484a35635bdfbc978a97c7d085304fb3ee24714f7bebe62f909759069ec03bd.jpg)



Figure 9.17 | Energy-band diagrams of a narrow-bandgap and a wide-bandgap material before contact.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/e77f181d10342d01c15ddeff8cafd60928d3a5241f4c3e115951e923e5f3e95f.jpg)



Figure 9.18 | Ideal energy-band diagram of an nP heterojunction in thermal equilibrium.


Figure 9.18 shows a general ideal nP heterojunction in thermal equilibrium. In order for the Fermi levels in the two materials to become aligned, electrons from the narrow-gap n region and holes from the wide-gap P region must fl ow across the junction. As in the case of a homojunction, this fl ow of charge creates a space charge region in the vicinity of the metallurgical junction. The space charge width into the n-type region is denoted by $x _ { n }$ and the space charge width into the P-type region is denoted by $x _ { P } .$ The discontinuities in the conduction and valence bands and the change in the vacuum level are shown in the fi gure. 

# 9.3.3 Two-Dimensional Electron Gas

Before we consider the electrostatics of the heterojunction, we will discuss a unique characteristic of an isotype junction. Figure 9.19 shows the energy-band diagram of an nN GaAs–AlGaAs heterojunction in thermal equilibrium. The AlGaAs can be moderately to heavily doped n type, while the GaAs can be more lightly doped or even intrinsic. As mentioned previously, to achieve thermal equilibrium, electrons from the wide-bandgap AlGaAs fl ow into the GaAs, forming an accumulation layer of electrons in the potential well adjacent to the interface. One basic quantummechanical result that we have found previously is that the energy of an electron contained in a potential well is quantized. The phrase two-dimensional electron gas refers to the condition in which the electrons have quantized energy levels in one spatial direction (perpendicular to the interface), but are free to move in the other two spatial directions. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/840f2a04a641089935b69b1422864542cd1f857887d95b1378fad69354e43f48.jpg)



Figure 9.19 | Ideal energy-band diagram of an nN heterojunction in thermal equilibrium.


The potential function near the interface can be approximated by a triangular potential well. Figure 9.20a shows the conduction band edges near the abrupt junction interface and Figure 9.20b shows the approximation of the triangular potential well. We can write 

$$
V (x) = e \mathrm{E} z \quad z > 0 \tag {9.35a}
$$

$$
V (z) = \infty \quad z <   0 \tag {9.35b}
$$

Schrodinger’s wave equation can be solved using this potential function. The quantized energy levels are shown in Figure 9.20b. Higher energy levels are usually not considered. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/bfa30ae3b2dd3ce18bbba333dee068dc5c0169abb2e44da1b8b39fcdcf0139b9.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/cc7b442943132794de56254e4dc6f0168ce225453527bf5abb3eb02088b96de6.jpg)



Figure 9.20 | (a) Conduction-band edge at N-AlGaAs, n-GaAs heterojunction; (b) triangular well approximation with discrete electron energies.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/258056d0f82ef44c0185d2ef1429c536f995eca67c686fbe33bbf5cffba4c228.jpg)



Figure 9.21 | Electron density in triangular potential well.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/878534884d7feee0848f8763a5e0248213732e7317e5d5fc77df03e91c4ed80e.jpg)



Figure 9.22 | Conduction-band edge at a graded heterojunction.


The qualitative distribution of electrons in the potential well is shown in Fig ure 9.21. A current parallel to the interface will be a function of this electron concentration and of the electron mobility. Since the GaAs can be lightly doped or intrinsic, the two-dimensional electron gas is in a region of low impurity doping so that impurity scattering effects are minimized. The electron mobility will be much larger than if the electrons were in the same region as the ionized donors. 

The movement of the electrons parallel to the interface will still be infl uenced by the coulomb attraction of the ionized impurities in the AlGaAs. The effect of these forces can be further reduced by using a graded AlGaAs–GaAs heterojunction. The graded layer is $\mathbf { A l } _ { x } \mathbf { G a } _ { 1 - x } \mathbf { A s }$ in which the mole fraction x varies with distance. In this case, an intrinsic layer of graded AlGaAs can be sandwiched between the N-type AlGaAs and the intrinsic GaAs. Figure 9.22 shows the conduction-band edges across a graded AlGaAs–GaAs heterojunction in thermal equilibrium. The electrons in the potential well are further separated from the ionized impurities so that the electron mobility is increased above that in an abrupt heterojunction. 

# *9.3.4 Equilibrium Electrostatics

We now consider the electrostatics of the nP heterojunction that is shown in Figure 9.18. As in the case of the homojunction, potential differences exist across the space charge regions in both the n region and the P region. These potential differences correspond to the built-in potential barriers on either side of the junction. The built-in potential barrier for this ideal case is defi ned as shown in Figure 9.18 to be the potential difference across the vacuum level. The built-in potential barrier is the sum of the potential differences across each of the space charge regions. The heterojunction built-in potential barrier, however, is not equal to the difference between the conduction bands across the junction or the difference between the valence bands across the junction, as we defi ned for the homojunction. 

Ideally, the total built-in potential barrier $V _ { b i }$ can be found as the difference between the work functions, or 

$$
V _ {b i} = \phi_ {s P} - \phi_ {s n} \tag {9.36}
$$

Equation (9.36), from Figure 9.17, can be written as 

$$
e V _ {b i} = \left[ e \chi_ {P} + E _ {g P} - \left(E _ {F P} - E _ {v P}\right) \right] - \left[ e \chi_ {n} + E _ {g n} - \left(E _ {F n} - E _ {v n}\right) \right] \tag {9.37a}
$$

or 

$$
e V _ {b i} = e (\chi_ {P} - \chi_ {n}) + (E _ {g P} - E _ {g n}) + (E _ {F n} - E _ {v n}) - (E _ {F P} - E _ {v P}) \tag {9.37b}
$$

which can be expressed as 

$$
e V _ {b i} = - \Delta E _ {c} + \Delta E _ {g} + k T \ln \left(\frac {N _ {v n}}{p _ {n o}}\right) - k T \ln \left(\frac {N _ {v P}}{p _ {p o}}\right) \tag {9.38}
$$

Finally, we can write Equation (9.38) as 

$$
e V _ {b i} = \Delta E _ {v} + k T \ln \left(\frac {p _ {p o}}{p _ {n o}} \cdot \frac {N _ {v n}}{N _ {v P}}\right) \tag {9.39}
$$

where $p _ { p o }$ and $p _ { n o }$ are the hole concentrations in the P and n materials, respectively, and $N _ { v n }$ and $N _ { v P }$ are the effective density of states functions in the n and P mate rials, respectively. We can also obtain an expression for the built-in potential barrier in terms of the conduction band shift as 

$$
e V _ {b i} = - \Delta E _ {c} + k T \ln \left(\frac {n _ {n o}}{n _ {p o}} \cdot \frac {N _ {c P}}{N _ {c n}}\right) \tag {9.40}
$$

Objective: Determine $\Delta E _ { c } , \Delta E _ { v }$ , and $V _ { b i }$ for an n–Ge to P–GaAs heterojunction using the electron affi nity rule. 

Consider n-type Ge doped with $N _ { d } ~ = ~ 1 0 ^ { 1 6 } ~ \mathrm { c m } ^ { - 3 }$ and P-type GaAs doped with $N _ { a } { = } ~ 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ . Let T  300 K so that $n _ { i } = 2 . 4 \times 1 0 ^ { 1 3 } \mathrm { c m } ^ { - 3 }$ for Ge. 

# Solution

From Equation (9.34a), we have 

$$
\Delta E _ {c} = e \left(\chi_ {n} - \chi_ {P}\right) = e (4. 1 3 - 4. 0 7) = 0. 0 6 \mathrm{eV}
$$

and from Equation (9.34b), we have 

$$
\Delta E _ {v} = \Delta E _ {g} - \Delta E _ {c} = (1. 4 3 - 0. 6 7) - 0. 0 6 = 0. 7 0 \mathrm{eV}
$$

To determine $V _ { b i }$ using Equation (9.39), we need to determine $p _ { n o }$ in Ge, or 

$$
p _ {n o} = \frac {n _ {i} ^ {2}}{N _ {d}} = \frac {(2 . 4 \times 1 0 ^ {1 3}) ^ {2}}{1 0 ^ {1 6}} = 5. 7 6 \times 1 0 ^ {1 0} \mathrm{cm} ^ {- 3}
$$

Then 

$$
e V _ {b i} = 0. 7 0 + (0. 0 2 5 9) \ln \left[ \frac {(1 0 ^ {1 6}) (6 \times 1 0 ^ {1 8})}{(5 . 7 6 \times 1 0 ^ {1 0}) (7 \times 1 0 ^ {1 8})} \right]
$$

or, fi nally, 

$$
V _ {b i} \approx 1. 0 \mathrm{V}
$$

# ■ Comment

There is a nonsymmetry in the $\Delta E _ { c }$ and $\Delta E _ { v }$ values that will tend to make the potential barriers seen by electrons and holes different. This nonsymmetry does not occur in homojunctions. 

# ■ EXERCISE PROBLEM

Ex 9.8 Repeat Example 9.8 for an n-Ge-to-P-GaAs heterojunction. The Ge is doped with $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ donors and the GaAs doped with $N _ { a } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ acceptors. Let 

$$
T = 3 0 0 \mathrm{K}. (\Lambda 6 8 8 \cdot 0 = ^ {i q} \Lambda \cdot \mathrm{suV})
$$

We can determine the electric fi eld and potential in the junction from Poisson’s equation in exactly the same way as we do for the homojunction. For homogeneous doping on each side of the junction, we have in the n region 

$$
\mathrm{E} _ {n} = \frac {e N _ {d n}}{\epsilon_ {n}} (x _ {n} + x) \quad (- x _ {n} \leq x <   0) \tag {9.41a}
$$

and in the P region 

$$
\mathrm{E} _ {P} = \frac {e N _ {a P}}{\epsilon_ {P}} (x _ {P} - x) \quad (0 <   x \leq x _ {P}) \tag {9.41b}
$$

where $\epsilon _ { n }$ and $\epsilon _ { P }$ are the permittivities of the n and P materials, respectively. We may note that $\mathrm { E } _ { n } = 0$ at $x = - x _ { n }$ and $\mathrm { E } _ { P } = 0$ at $x = x _ { P } .$ The electric fl ux density D is continuous across the junction, so 

$$
\epsilon_ {n} \mathrm{E} _ {n} (x = 0) = \epsilon_ {P} \mathrm{E} _ {P} (x = 0) \tag {9.42a}
$$

which gives 

$$
N _ {d n} x _ {n} = N _ {a P} x _ {P} \tag {9.42b}
$$

Equation (9.42b) simply states that the net negative charge in the P region is equal to the net positive charge in the n region—the same condition we had in a pn homojunction. We are neglecting any interface states that may exist at the heterojunction. 

The electric potential can be found by integrating the electric fi eld through the space charge region so that the potential difference across each region can be determined. We fi nd that 

$$
V _ {b i n} = \frac {e N _ {d n} x _ {n} ^ {2}}{2 \epsilon_ {n}} \tag {9.43a}
$$

and 

$$
V _ {b i P} = \frac {e N _ {a P} x _ {P} ^ {2}}{2 \epsilon_ {P}} \tag {9.43b}
$$

Equation (9.42b) can be rewritten as 

$$
\frac {x _ {n}}{x _ {P}} = \frac {N _ {a P}}{N _ {d n}} \tag {9.44}
$$

The ratio of the built-in potential barriers can then be determined as 

$$
\frac {V _ {\text { bin }}}{V _ {\text { biP }}} = \frac {\epsilon_ {P}}{\epsilon_ {n}} \cdot \frac {N _ {\text { dn }}}{N _ {\text { aP }}} \cdot \frac {x _ {n} ^ {2}}{x _ {P} ^ {2}} = \frac {\epsilon_ {P} N _ {\text { aP }}}{\epsilon_ {n} N _ {\text { dn }}} \tag {9.45}
$$

Assuming that $\epsilon _ { n }$ and $\epsilon _ { P }$ are of the same order of magnitude, the larger potential difference is across the lower-doped region. 

The total built-in potential barrier is 

$$
V _ {b i} = V _ {b i n} + V _ {b i P} = \frac {e N _ {d n} x _ {n} ^ {2}}{2 \epsilon_ {n}} + \frac {e N _ {a P} x _ {P} ^ {2}}{2 \epsilon_ {P}} \tag {9.46}
$$

If we solve for $x _ { P } ,$ , for example, from Equation (9.42b) and substitute into Equation (9.46), we can solve for $x _ { n }$ as 

$$
x _ {n} = \left[ \frac {2 \epsilon_ {n} \epsilon_ {P} N _ {a P} V _ {b i}}{e N _ {d n} (\epsilon_ {n} N _ {d n} + \epsilon_ {P} N _ {a P})} \right] ^ {1 / 2} \tag {9.47a}
$$

We can also fi nd 

$$
x _ {P} = \left[ \frac {2 \epsilon_ {n} \epsilon_ {P} N _ {d n} V _ {b i}}{e N _ {a P} (\epsilon_ {n} N _ {d n} + \epsilon_ {P} N _ {a P})} \right] ^ {1 / 2} \tag {9.47b}
$$

The total depletion width is found to be 

$$
W = x _ {n} + x _ {P} = \left[ \frac {2 \epsilon_ {n} \epsilon_ {P} (N _ {d n} + N _ {a P}) ^ {2} V _ {b i}}{e N _ {d n} N _ {a P} (\epsilon_ {n} N _ {d n} + \epsilon_ {P} N _ {a P})} \right] ^ {1 / 2} \tag {9.48}
$$

If a reverse-biased voltage is applied across the heterojunction, the same equations apply if $V _ { b i }$ is replaced by $V _ { b i } + V _ { R }$ . Similarly, if a forward bias is applied, the same equations also apply if $V _ { b i }$ is replaced by $V _ { b i } - V _ { a \cdot }$ . As explained earlier, $V _ { R }$ is the magnitude of the reverse-biased voltage and $V _ { a }$ is the magnitude of the forward-bias voltage. 

As in the case of a homojunction, a change in depletion width with a change in junction voltage yields a junction capacitance. We can fi nd for the nP junction 

$$
C _ {j} ^ {\prime} = \left[ \frac {e N _ {d n} N _ {a P} \epsilon_ {n} \epsilon_ {P}}{2 (\epsilon_ {n} N _ {d n} + \epsilon_ {P} N _ {a P}) (V _ {b i} + V _ {R})} \right] ^ {1 / 2} \quad (\mathrm{F/cm} ^ {2}) \tag {9.49}
$$

A plot of $( 1 / C _ { j } ^ { \prime } ) ^ { 2 }$ versus $V _ { R }$ again yields a straight line. The extrapolation of this plot of $( 1 / C _ { i } ^ { \prime } ) ^ { 2 } = 0 $ is used to fi nd the built-in potential barrier, $V _ { b i }$ . 

Figure 9.18 shows the ideal energy-band diagram for the nP abrupt heterojunction. The experimentally determined values of $\Delta E _ { c }$ and $\Delta E _ { v }$ may differ from the ideal values determined using the electron affi nity rule. One possible explanation for this difference is that most heterojunctions have interface states. If we assume that the electrostatic potential is continuous through the junction, then the electric fl ux density will be discontinuous at the heterojunction due to the surface charge trapped in the interface states. The interface states will then change the energy-band diagram of the semiconductor heterojunction just as they changed the energy-band diagram of the metal–semiconductor junction. Another possible explanation for the deviation from the ideal is that as the two materials are brought together to form the heterojunction, the electron orbitals of each material begin to interact with each other, resulting in a transition region of a few angstroms at the interface. The energy bandgap is then continuous through this transition region and not a characteristic of either material. However, we still have the relation 

$$
\Delta E _ {c} + \Delta E _ {v} = \Delta E _ {g} \tag {9.50}
$$

for the straddling type of heterojunction, although the $\Delta E _ { c }$ and $\Delta E _ { v }$ values may differ from those determined from the electron affi nity rule. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/81c501b2cff6a2dd4a0ba96ccdd0b7738f2d7cf4d2334db70e31de3e13c942bb.jpg)



Figure 9.23 | Ideal energy-band diagram of an Np heterojunction in thermal equilibrium.


We may consider the general characteristics of the energy-band diagrams of the other types of heterojunction. Figure 9.23 shows the energy-band diagram of an Np heterojunction. The same Ec and Ev discontinuities exist, although the general shape of the conduction band, for example, is different in the nP and the Np junctions. This difference in energy bands will infl uence the I–V characteristics of the two junctions. 

The other two types of heterojunctions are the nN and the $\mathsf { p P }$ isotype junctions. The energy-band diagram of the nN junction is shown in Figure 9.19. To achieve thermal equilibrium, electrons from the wide-bandgap material will fl ow into the narrowbandgap material. A positive space charge region exists in the wide-bandgap material and an accumulation layer of electrons now exists at the interface in the narrow-bandgap material. Since there are a large number of allowed energy states in the conduction band, we expect the space charge width $x _ { n }$ and the built-in potential barrier $V _ { b i n }$ to be small in the narrow-gap material. The energy-band diagram of the pP heterojunction in thermal equilibrium is shown in Figure 9.24. To achieve thermal equilibrium, holes from the wide-bandgap material will fl ow into the narrow-bandgap material, creating an accumulation layer of holes in the narrow-bandgap material at the interface. These types of isotype heterojunctions are obviously not possible in a homojunction. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/1414ab7c863b2e707cfe171cf75bb47a2449c0fedaf397295c521eadff11c3cd.jpg)



Figure 9.24 | Ideal energy-band diagram of a $\mathsf { p P }$ heterojunction in thermal equilibrium.


# *9.3.5 Current–Voltage Characteristics

The ideal current–voltage characteristics of a pn homojunction have been developed in Chapter 8. Since the energy-band diagram of a heterojunction is more complicated than that of a homojunction, we would expect the I–V characteristics of the two junctions to differ. 

One immediate difference between a homojunction and a heterojunction is in the barrier heights seen by the electrons and holes. Since the built-in potential barrier for electrons and holes in a homojunction is the same, the relative magnitude of the electron and hole currents is determined by the relative doping levels. In a heterojunction, the barrier heights seen by electrons and holes are not the same. The energy-band diagrams in Figures 9.18 and 9.23 demonstrate that the barrier heights for electrons and holes in a heterojunction can be signifi cantly different. The barrier height for electrons in Figure 9.18 is larger than that for holes, so we would expect the current due to electrons to be insignifi cant compared to the hole current. If the barrier height for electrons is 0.2 eV larger than that for holes, the electron current will be approximately a factor of 104 smaller than the hole current, assuming all other parameters are equal. The opposite situation exists for the band diagram shown in Figure 9.23. 

The conduction-band edge in Figure 9.23 and the valence-band edge in Figure 9.18 are somewhat similar to that of a rectifying metal–semiconductor contact. We derive the current–voltage characteristics of a heterojunction, in general, on the basis of thermionic emission of carriers over the barrier, as we do in the case of metal–semiconductor junction. We can then write 

$$
J = A ^ {*} T ^ {2} \exp \left(\frac {- E _ {w}}{k T}\right) \tag {9.51}
$$

where Ew is an effective barrier height. The barrier height can be increased or reduced by an applied potential across the junction as in the case of a pn homojunction or a Schottky barrier junction. The heterojunction I–V characteristics, however, may need to be modifi ed to include diffusion effects and tunneling effects. Another complicating factor is that the effective mass of a carrier changes from one side of the junction to the other. Although the actual derivation of the I–V relationship of the heterojunction is complex, the general form of the I–V equation is still similar to that of a Schottky barrier diode and is generally dominated by one type of carrier. 

# 9.4 | SUMMARY

■ A metal on a lightly doped semiconductor can produce a rectifying contact that is known as a Schottky barrier diode. The ideal barrier height between the metal and semiconductor is the difference between the metal work function and the semiconductor electron affi nity. 

■ When a positive voltage is applied to an n-type semiconductor with respect to the metal (reverse bias), the barrier between the semiconductor and metal increases so that there is essentially no fl ow of charged carriers. When a positive voltage is applied to the metal with respect to an n-type semiconductor (forward bias), the barrier between the semi conductor and metal is lowered so that electrons can easily fl ow from the semi conductor into the metal by a process called thermionic emission. 

■ The ideal current–voltage relationship of the Schottky barrier diode is the same as that of the pn junction diode. However, since the current mechanism is different from that of the pn junction diode, the switching speed of the Schottky diode is faster. In addition, the reverse saturation current of the Schottky diode is larger than that of the pn junction diode, so a Schottky diode requires less forward bias voltage to achieve a given current compared to a pn junction diode. 

■ Metal–semiconductor junctions can also form ohmic contacts, which are low-resistance junctions providing conduction in both directions with very little voltage drop across the junction. 

■ Semiconductor heterojunctions are formed between two semiconductor materials with different bandgap energies. One useful property of a heterojunction is the creation of a potential well at the interface. Electrons are confi ned to the potential well in the direction perpendicular to the interface, but are free to move in the other two directions. 

# GLOSSARY OF IMPORTANT TERMS

anisotype junction A heterojunction in which the type of dopant changes at the metallurgical junction. 

electron affi nity rule The rule stating that, in an ideal heterojunction, the discontinuity at the conduction band is the difference between the electron affi nities in the two semiconductors. 

heterojunction The junction formed by the contact between two different semiconductor materials. 

image force–induced lowering The lowering of the peak potential barrier at the metal– semiconductor junction due to an electric fi eld. 

isotype junction A heterojunction in which the type of dopant is the same on both sides of the junction. 

ohmic contact A low-resistance metal–semiconductor contact providing conduction in both directions between the metal and semiconductor. 

Richardson constant The parameter A* in the current–voltage relation of a Schottky diode. 

Schottky barrier height The potential barrier -Bn from the metal to semiconductor in a metal–semiconductor junction. 

Schottky effect Another term for image force–induced lowering. 

specifi c contact resistance The inverse of the slope of the J versus V curve of a metal– semiconductor contact evaluated at V  0. 

thermionic emission The process by which charge fl ows over a potential barrier as a result of carriers with suffi cient thermal energy. 

tunneling barrier A thin potential barrier in which the current is dominated by the tunneling of carriers through the barrier. 

two-dimensional electron gas (2-DEG) The accumulation layer of electrons contained in a potential well at a heterojunction interface. The electrons are free to move in the “other” two spatial directions. 

# CHECKPOINT

After studying this chapter, the reader should have the ability to: 

■ Sketch the energy-band diagram of zero-biased, reverse-biased, and forward-biased Schottky barrier diodes. 

■ Describe the charge fl ow in a forward-biased Schottky barrier diode. 

Explain the Schottky barrier lowering and its effect on the reverse saturation current in a Schottky barrier diode. 

■ Explain the effect of interface states on the characteristics of a Schottky barrier diode. 

■ Describe one effect of a larger reverse saturation current in a Schottky barrier diode compared to that of a pn junction diode. 

■ Describe what is meant by an ohmic contact. 

■ Draw the energy-band diagram of an nN heterojunction. 

■ Explain what is meant by a two-dimensional electron gas. 

# REVIEW QUESTIONS

1. What is the ideal Schottky barrier height? Indicate the Schottky barrier height on an energy-band diagram. 

2. Using an energy-band diagram, indicate the effect of the Schottky barrier lowering. 

3. What is the mechanism of charge fl ow in a forward-biased Schottky barrier diode? 

4. Compare the forward-biased current–voltage characteristic of a Schottky barrier diode to that of pn junction diode. 

5. Explain the difference in switching characteristics between a Schottky diode and a pn junction diode. Discuss charge storage effects. 

6. Sketch the ideal energy-band diagram of a metal–semiconductor junction in which $\phi _ { m } < \phi .$ s. Explain why this is an ohmic contact. 

7. Sketch the energy-band diagram of a tunneling junction. Why is this an ohmic contact? 

8. What is a heterojunction? 

9. What is a 2-D electron gas? 

# PROBLEMS

(In the following problems, assume $A ^ { * } = 1 2 0 \mathrm { A } / \mathrm { K } ^ { 2 } { \mathrm { - c m } } ^ { 2 }$ for silicon and $A ^ { * } = 1 . 1 2 \mathrm { A } / \mathrm { K } ^ { 2 } \mathrm { - } \mathrm { c m } ^ { 2 }$ for gallium arsenide Schottky diodes unless otherwise stated.) 

# Section 9. 1 The Schottky Barrier Diode

9.1 Consider a contact between Al and n Si doped at $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } . T = 3 0 0 \mathrm { K }$ 

(a) Draw the energy-band diagrams of the two materials before the junction is formed. (b) Draw the ideal energy band at zero bias after the junction is formed. (c) Calculate -B0, $x _ { d } ,$ and $\mathrm { E } _ { \mathrm { m a x } }$ for part (b). (d) Repeat parts (b) and (c) using the data in Figure 9.5. 

9.2 (a) A Schottky barrier diode formed on n-type silicon has a doping concentration of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and a barrier height of $\phi _ { B 0 } = 0 . 6 5 \ : \mathrm { V } .$ . Determine the builtin potential barrier $V _ { b i \bullet } \left( b \right)$ If the doping concentration changes to $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , determine the values of $\phi _ { B 0 }$ and $V _ { b i \cdot }$ Do these values increase, decrease, or remain the same? (c) Repeat part (b) if the doping concentration is $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

9.3 Gold is deposited on n-type silicon forming an ideal rectifying junction. The doping concentration is $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Assume $T = 3 0 0 \mathrm { K }$ . Determine the theoretical values of $( a ) \phi _ { B 0 } , ( b ) V _ { b i } ,$ and $( c ) x _ { n }$ and $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ at (i) $V _ { R } = 1 \mathrm { V }$ and (ii) $V _ { R } = 5 \mathrm { V } .$ 

9.4 A Schottky diode is formed by depositing gold on n-type GaAs that is doped at a concentration of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . For $T = 3 0 0 \mathrm { K }$ , determine the theoretical values of (a) $\phi _ { B 0 } , \left( b \right) \phi _ { n } , \left( c \right) V _ { b i } ,$ , and $( d ) x _ { n }$ and $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ at (i) $V _ { R } = 1 \mathrm { V }$ and (ii) $V _ { R } = 5 \mathrm { V } .$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/b7db3b9e1e72ec8d76be364fa0f9b05f172df2059581862d8b6374e738e63bd5.jpg)



Figure P9.7 | Figure for Problem 9.7.


9.5 Repeat Problem 9.4, parts (b) through $( d )$ , if the experimentally determined barrier height is found to be $\phi _ { B n } = 0 . 8 8 \mathrm { V } .$ 

9.6 (a) A Pt–n-type silicon junction with $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ has a cross-sectional area of $A = 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . Let $T = 3 0 0$ K. Using the data shown in Figure 9.5, determine the junction capacitance at $( i ) \ V _ { R } = 1 \ V$ and (ii) $V _ { R } = 5 \mathrm { V } . ( b )$ Repeat part (a) for a doping concentration of $N _ { d } = 1 0 ^ { 1 6 }$ cm3. 

9.7 A Schottky diode with n-type GaAs at $T = 3 0 0 \mathrm { K }$ yields the $1 / C ^ { \prime } { } ^ { 2 }$ versus $V _ { R }$ plot shown in Figure P9.7, where $C ^ { \prime }$ is the capacitance per cm2. Determine (a) $V _ { b i } , \left( b \right) N _ { d } ,$ (c) $\phi _ { n } ,$ and (d) $\phi _ { B 0 }$ . 

9.8 Consider a W–n-type silicon Schottky barrier at $T = 3 0 0 ~ \mathrm { K }$ with $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ Use the data in Figure 9.5 to determine the barrier height. (a) Determine $V _ { b i } , x _ { n } ,$ and $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ for (i) $V _ { R } = 1 \mathrm { V }$ and (ii) $V _ { R } = 5 \mathrm { V } . ( b )$ Using the values of $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ from part (a), determine the Schottky barrier lowering parameters $\Delta \phi$ and $x _ { m } .$ 

9.9 Starting with Equation (9.12), derive Equations (9.14) and (9.15). 

9.10 A Au-n-GaAs Schottky diode at $T = 3 0 0 \mathrm { K }$ is doped at a concentration of $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Use the data in Figure 9.5 to determine the barrier height. Then determine (a) $V _ { b i } , x _ { n } ,$ , and $\left| { \mathrm { E } } _ { \operatorname* { m a x } } \right|$ for zero bias. (b) Determine the reverse-biased voltage at which the Schottky barrier lowering, -, will be 5 percent of the barrier height. 

9.11 Consider n-type silicon doped at $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ with a gold contact to form a Schottky diode. Investigate the effect of Schottky barrier lowering. (a) Plot the Schottky barrier lowering $\Delta \phi$ versus reverse-biased voltage over the range $0 \leq V _ { R } \leq 5 0 \mathrm { V } .$ (b) Plot the ratio $J _ { s T } ( V _ { R } ) / J _ { s T } ( V _ { R } = 0 )$ over the same range of reversebiased voltage. 

*9.12 The energy-band diagram of a Schottky diode is shown in Figure 9.6. Assume the following parameters: 

$$
\phi_ {m} = 5. 2 \mathrm{V} \quad \phi_ {n} = 0. 1 0 \mathrm{V} \quad \phi_ {0} = 0. 6 0 \mathrm{V}
$$

$$
E _ {g} = 1. 4 3 \mathrm{eV} \quad \delta = 2 5 \mathrm{A} \quad \epsilon_ {i} = \epsilon_ {0}
$$

$$
\epsilon_ {s} = (1 3. 1) \epsilon_ {0} \quad \chi = 4. 0 7 \mathrm{V} \quad N _ {d} = 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}
$$

$$
D _ {i t} = 1 0 ^ {1 3} \mathrm{eV} ^ {- 1} \mathrm{cm} ^ {- 2}
$$

(a) Determine the theoretical barrier height $\phi _ { B 0 }$ without interface states. (b) Determine the barrier height with interface states. (c) Repeat parts (a) and (b) if $\phi _ { m } = 4 . 5 \ : \mathrm { V } .$ 

*9.13 A Schottky barrier diode contains interface states and an interfacial layer. Assume the following parameters: 

$$
\phi_ {m} = 4. 7 5 \mathrm{V} \quad \phi_ {n} = 0. 1 6 4 \mathrm{V} \quad \phi_ {0} = 0. 2 3 0 \mathrm{V}
$$

$$
E _ {g} = 1. 1 2 \mathrm{eV} \quad \delta = 2 0 \AA \quad \epsilon_ {i} = \epsilon_ {0}
$$

$$
\epsilon_ {s} = (1 1. 7) \epsilon_ {0} \quad \chi = 4. 0 1 \mathrm{V} \quad N _ {d} = 5 \times 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}
$$

$$
\phi_ {B 0} = 0. 6 0 \mathrm{V}
$$

Determine the interface state density, $D _ { i t } ,$ in units of $\mathrm { e V } ^ { - 1 } \mathrm { c m } ^ { - 2 } ,$ . 

9.14 A Schottky diode at $T = 3 0 0 \mathrm { K }$ is formed with Pt on n-type silicon with a doping concentration of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The barrier height is found to be $\phi _ { B n } = 0 . 8 9 \mathrm { V } .$ . Determine (a) $\phi _ { n } , ( b ) V _ { b i } , ( c ) J _ { s T } ,$ and (d) $V _ { a }$ such that $J _ { n } = 5 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . (Neglect the barrier lowering effect.) 

9.15 (a) Consider a Schottky diode at $T = 3 0 0 \mathrm { ~ k ~ }$ K that is formed with tungsten on n-type silicon. Use Figure 9.5 to determine the barrier height. Assume a doping concentration of $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and assume a cross-sectional area $A = 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . Determine the forward-bias voltage required to induce a current of $( i ) 1 0 \mu \mathrm { A } .$ , (ii) 100 $\mu \mathrm { A } .$ , and (iii) 1 mA. (b) Repeat part (a) for a temperature of $T = 3 5 0 \mathrm { K } .$ . (Neglect the barrier lowering effect.) 

9.16 An $\mathbf { A u - n - G a A s }$ Schottky diode at $T = 3 0 0 \mathrm { K }$ has a doping concentration of $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ . (a) Using Figure 9.5, determine the barrier height. (b) Calculate the reverse-biased saturation current $J _ { s T \star } \left( c \right)$ Determine the forward-bias voltage required to induce a current density of $J _ { n } = 1 0 \mathrm { A } / \mathrm { c m } ^ { 2 } .$ (d) What is the change in forwardbias voltage necessary to double the current density? (Neglect the Schottky barrier lowering.) 

9.17 (a) Consider an Au–n-type GaAs Schottky diode with a cross-sectional area of 104 cm2. Plot the forward-bias current–voltage characteristics over a voltage range of $0 \leq V _ { D } \leq 0 . 5 \ : \mathrm { V } .$ Plot the current on a log scale. (b) Repeat part (a) for an $_ \mathrm { A u - n - t y p e }$ silicon Schottky diode. (c) What conclusions can be drawn from these results? 

9.18 A Schottky diode at $T = 3 0 0 \mathrm { K }$ is formed between tungsten and n-type silicon doped at $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The cross-sectional area is $A = 1 0 ^ { - 4 }$ cm2. Determine the reverse-biased saturation current at (a) $V _ { R } = 2 \mathrm { V }$ and (b) $V _ { R } = 4 \mathrm { V } .$ . (Take into account the Schottky barrier lowering.) 

*9.19 Starting with the basic current equation given by Equation (9.18), derive the relation given by Equation (9.23). 

9.20 The reverse-saturation current densities in a pn junction diode and a Schottky diode are $1 0 ^ { - 1 1 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ and $6 \times 1 0 ^ { - 8 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ , respectively, at $T = 3 0 0 \mathrm { K } .$ . The cross-sectional area of the Schottky diode is $A = 1 0 ^ { - 4 }$ cm2. The current in each diode is 0.80 mA. The difference in forward-bias voltages between the two diodes is 0.285 V. Determine (a) the voltage applied to each diode and (b) the cross-sectional area of the pn junction diode. 

9.21 A pn junction diode and a Schottky diode each have cross-sectional areas of $A = 8 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . The reverse saturation current densities at $T = 3 0 0 \ \cdot$ K for the pn junction diode and Schottky diode are $8 \times 1 0 ^ { - 1 3 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ and $6 \times 1 0 ^ { - 9 } \mathrm { A } / \mathrm { c m } ^ { 2 } .$ , respectively. Determine the required forward-bias voltage in each diode to yields currents of (a)150 
A, (b) 700 $\mu \mathrm { A }$ , and (c) 1.2 mA. 

9.22 (a) The two diodes described in Problem 9.21 are connected in series and are driven by a constant current source of 0.80 mA. Determine (i) the current in each diode and (ii) the voltage across each diode. (b) Repeat part (a) for the case when the diodes are connected in parallel. 

9.23 A Schottky diode and a pn junction diode have cross-sectional areas of $A = 7 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . The reverse-saturation current densities at $T = 3 0 0 \mathrm { K }$ of the Schottky diode and pn junction are $4 \times 1 0 ^ { - 8 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ and $3 \times 1 0 ^ { - 1 2 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ , respectively. A forward-bias current of 0.8 mA is required in each diode. (a) Determine the forward-bias voltage required across each diode. (b) If the voltage from part (a) is maintained across each diode, determine the current in each diode if the temperature is increased to 400 K. (Take into account the temperature dependence of the reversesaturation currents. Assume $E _ { g } = 1 . 1 2 \mathrm { e V }$ for the pn junction diode and $\phi _ { B 0 } = 0 . 8 2 \ : \mathrm { V }$ for the Schottky diode.) 

9.24 Compare the current–voltage characteristics of a Schottky barrier diode and a pn junction diode. Use the results of Example 9.5 and assume diode areas of $5 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ . Plot the current–voltage characteristics on a linear scale over a current range of $0 \le I _ { D } \le 1 0 \mathrm { m A }$ . 

# Section 9.2 Metal–Semiconductor Ohmic Contacts

9.25 The contact resistance of an ohmic contact is $R _ { c } = 1 0 ^ { - 4 } \Omega { \mathrm { - c m } } ^ { 2 }$ . Determine the junction resistance if the cross-sectional area is (a) $1 0 ^ { - 3 } \mathrm { c m } ^ { 2 } , ( b ) 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 } .$ , and $( c ) 1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ . 

9.26 (a) The contact resistance of an ohmic contact is $R _ { c } = 5 \times 1 0 ^ { - 5 } \Omega { \mathrm { - c m } } ^ { 2 }$ . The crosssectional area of the junction is $1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ . Determine the voltage across the junction if the current is $( i ) I = 1$ mA and (ii) $I = 1 0 0 \mu \mathrm { A }$ . (b) Repeat part (a) if the crosssectional area is $1 0 ^ { - 6 } \mathrm { c m } ^ { 2 }$ . 

9.27 An ohmic contact between a metal and silicon may be formed that has a very low barrier height. (a) Determine the value of $\phi _ { B n }$ that will produce a contact resistance of $R _ { c } = 5 \times 1 0 ^ { - 5 } \Omega { \mathrm { - c m } } ^ { 2 }$ at $T = 3 0 0 \mathrm { K }$ . (b) Repeat part (a) for a contact resistance of $R _ { c } = 5 \times 1 0 ^ { - 6 } \Omega { \mathrm { - c m } } ^ { 2 }$ . 

9.28 A metal, with a work function $\phi _ { m } = 4 . 2 \ : \mathrm { V } ,$ is deposited on an n-type silicon semiconductor with $\chi _ { s } = 4 . 0 ~ \mathrm { V }$ and $E _ { g } = 1 . 1 2 \ : \mathrm { e V } .$ Assume no interface states exist at the junction. Let $T = 3 0 0 \mathrm { K } . ( a )$ Sketch the energy-band diagram for zero bias for the case when no space charge region exists at the junction. (b) Determine $N _ { d }$ so that the condition in part (a) is satisfi ed. (c) What is the potential barrier height seen by electrons in the metal moving into the semiconductor? 

9.29 Consider the energy-band diagram of a silicon Schottky junction under zero bias shown in Figure P9.29. Let $\phi _ { B 0 } = 0 . 7 \ : \mathrm { V }$ and $T = 3 0 0 \mathrm { K }$ . Determine the doping required so that $x _ { d } = 5 0 \mathrm { ~ \AA }$ at the point where the potential is $\phi _ { B 0 } / 2$ below the peak value. (Neglect the barrier lowering effect.) 

9.30 A metal–semiconductor junction is formed between a metal with a work function of 4.3 eV and p-type silicon with an electron affi nity of 4.0 eV. The acceptor doping concentration in the silicon is $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Assume $T = 3 0 0 \mathrm { K } . ( a )$ Sketch the thermal equilibrium energy-band diagram. (b) Determine the height of the Schottky barrier. (c) Sketch the energy-band diagram with an applied reverse-biased voltage of $V _ { R } = 3 { \mathrm { V } } . ( d )$ Sketch the energy-band diagram with an applied forward-bias voltage of $V _ { a } = 0 . 2 5 \ : \mathrm { V } .$ 

9.31 (a) Consider a metal–semiconductor junction formed between a metal with a work function of 4.65 eV and Ge with an electron affi nity of 4.13 eV. The doping 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-09/ee95e1ec-f455-4924-873f-aa798b33401a/2dcbc9ae99b9589f9aba08c061b853370cb4203dd17b6bddd3646a9e43ce983e.jpg)



Figure P9.29 | Figure for Problem 9.29.


concentration in the Ge material is $N _ { d } = 6 \times 1 0 ^ { 1 3 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 3 \times 1 0 ^ { 1 3 } \mathrm { c m } ^ { - 3 } .$ . Assume $T = 3 0 0 \mathrm { K }$ Sketch the zero bias energy-band diagram and determine the Schottky barrier height. (b) Repeat part (a) if the metal work function is 4.35 eV. 

# Section 9.3 Heterojunctions

9.32 Sketch the energy-band diagrams of an abrupt $\mathrm { A l _ { 0 . 3 } G a _ { 0 . 7 } A s { - } G a A s }$ hetero junction for: (a) N–AlGaAs, intrinsic GaAs, (b) $\mathrm { N ^ { + } { - } A l G a A s , p { - } G a A s , }$ and $( c ) \mathrm { P ^ { + } { - } A l G a A s , n ^ { + } { - } }$ GaAs. Assume $E _ { g } = 1 . 8 5 \mathrm { e V }$ for $\mathrm { { A l } _ { 0 . 3 } \mathrm { { G a } _ { 0 . 7 } \mathrm { { A s } } } }$ and assume $\begin{array} { r } { \Delta E _ { c } = \frac { 2 } { 3 } \Delta E _ { g } , } \end{array}$ . 

9.33 Repeat Problem 9.32 assuming the ideal electron affi nity rule. Determine $\Delta E _ { c }$ c and $\Delta E _ { v }$ . 

*9.34 Starting with Poisson’s equation, derive Equation (9.48) for an abrupt heterojunction. 

# Summary and Review

*9.35 (a) Derive an expression for $d V _ { a } / d T$ as a function of current density in a Schottky diode. Assume the minority carrier current is negligible. (b) Compare $d V _ { a } / d T$ for a GaAs Schottky diode to that for a Si Schottky diode. (c) Compare $d V _ { a } / d T$ for a Si Schottky diode to that for a Si pn junction diode. 

9.36 The $( 1 / C _ { j } ) ^ { 2 }$ versus $V _ { R }$ data are measured for two Schottky diodes with equal areas. One diode is fabricated with 1 -cm silicon and the other diode with 5 -cm silicon. The plots intersect the voltage axis as $V _ { R } = - 0 . 5 \ : \mathrm { V }$ for diode A and at $V _ { R } = - 1 . 0 \ : \mathrm { V }$ for diode B. The slope of the plot for diode A is $1 . 5 \times 1 0 ^ { 1 8 } ( \mathrm { F } ^ { 2 } \mathrm { - } \mathrm { V } ) ^ { - 1 }$ and that for diode B is $1 . 5 \times 1 0 ^ { 1 7 } ( \mathrm { F ^ { 2 } { - } V ) ^ { - 1 } }$ . Determine which diode has the higher metal work function and which diode has the lower resistivity silicon. 

*9.37 Both Schottky barrier diodes and ohmic contacts are to be fabricated by depositing a particular metal on a silicon integrated circuit. The work function of the metal is 4.5 V. Considering the ideal metal–semiconductor contact, determine the allowable range of doping concentrations for each type of contact. Consider both p- and n-type silicon regions. 

9.38 Consider an n-GaAs–p-AlGaAs heterojunction in which the bandgap offsets are $\Delta E _ { c } = 0 . 3 \mathrm { e V }$ and $\Delta E _ { v } = 0 .$ . 15 eV. Discuss the difference in the expected electron and hole currents when the junction is forward biased. 

# READING LIST



1. Anderson, R. L. “Experiments on Ge–GaAs Heterojunctions.” Solid-State Electronics 5, no. 5 (September–October 1962), pp. 341–351. 





2. Crowley, A. M., and S. M. Sze. “Surface States and Barrier Height of Metal– Semiconductor Systems.” Journal of Applied Physics 36 (1965), p. 3212. 





3. Hu, C. C. Modern Semiconductor Devices for Integrated Circuits. Upper Saddle River, NJ: Pearson Prentice Hall, 2010. 





4. MacMillan, H. F., H. C. Hamaker, G. F. Virshup, and J. G. Werthen. “Multijunction III-V Solar Cells: Recent and Projected Results.” Twentieth IEEE Photovoltaic Specialists Conference (1988), pp. 48–54. 





5. Michaelson, H. B. “Relation between an Atomic Electronegativity Scale and the Work Function.” IBM Journal of Research and Development 22, no. 1 (January 1978), pp. 72–80. 





6. Pierret, R. F. Semiconductor Device Fundamentals. Reading, MA: Addison-Wesley, 1996. 





7. Rideout, V. L. “A Review of the Theory, Technology and Applications of Metal–Semiconductor Rectifi ers.” Thin Solid Films 48, no. 3 (February 1, 1978), pp. 261–291. 





8. Roulston, D. J. Bipolar Semiconductor Devices. New York: McGraw-Hill, 1990. 





*9. Shur, M. GaAs Devices and Circuits. New York: Plenum Press, 1987. 





10. . Introduction to Electronic Devices. New York: John Wiley and Sons, 1996. 





*11. . Physics of Semiconductor Devices. Englewood Cliffs, NJ: Prentice Hall, 1990. 





*12. Singh, J. Physics of Semiconductors and Their Heterostructures. New York: McGraw-Hill, 1993. 





13. . Semiconductor Devices: Basic Principles. New York: John Wiley and Sons, 2001. 





14. Streetman, B. G., and S. K. Banerjee. Solid State Electronic Devices. 6th ed. Upper Saddle River, NJ: Pearson Prentice Hall, 2006. 





15. Sze, S. M., and K. K. Ng. Physics of Semiconductor Devices, 3rd ed. Hoboken, NJ: John Wiley and Sons, 2007. 





*16. Wang, S. Fundamentals of Semiconductor Theory and Device Physics. Englewood Cliffs, NJ: Prentice Hall, 1989. 





*17. Wolfe, C. M., N. Holonyak, Jr., and G. E. Stillman. Physical Properties of Semiconductors. Englewood Cliffs, NJ: Prentice Hall, 1989. 





18. Yang, E. S. Microelectronic Devices. New York: McGraw-Hill, 1988. 





*19. Yuan, J. S. SiGe, GaAs, and InP Heterojunction Bipolar Transistors. New York: John Wiley and Sons, 1999. 

