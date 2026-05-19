# Carrier Transport Phenomena

I n the previous chapter, we considered the semiconductor in equilibrium and de-termined electron and hole concentrations in the conduction and valence bands, respectively. A knowledge of the densities of these charged particles is important toward an understanding of the electrical properties of a semiconductor material. The net fl ow of the electrons and holes in a semiconductor will generate currents. The pro cess by which these charged particles move is called transport. In this chapter we consider two basic transport mechanisms in a semiconductor crystal: drift— the movement of charge due to electric fi elds, and diffusion—the fl ow of charge due to density gradients. 

The carrier transport phenomena are the foundation for fi nally determining the current–voltage characteristics of semiconductor devices. We will implicitly assume in this chapter that, although there will be a net fl ow of electrons and holes due to the transport processes, thermal equilibrium will not be substantially disturbed. Nonequilibrium processes are considered in the next chapter. ■ 

# 5.0 | PREVIEW

In this chapter, we will: 

■ Describe the mechanism of carrier drift and induced drift current due to an applied electric fi eld. 

■ Defi ne and describe the characteristics of carrier mobility. 

■ Describe the mechanism of carrier diffusion and induced diffusion current due to a gradient in the carrier concentration. 

■ Defi ne the carrier diffusion coeffi cient. 

■ Describe the effects of a nonuniform impurity doping concentration in a semiconductor material. 

■ Discuss and analyze the Hall effect in a semiconductor material. 

# 5.1 | CARRIER DRIFT

An electric fi eld applied to a semiconductor will produce a force on electrons and holes so that they will experience a net acceleration and net movement, provided there are available energy states in the conduction and valence bands. This net movement of charge due to an electric fi eld is called drift. The net drift of charge gives rise to a drift current. 

# 5.1.1 Drift Current Density

If we have a positive volume charge density $\rho$ moving at an average drift velocity $v _ { d } ,$ the drift current density is given by 

$$
J _ {d r f} = \rho v _ {d} \tag {5.1a}
$$

In terms of units, we have 

$$
J _ {d r f} = \left(\frac {\text { Coul }}{c m ^ {3}}\right) \cdot \left(\frac {c m}{s}\right) = \frac {\text { Coul }}{c m ^ {2} - s} = \frac {A}{c m ^ {2}} \tag {5.1b}
$$

If the volume charge density is due to positively charged holes, then 

$$
J _ {p \mid d r f} = (e p) v _ {d p} \tag {5.2}
$$

where ${ \cal J } _ { p \vert d r f }$ is the drift current density due to holes and $v _ { d p }$ is the average drift velocity of the holes. 

The equation of motion of a positively charged hole in the presence of an electric fi eld is 

$$
F = m _ {c p} ^ {*} a = e \mathrm{E} \tag {5.3}
$$

where e is the magnitude of the electronic charge, a is the acceleration, E is the electric fi eld, and $m _ { c p } ^ { * }$ is the conductivity effective mass of the hole.1 If the electric fi eld is constant, then we expect the velocity to increase linearly with time. However, charged particles in a semiconductor are involved in collisions with ionized impurity atoms and with thermally vibrating lattice atoms. These collisions, or scattering events, alter the velocity characteristics of the particle. 

As the hole accelerates in a crystal due to the electric fi eld, the velocity increases. When the charged particle collides with an atom in the crystal, for example, the particle loses most, or all, of its energy. The particle will again begin to accelerate and gain energy until it is again involved in a scattering process. This continues over and over again. Throughout this process, the particle will gain an average drift velocity which, for low electric fi elds, is directly proportional to the electric fi eld. We may then write 

$$
v _ {d p} = \mu_ {p} \mathrm{E} \tag {5.4}
$$

where $\mu _ { p }$ is the proportionality factor and is called the hole mobility. The mobility is an important parameter of the semiconductor since it describes how well a particle will move due to an electric fi eld. The unit of mobility is usually expressed in terms of $\mathrm { c m } ^ { 2 } / \mathrm { V } { \mathrm { - s } } .$ . 


Table 5.1 | Typical mobility values at T - 300 K and low doping concentrations


<table><tr><td></td><td><eq>\mu_n</eq> (cm2/V·s)</td><td><eq>\mu_p</eq> (cm2/V·s)</td></tr><tr><td>Silicon</td><td>1350</td><td>480</td></tr><tr><td>Gallium arsenide</td><td>8500</td><td>400</td></tr><tr><td>Germanium</td><td>3900</td><td>1900</td></tr></table>

By combining Equations (5.2) and (5.4), we may write the drift current density due to holes as 

$$
J _ {p \mid d r f} = (e p) v _ {d p} = e \mu_ {p} p E \tag {5.5}
$$

The drift current due to holes is in the same direction as the applied electric fi eld. 

The same discussion of drift applies to electrons. We may write 

$$
J _ {n \mid d r f} = \rho v _ {d n} = (- e n) v _ {d n} \tag {5.6}
$$

where $J _ { n | d r f }$ is the drift current density due to electrons and $v _ { d n }$ is the average drift velocity of electrons. The net charge density of electrons is negative. 

The average drift velocity of an electron is also proportional to the electric fi eld for small fi elds. However, since the electron is negatively charged, the net motion of the electron is opposite to the electric fi eld direction. We can then write 

$$
v _ {d n} = - \mu_ {n} \mathrm{E} \tag {5.7}
$$

where $\mu _ { n }$ is the electron mobility and is a positive quantity. Equation (5.6) may now be written as 

$$
J _ {n \mid d r f} = (- e n) \left(- \mu_ {n} \mathrm{E}\right) = e \mu_ {n} n \mathrm{E} \tag {5.8}
$$

The conventional drift current due to electrons is also in the same direction as the applied electric fi eld even though the electron movement is in the opposite direction. 

Electron and hole mobilities are functions of temperature and doping concentrations, as we will see in the next section. Table 5.1 shows some typical mobility values at $T = 3 0 0 \mathrm { K }$ for low doping concentrations. 

Since both electrons and holes contribute to the drift current, the total drift current density is the sum of the individual electron and hole drift current densities, so we may write 

$$
J _ {d r f} = e \left(\mu_ {n} n + \mu_ {p} p\right) \mathrm{E} \tag {5.9}
$$

# Solution

Since $N _ { d } > N _ { a } ,$ the semiconductor is n type and the majority carrier electron concentration, from Chapter 4 is given by 

$$
n = \frac {N _ {d} - N _ {a}}{2} + \sqrt {\left(\frac {N _ {d} - N _ {a}}{2}\right) ^ {2} + n _ {i} ^ {2}} \approx 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}
$$

The minority carrier hole concentration is 

$$
p = \frac {n _ {i} ^ {2}}{n} = \frac {(1 . 8 \times 1 0 ^ {6}) ^ {2}}{1 0 ^ {1 6}} = 3. 2 4 \times 1 0 ^ {- 4} \mathrm{cm} ^ {- 3}
$$

For this extrinsic n-type semiconductor, the drift current density is 

$$
J _ {d r f} = e \left(\mu_ {n} n + \mu_ {p} p\right) \mathrm{E} \approx e \mu_ {n} N _ {d} \mathrm{E}
$$

Then 

$$
J _ {d r f} = (1. 6 \times 1 0 ^ {- 1 9}) (8 5 0 0) (1 0 ^ {1 6}) (1 0) = 1 3 6 \mathrm{A} / \mathrm{cm} ^ {2}
$$

# ■ Comment

Signifi cant drift current densities can be obtained in a semiconductor applying relatively small electric fi elds. We may note from this example that the drift current will usually be due primarily to the majority carrier in an extrinsic semiconductor. 

# ■ EXERCISE PROBLEM

Ex 5.1 A drift current density of $J _ { d r f } = 7 5 \mathrm { A } / \mathrm { c m } ^ { 2 }$ is required in a device using p-type silicon when an electric fi eld of E - 120 V/cm is applied. Determine the required impurity doping concentration to achieve this specifi cation. Assume that electron and hole mobilities given in Table 5.1 apply. $( \phantom { } _ { \varepsilon - } \mathbf { U } \mathbf { 0 } \phantom { } _ { \varsigma _ { 1 } } 0 \mathbf { I } \times \mathbf { \hat { \nu } } \mathbf { 0 } ^ { \circ } \mathbf { - } \mathbf { \overset { . } { \ 8 } } = \mathbf { \overset { . } { \ 8 } } \mathbf { \cdot } \mathbf { \overset { . } { \mathbf { S } } } \mathbf { U } \mathbf { \overset { . } { \ V } } )$ 

# 5.1.2 Mobility Effects

In the previous section, we defi ned mobility, which relates the average drift velocity of a carrier to the electric fi eld. Electron and hole mobilities are important semiconductor parameters in the characterization of carrier drift, as seen in Equation (5.9). 

Equation (5.3) related the acceleration of a hole to a force such as an electric fi eld. We may write this equation as 

$$
F = m _ {c p} ^ {*} \frac {d v}{d t} = e \mathrm{E} \tag {5.10}
$$

where v is the velocity of the particle due to the electric fi eld and does not include the random thermal velocity. If we assume that the conductivity effective mass and electric fi eld are constants, then we may integrate Equation (5.10) and obtain 

$$
v = \frac {e \mathrm{E} t}{m _ {c p} ^ {*}} \tag {5.11}
$$

where we have assumed the initial drift velocity to be zero. 

Figure 5.1a shows a schematic model of the random thermal velocity and motion of a hole in a semiconductor with zero electric fi eld. There is a mean time between collisions which may be denoted by $\tau _ { c p } .$ If a small electric fi eld (E-fi eld) is applied as indicated in Figure 5.1b, there will be a net drift of the hole in the direction of the E-fi eld, and the net drift velocity will be a small perturbation on the random thermal velocity, so the time between collisions will not be altered appreciably. If we use the mean time between collisions $\tau _ { c p }$ in place of the time t in Equation (5.11), then the mean peak velocity just prior to a collision or scattering event is 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/2ac93888e203a5678c6b42afa81f1b3c258d8381630b7f28be3e3e6ce409d25b.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/a980bf411232ed4522a134318b153521de897ffe5e3dea1f30a4e5878c2594f6.jpg)



Figure 5.1 | Typical random behavior of a hole in a semiconductor (a) without an electric fi eld and (b) with an electric fi eld.


$$
v _ {d \mid \text { peak }} = \left(\frac {e \tau_ {c p}}{m _ {c p} ^ {*}}\right) \mathrm{E} \tag {5.12a}
$$

The average drift velocity is one half the peak value so that we can write 

$$
\langle v _ {d} \rangle = \frac {1}{2} \left(\frac {e \tau_ {c p}}{m _ {c p} ^ {*}}\right) \mathrm{E} \tag {5.12b}
$$

However, the collision process is not as simple as this model, but is statistical in nature. In a more accurate model including the effect of a statistical distribution, the factor $\frac { 1 } { 2 }$ in Equation (5.12b) does not appear. The hole mobility is then given by 

$$
\mu_ {p} = \frac {v _ {d p}}{\mathrm{E}} = \frac {e \tau_ {c p}}{m _ {c p} ^ {*}} \tag {5.13}
$$

The same analysis applies to electrons; thus, we can write the electron mobility as 

$$
\mu_ {n} = \frac {e \tau_ {c n}}{m _ {c n} ^ {*}} \tag {5.14}
$$

where $\tau _ { c n }$ is the mean time between collisions for an electron. 

There are two collision or scattering mechanisms that dominate in a semiconductor and affect the carrier mobility: phonon or lattice scattering, and ionized impurity scattering. 

The atoms in a semiconductor crystal have a certain amount of thermal energy at temperatures above absolute zero that causes the atoms to randomly vibrate about their lattice position within the crystal. The lattice vibrations cause a disruption in the perfect periodic potential function. A perfect periodic potential in a solid allows electrons to move unimpeded, or with no scattering, through the crystal. But the thermal vibrations cause a disruption of the potential function, resulting in an interaction between the electrons or holes and the vibrating lattice atoms. This lattice scattering is also referred to as phonon scattering. 

Since lattice scattering is related to the thermal motion of atoms, the rate at which the scattering occurs is a function of temperature. If we denote $\mu _ { L }$ as the mobility that would be observed if only lattice scattering existed, then the scattering theory states that to fi rst order 

$$
\mu_ {L} \propto T ^ {- 3 / 2} \tag {5.15}
$$

Mobility that is due to lattice scattering increases as the temperature decreases. Intuitively, we expect the lattice vibrations to decrease as the temperature decreases, which implies that the probability of a scattering event also decreases, thus increasing mobility. 

Figure 5.2 shows the temperature dependence of electron and hole mobilities in silicon. In lightly doped semiconductors, lattice scattering dominates and the carrier mobility decreases with temperature as we have discussed. The temperature dependence of mobility is proportional to $T ^ { - n }$ . The inserts in the fi gure show that the parameter n is not equal to $\frac { 3 } { 2 }$ as the fi rst-order scattering theory predicted. However, mobility does increase as the temperature decreases. 

The second interaction mechanism affecting carrier mobility is called ionized impurity scattering. We have seen that impurity atoms are added to the semiconductor to control or alter its characteristics. These impurities are ionized at room temperature so that a coulomb interaction exists between the electrons or holes and the ionized impurities. This coulomb interaction produces scattering or collisions and also alters the velocity characteristics of the charge carrier. If we denote $\mu _ { I }$ as the mobility that would be observed if only ionized impurity scattering existed, then to fi rst order we have 

$$
\mu_ {I} \propto \frac {T ^ {+ 3 / 2}}{N _ {I}} \tag {5.16}
$$

where $N _ { I } = N _ { d } ^ { + } + N _ { a } ^ { - }$ is the total ionized impurity concentration in the semiconductor. If temperature increases, the random thermal velocity of a carrier increases, reducing the time the carrier spends in the vicinity of the ionized impurity center. The less time spent in the vicinity of a coulomb force, the smaller the scattering effect and the larger the expected value of $\mu _ { I }$ . If the number of ionized impurity centers increases, then the probability of a carrier encountering an ionized impurity center increases, implying a smaller value of $\mu _ { I }$ . 

Figure 5.3 is a plot of electron and hole mobilities in germanium, silicon, and gallium arsenide at $T = 3 0 0 ~ \mathrm { K }$ as a function of impurity concentration. More accurately, these curves are of mobility versus ionized impurity concentration $N _ { I } .$ . As the impurity concentration increases, the number of impurity scattering centers increases, thus reducing mobility. 

If $\tau _ { L }$ is the mean time between collisions due to lattice scattering, then $d t / \tau _ { L }$ is the probability of a lattice scattering event occurring in a differential time dt. Likewise, if $\tau _ { I }$ is the mean time between collisions due to ionized impurity scattering, then $d t / \tau _ { I }$ is the probability of an ionized impurity scattering event occurring in the differential time dt. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/b9075bb20a949ab44a2c4977a40660b5fb380eb9048db8788003679a3d1ce71f.jpg)



( a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/0489440e58f303b71940ee2236db096855209a94512ed4f50d5720bdd0e8390e.jpg)



( b )



Figure 5.2 | (a) Electron and (b) hole mobilities in silicon versus temperature for various doping concentrations . Inserts show temperature dependence for “almost” intrinsic silicon.



(From Pierret [8]. )


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/0c98947fe7e35cef4690d1de0bf106634757c53235fbeafb723f163107c428ca.jpg)



Figure 5.3 | Electron and hole mobilities versus impurity concentrations for germanium, silicon, and gallium arsenide at T - 300 K.



(From Sze [14].)


If these two scattering processes are independent, then the total probability of a scattering event occurring in the differential time dt is the sum of the individual events, or 

$$
\frac {d t}{\tau} = \frac {d t}{\tau_ {I}} + \frac {d t}{\tau_ {L}} \tag {5.17}
$$

where  is the mean time between any scattering event. 

Comparing Equation (5.17) with the defi nitions of mobility given by Equation (5.13) or (5.14), we can write 

$$
\boxed {\frac {1}{\mu} = \frac {1}{\mu_ {I}} + \frac {1}{\mu_ {L}}} \tag {5.18}
$$

where $\mu _ { I }$ is the mobility due to the ionized impurity scattering process and $\mu _ { L }$ is the mobility due to the lattice scattering process. The parameter $\mu$ is the net mobility. With two or more independent scattering mechanisms, the inverse mobilities add, which means that the net mobility decreases. 

# EXAMPLE 5.2

Objective: Determine the electron mobility in silicon at various doping concentrations and various temperatures. 

Using Figure 5.2, fi nd the electron mobility in silicon for: 

(a) $T = 2 5 ^ { \circ } \mathrm { C }$ for (i) Nd - 1016 cm3 and (ii) Nd - 1017 cm3. 

(b) $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } \mathrm { f o r } ( i ) T = 0 ^ { \circ } \mathrm { C } \mathrm { a n d } ( i i ) T = 1 0 0 ^ { \circ } \mathrm { C } .$ 

# Solution:

From Figure 5.2, we fi nd the following: 

${ \mathrm { ( a ) } } T = 2 5 ^ { \circ } \mathrm { C } ; { \mathrm { ( } i \mathrm { ) } N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } \Rightarrow \mu _ { n } \cong 1 2 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } } .$ 

$$
(i i) N _ {d} = 1 0 ^ {1 7} \mathrm{cm} ^ {- 3} \Rightarrow \mu_ {n} \cong 8 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}.
$$

${ \mathrm { ( b ) } } N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } ; \left( i \right) T = 0 ^ { \circ } \mathrm { C } \Rightarrow \mu _ { n } \cong 1 4 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } .$ 

$$
(i i) T = 1 0 0 ^ {\circ} \mathrm{C} \Rightarrow \mu_ {n} \cong 7 8 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}.
$$

# ■ Comment

The results of this example show that the mobility values are strong functions of the doping concentration and temperature. These variations must be taken into account in the design of semiconductor devices. 

# ■ EXERCISE PROBLEM

Ex 5.2 Using Figure 5.2, fi nd the hole mobility in silicon for: 

(a) T - 25°C for (i) $N _ { a } = 1 0 ^ { 1 6 } \thinspace \mathrm { c m } ^ { - 3 }$ and (ii) $N _ { a } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 }$ , and 

(b) $N _ { a } = 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ for (i) T - 0°C and (ii) $T = 1 0 0 ^ { \circ } \mathrm { C } .$ 

$$
[ (s - \Lambda / 2 m c m ^ {2} / V - s), (i i) \mu_ {q} \approx 3 0 0 c m ^ {2} / V - s) ]
$$

$$
[ (\text { Ans. } (a) (i) \mu_ {p} \equiv 4 1 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}, (i i) \mu_ {p} \equiv 1 3 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s};
$$

# 5.1.3 Conductivity

The drift current density, given by Equation (5.9), may be written as 

$$
J _ {d r f} = e (\mu_ {n} n + \mu_ {p} p) \mathrm{E} = \sigma \mathrm{E} \tag {5.19}
$$

where  is the conductivity of the semiconductor material. The conductivity is given in units of $( \Omega { \mathrm { - c m } } ) ^ { - 1 }$ and is a function of the electron and hole concentrations and mobilities. We have just seen that the mobilities are functions of impurity concentrations; conductivity, then is a somewhat complicated function of impurity concentration. 

The reciprocal of conductivity is resistivity, which is denoted by $\rho$ and is given in units of ohm-cm. We can write the formula for resistivity as2 

$$
\rho = \frac {1}{\sigma} = \frac {1}{e (\mu_ {n} n + \mu_ {p} p)} \tag {5.20}
$$

Figure 5.4 is a plot of resistivity as a function of impurity concentration in silicon, germanium, gallium arsenide, and gallium phosphide at $T = 3 0 0 \mathrm { K } .$ . Obviously, the curves are not linear functions of $N _ { d }$ or $N _ { a }$ because of mobility effects. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/3e0fb58bb82b74afac135b9b25f40bd938d4544dfe7ca6395cef2cb618b32c22.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/6ea60d0298fa83367ff4475e17d6a46833ca31143d786e6644e87ced6d68839a.jpg)



Figure 5.4 | Resistivity versus impurity concentration at T - 300 K in (a) silicon and (b) germanium, gallium arsenide, and gallium phosphide.



(From Sze [14].)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/d857fa3de40abcc87e72c620ed356863d34e93c1043909e778e7932c1cbdfa52.jpg)



Figure 5.5 | Bar of semiconductor material as a resistor.


If we have a bar of semiconductor material as shown in Figure 5.5 with a voltage applied that produces a current I, then we can write 

$$
J = \frac {I}{A} \tag {5.21a}
$$

and 

$$
\mathrm{E} = \frac {V}{L} \tag {5.21b}
$$

We can now rewrite Equation (5.19) as 

$$
\frac {I}{A} = \sigma \left(\frac {V}{L}\right) \tag {5.22a}
$$

or 

$$
V = \left(\frac {L}{\sigma A}\right) I = \left(\frac {\rho L}{A}\right) I = I R \tag {5.22b}
$$

Equation (5.22b) is Ohm’s law for a semiconductor. The resistance is a function of resistivity, or conductivity, as well as the geometry of the semiconductor. 

If we consider, for example, a p-type semiconductor with an acceptor doping $N _ { a } ( N _ { d } = 0 )$ in which $N _ { a } \gg n _ { i } .$ , and if we assume that the electron and hole mobilities are of the same order of magnitude, then the conductivity becomes 

$$
\sigma = e (\mu_ {n} n + \mu_ {p} p) \approx e \mu_ {p} p \tag {5.23}
$$

If we also assume complete ionization, then Equation (5.23) becomes 

$$
\sigma \approx e \mu_ {\rho} N _ {a} \approx \frac {1}{\rho} \tag {5.24}
$$

The conductivity and resistivity of an extrinsic semiconductor are a function primarily of the majority carrier parameters. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/c35c34361c60449fdeeb61cbe11e3f0ee8498a293d96290c70483d98f32f21ee.jpg)



Figure 5.6 | Electron concentration and conductivity versus inverse temperature for silicon.



(After Sze [14].)


We may plot the carrier concentration and conductivity of a semiconductor as a function of temperature for a particular doping concentration. Figure 5.6 shows the electron concentration and conductivity of silicon as a function of inverse temperature for the case when $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . In the midtemperature range, or extrinsic range, as shown, we have complete ionization—the electron concentration remains essentially constant. However, the mobility is a function of temperature so the conductivity varies with temperature in this range. At higher temperatures, the intrinsic carrier concentration increases and begins to dominate the electron concentration as well as the conductivity. In the lower temperature range, freeze-out begins to occur; the electron concentration and conductivity decrease with decreasing temperature. 

Objective: Determine the doping concentration and majority carrier mobility given the type and conductivity of a compensated semiconductor. 

Consider compensated n-type silicon at ${ \cal T } = 3 0 0 \mathrm { ~ K } ,$ , with a conductivity of $\sigma =$ $1 6 ( \Omega { \cdot } \mathrm { c m } ) ^ { - 1 }$ and an acceptor doping concentration of $1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ . Determine the donor concentration and the electron mobility. 

# Solution

For n-type silicon at $T = 3 0 0 \mathrm { K } .$ , we can assume complete ionization; therefore the conductivity, assuming $N _ { d } - N _ { a } \gg n _ { i } ,$ is given by 

$$
\sigma \approx e \mu_ {n} n = e \mu_ {n} (N _ {d} - N _ {a})
$$

We have that 

$$
1 6 = (1. 6 \times 1 0 ^ {- 1 9}) \mu_ {n} (N _ {d} - 1 0 ^ {1 7})
$$

EXAMPLE 5.3 

Since mobility is a function of the ionized impurity concentration, we can use Figure 5.3 along with trial and error to determine $\mu _ { n }$ and $N _ { d } .$ For example, if we choose $N _ { d } = 2 \times 1 0 ^ { 1 7 } .$ , then $N _ { I } = N _ { d } ^ { + } + N _ { a } ^ { - } = 3 \times 1 0 ^ { 1 7 } \nonumber$ so that $\mu _ { n } \approx 5 1 0$ cm2/V-s which gives $\sigma = 8 . 1 6 ~ ( \Omega { \mathrm { - c m } } ) ^ { - 1 } .$ . If we choose $N _ { d } = 5 \times 1 0 ^ { 1 7 }$ , then $N _ { I } = 6 \times 1 0 ^ { 1 7 }$ so that $\mu _ { n } \approx 3 2 5$ cm2/V-s, which gives $\sigma =$ $2 0 . 8 ( \Omega \mathrm { - c m } ) ^ { - 1 }$ . The doping is bounded between these two values. Further trial and error yields 

$$
N _ {d} \approx 3. 5 \times 1 0 ^ {1 7} \mathrm{cm} ^ {- 3} \quad \text { and } \quad \mu_ {n} \approx 4 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}
$$

which gives 

$$
\sigma \approx 1 6 (\Omega - \mathrm{cm}) ^ {- 1}
$$

# ■ Comment

We can see from this example that, in a high-conductivity semiconductor material, mobility is a strong function of carrier concentration. 

# ■ EXERCISE PROBLEM

Ex 5.3 A compensated p-type silicon material at T - 300 K has impurity doping concentrations of $N _ { a } = 2 . 8 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ and $N _ { d } = 8 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Determine the (a) hole mobility, (b) conductivity, and (c) resistivity. 

$$
[ (\text { Ans. } (a) \mu_ {p} \approx 2 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}; (b) \sigma = 6. 4 (\Omega - \mathrm{cm}) ^ {- 1}, (c) p = 0. 1 5 6 (\Omega - \mathrm{cm}) ]
$$

# DESIGN EXAMPLE 5.4

Objective: Design a semiconductor resistor with a specifi ed resistance to handle a given current density. 

A silicon semiconductor at T - 300 K is initially doped with donors at a concentration of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } ,$ . Acceptors are to be added to form a compensated p-type material. The resistor is to have a resistance of 10 k
 and handle a current density of 50 A/cm2 when 5 V is applied. 

# ■ Solution

For 5 V applied to a 10-k
 resistor, the total current is 

$$
I = \frac {V}{R} = \frac {5}{1 0} = 0. 5 \mathrm{mA}
$$

If the current density is limited to 50 A/cm2, then the cross-sectional area is 

$$
A = \frac {I}{J} = \frac {0 . 5 \times 1 0 ^ {- 3}}{5 0} = 1 0 ^ {- 5} \mathrm{cm} ^ {2}
$$

If we, somewhat arbitrarily at this point, limit the electric fi eld to E - 100 V/cm, then the length of the resistor is 

$$
L = \frac {V}{\mathrm{E}} = \frac {5}{1 0 0} = 5 \times 1 0 ^ {- 2} \mathrm{cm}
$$

From Equation (5.22b), the conductivity of the semiconductor is 

$$
\sigma = \frac {L}{R A} = \frac {5 \times 1 0 ^ {- 2}}{(1 0 ^ {4}) (1 0 ^ {- 5})} = 0. 5 0 (\Omega - \mathrm{cm}) ^ {- 1}
$$

The conductivity of a compensated p-type semiconductor is 

$$
\sigma \approx e \mu_ {p} p = e \mu_ {p} (N _ {a} - N _ {d})
$$

where the mobility is a function of the total ionized impurity concentration $N _ { a } + N _ { d } .$ . 

Using trial and error, if $N _ { a } = 1 . 2 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , then $N _ { a } + N _ { d } = 1 . 7 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , and the hole mobility, from Figure 5.3, is approximately $\mu _ { p } = 4 1 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ . The conductivity is then 

$$
\sigma = e \mu_ {p} (N _ {a} - N _ {d}) = (1. 6 \times 1 0 ^ {- 1 9}) (4 1 0) (1. 2 5 \times 1 0 ^ {1 6} - 5 \times 1 0 ^ {1 5}) = 0. 4 9 2
$$

which is very close to the value we need. 

# ■ Comment

Since the mobility is related to the total ionized impurity concentration, the determination of the impurity concentration to achieve a particular conductivity is not straightforward. 

# ■ EXERCISE PROBLEM

Ex 5.4 A bar of p-type silicon, such as shown in Figure 5.5, has a cross-sectional area 

$A = 1 0 ^ { - 6 } \mathrm { c m } ^ { 2 }$ and a length $L = 1 . 2 \times 1 0 ^ { - 3 }$ cm. For an applied voltage of 5 V, a current of 2 mA is required. What is the required (a) resistance, (b) resistivity, and 

(c) impurity doping concentration? (d ) What is the resulting hole mobility? 

$$
[ \text { Ans. } (a) 2. 5 \mathrm{K} \Omega ; (b) 2. 0 8 3 (\Omega - \mathrm{cm}); (\mathrm{c}) N _ {a} \approx 7. 3 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}; (d) \mu_ {p} \approx 4 1 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s} ]
$$

For an intrinsic material, the conductivity can be written as 

$$
\sigma_ {i} = e \left(\mu_ {n} + \mu_ {p}\right) n _ {i} \tag {5.25}
$$

The concentrations of electrons and holes are equal in an intrinsic semiconductor, so the intrinsic conductivity includes both the electron and hole mobility. Since, in general, the electron and hole mobilities are not equal, the intrinsic conductivity is not the minimum value possible at a given temperature. 

# 5.1.4 Velocity Saturation

So far in our discussion of drift velocity, we have assumed that mobility is not a function of electric fi eld, meaning that the drift velocity will increase linearly with applied electric fi eld. The total velocity of a particle is the sum of the random thermal velocity and drift velocity. At $T = 3 0 0 ~ \mathrm { K }$ , the average random thermal energy is given by 

$$
\frac {1}{2} m v _ {t h} ^ {2} = \frac {3}{2} k T = \frac {3}{2} (0. 0 2 5 9) = 0. 0 3 8 8 5 \mathrm{eV} \tag {5.26}
$$

This energy translates into a mean thermal velocity of approximately $1 0 ^ { 7 }$ cm /s for an electron in silicon. If we assume an electron mobility of $\mu _ { n } = 1 3 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ in low-doped silicon, a drift velocity of $1 0 ^ { 5 }$ cm/s, or 1 percent of the thermal velocity, is achieved if the applied electric fi eld is approximately 75 V/cm. This applied electric fi eld does not appreciably alter the energy of the electron. 

Figure 5.7 is a plot of average drift velocity as a function of applied electric fi eld for electrons and holes in silicon, gallium arsenide, and germanium. At low electric fi elds, where there is a linear variation of velocity with electric fi eld, the slope of the drift velocity versus electric fi eld curve is the mobility. The behavior of the drift velocity of carriers at high electric fi elds deviates substantially from the linear relationship observed at low fi elds. The drift velocity of electrons in silicon, for example, saturates at approximately 107 cm /s at an electric fi eld of approximately 30 kV/cm. If the drift velocity of a charge carrier saturates, then the drift current density also saturates and becomes independent of the applied electric fi eld. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/aee2b18749dd80104fd8a742e998105ee7cb54b57e9a4af24d3ac92d653c04bb.jpg)



Figure 5.7 | Carrier drift velocity versus electric fi eld for high-purity silicon, germanium, and gallium arsenide. (From Sze [14].)


The experimental carrier drift velocity versus electric fi eld in silicon can be approximated for electrons by [2] 

$$
v _ {n} = \frac {v _ {s}}{\left[ 1 + \left(\frac {\mathrm{E} _ {\mathrm{on}}}{\mathrm{E}}\right) ^ {2} \right] ^ {1 / 2}} \tag {5.27a}
$$

and for holes by 

$$
v _ {p} = \frac {v _ {s}}{\left[ 1 + \left(\frac {\mathrm{E} _ {\mathrm{op}}}{\mathrm{E}}\right) \right]} \tag {5.27b}
$$

The variables are $v _ { s } = 1 0 ^ { 7 }$ cm/s at $T = 3 0 0 ~ \mathrm { K } , \mathrm { E _ { o n } = 7 ~ \times ~ 1 0 ^ { 3 } }$ V/cm, and $\mathrm { E _ { o p } = }$ $2 \times 1 0 ^ { 4 } \mathrm { V / c m }$ . 

We may note that for small electric fi elds, the drift velocities reduce to 

$$
v _ {n} \cong \left(\frac {\mathrm{E}}{\mathrm{E} _ {\mathrm{on}}}\right) \cdot v _ {s} \tag {5.28a}
$$

and 

$$
v _ {p} \cong \left(\frac {\mathrm{E}}{\mathrm{E} _ {\mathrm{op}}}\right) \cdot v _ {s} \tag {5.28b}
$$

At low electric fi elds, the drift velocities are linear functions of the electric fi eld as we have discussed. However, for large electric fi elds, the drift velocities approach the saturation value. 

The drift velocity versus electric fi eld characteristic of gallium arsenide is more complicated than for silicon or germanium. At low fi elds, the slope of the drift velocity versus E-fi eld is constant and is the low-fi eld electron mobility, which is approximately 8500 cm2/V-s for gallium arsenide. The low-fi eld electron mobility in gallium arsenide is much larger than in silicon. As the fi eld increases, the electron drift velocity in gallium arsenide reaches a peak and then decreases. A differential mobility is the slope of the $v _ { d }$ versus E curve at a particular point on the curve and the negative slope of the drift velocity versus electric fi eld represents a negative differential mobility. The negative differential mobility produces a negative differential resistance; this characteristic is used in the design of oscillators. 

The negative differential mobility can be understood by considering the $E$ versus k diagram for gallium arsenide, which is shown again in Figure 5.8. The density of states effective mass of the electron in the lower valley is $m _ { n } ^ { * } = 0 . 0 6 7 m _ { 0 } .$ . The small effective mass leads to a large mobility. As the E-fi eld increases, the energy of the electron increases and the electron can be scattered into the upper valley, where the density of states effective mass is $0 . 5 5 m _ { 0 } .$ . The larger effective mass in the upper valley yields a smaller mobility. This intervalley transfer mechanism results in a decreasing average drift velocity of electrons with electric fi eld, or the negative differential mobility characteristic. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/b25522c4a45e25b266fa27d1ac73fc1679d7c0e3c6f493aeceeca95366883c29.jpg)



Figure 5.8 | Energy-band structure for gallium arsenide showing the upper valley and lower valley in the conduction band. (From Sze [15].)


# TEST YOUR UNDERSTANDING

TYU 5.1 Consider a sample of silicon at $T = 3 0 0$ K doped at an impurity concentration of $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ . Assume electron and hole mobilities given in Table 5.1. Calculate the drift current density if the applied electric fi eld is E - 35 V/cm. ) 2  (Ans. 6.80 A/cm 

TYU 5.2 Silicon at $T = 3 0 0 \mathrm { K }$ is doped with impurity concentrations of $N _ { d } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ . (a) What are the electron and hole mobilities? (b) Determine the conductivity and resistivity of the material. 

$$
[ \text { Ans. } (a) \mu_ {n} = 1 0 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}, \mu_ {p} = 3 5 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}; (b) \sigma = 4. 8 (\Omega - \mathrm{cm}) ^ {- 1}, p = 0. 2 0 8 \Omega - \mathrm{cm} ]
$$

TYU 5.3 For a particular silicon semiconductor device at T - 300 K, the required material is n type with a resistivity of 0.10 
-cm. (a) Determine the required impurity doping concentration and (b) the resulting electron mobility. $\begin{array} { r } { \left[ \bar { \mathsf { s } } - \Lambda / \zeta \mathsf { U } \mathsf { U } \right) \bar { \mathsf { S } } 6 9 \approx \overset { u } { \eta } \bar { d } ( q ) : _ { \updownarrow - \updownarrow } \mathtt { U } \mathsf { 0 } _ { \updownarrow } 0 \mathsf { I } \times 6 \approx \overset { p } { N } \cdot \bar { \pmb { \gamma } } \cdot \mathsf { S } } \end{array}$ ) From Figure a [Ans. ( 

# 5.2 | CARRIER DIFFUSION

There is a second mechanism, in addition to drift, that can induce a current in a semiconductor. We may consider a classic physics example in which a container, as shown in Figure 5.9, is divided into two parts by a membrane. The left side contains gas molecules at a particular temperature and the right side is initially empty. The gas molecules are in continual random thermal motion so that, when the membrane is broken, the gas molecules fl ow into the right side of the container. Diffusion is the process whereby particles fl ow from a region of high concentration toward a region of low concentration. If the gas molecules were electrically charged, the net fl ow of charge would result in a diffusion current. 

# 5.2.1 Diffusion Current Density

To begin to understand the diffusion process in a semiconductor, we will consider a simplifi ed analysis. Assume that an electron concentration varies in one dimension as shown in Figure 5.10. The temperature is assumed to be uniform so that the average thermal velocity of electrons is independent of x. To calculate the current, we will determine the net fl ow of electrons per unit time per unit area crossing the plane at x - 0. If the distance l shown in Figure 5.10 is less than the mean-free path of an electron, that is, the average distance an electron travels between collisions $( l < v _ { t h } \tau _ { c n } )$ , then on the average, electrons moving to the right at $x = - l$ and electrons moving to the left at $x = + l$ will cross the $x = 0 { \mathrm { p l a n e } }$ . One half of the electrons at x - l will be traveling to the right at any instant of time and one half of the electrons at x - l will be traveling to the left at any given time. The net rate of electron fl ow, $F _ { n } ,$ in the x direction at $x = 0$ is given by 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/bc8432b2f056cda71acfb6a1ea20868175bac1425a7dbf09ec6e1ac0dfafc540.jpg)



Figure 5.9 | Container divided by a membrane with gas molecules on one side.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/f868d02d62b1973bfb7d45e7a76f7c608a755a4e1c6776a4c86b212241a613e1.jpg)



Figure 5.10 | Electron concentration versus distance.


$$
F _ {n} = \frac {1}{2} n (- l) v _ {t h} - \frac {1}{2} n (+ l) v _ {t h} = \frac {1}{2} v _ {t h} [ n (- l) - n (+ l) ] \tag {5.29}
$$

If we expand the electron concentration in a Taylor series about $x = 0$ keeping only the fi rst two terms, then we can write Equation (5.29) as 

$$
F _ {n} = \frac {1}{2} v _ {t h} \left\{\left[ n (0) - l \frac {d n}{d x} \right] - \left[ n (0) + l \frac {d n}{d x} \right] \right\} \tag {5.30}
$$

which becomes 

$$
F _ {n} = - v _ {t h} l \frac {d n}{d x} \tag {5.31}
$$

Each electron has a charge (e), so the current is 

$$
J = - e F _ {n} = + e v _ {t h} l \frac {d n}{d x} \tag {5.32}
$$

The current described by Equation (5.32) is the electron diffusion current and is proportional to the spatial derivative, or density gradient, of the electron concentration. 

The diffusion of electrons from a region of high concentration to a region of low concentration produces a fl ux of electrons fl owing in the negative x direction for this example. Since electrons have a negative charge, the conventional current direction is in the positive x direction. Figure 5.11a shows these one-dimensional fl ux and current directions. We may write the electron diffusion current density for this onedimensional case, in the form 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/d997d6d184b6b62a1643c3b7c8dabbd7d4d9300e5eaa088380eeeff92844cb51.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/7eb395ab368224d97cd304b161c2a3bcb90dbfa3332e48ce76aa7952b084f4e8.jpg)



(b)



Figure 5.11 | (a) Diffusion of electrons due to a density gradient. (b) Diffusion of holes due to a density gradient.


$$
J _ {n x \mid d i f} = e D _ {n} \frac {d n}{d x} \tag {5.33}
$$

where $D _ { n }$ is called the electron diffusion coeffi cient, has units of cm2/s, and is a positive quantity. If the electron density gradient becomes negative, the electron diffusion current density will be in the negative x direction. 

Figure 5.11b shows an example of a hole concentration as a function of distance in a semiconductor. The diffusion of holes, from a region of high concentration to a region of low concentration, produces a fl ux of holes in the negative x direction. Since holes are positively charged particles, the conventional diffusion current density is also in the negative x direction. The hole diffusion current density is proportional to the hole density gradient and to the electronic charge, so we may write 

$$
J _ {p x \mid d i f} = - e D _ {p} \frac {d p}{d x} \tag {5.34}
$$

for the one-dimensional case. The parameter $D _ { p }$ is called the hole diffusion coeffi cient, has units of cm2/s, and is a positive quantity. If the hole density gradient becomes negative, the hole diffusion current density will be in the positive x direction. 

Objective: Calculate the diffusion current density given a density gradient. 

Assume that, in an n-type gallium arsenide semiconductor at T - 300 K, the electron concentration varies linearly from $1 \times 1 0 ^ { 1 8 } \mathrm { t o } 7 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ over a distance of 0.10 cm. Calculate the diffusion current density if the electron diffusion coeffi cient is $D _ { n } = 2 2 5 \mathrm { c m } ^ { 2 } / \mathrm { s } .$ . 

EXAMPLE 5.5 

# Solution

The diffusion current density is given by 

$$
\begin{array}{l} J _ {n \mid d i f} = e D _ {n} \frac {d n}{d x} \approx e D _ {n} \frac {\Delta n}{\Delta x} \\ = (1. 6 \times 1 0 ^ {- 1 9}) (2 2 5) \left(\frac {1 \times 1 0 ^ {1 8} - 7 \times 1 0 ^ {1 7}}{0 . 1 0}\right) = 1 0 8 \mathrm{A} / \mathrm{cm} ^ {2} \\ \end{array}
$$

# ■ Comment

A signifi cant diffusion current density can be generated in a semiconductor material with only a modest density gradient. 

# ■ EXERCISE PROBLEM

Ex 5.5 The hole density in silicon is given by $p ( x ) = 1 0 ^ { 1 6 } e ^ { - ( x / L p ) } ( x \geq 0 )$ where $L _ { p } = 2 \times 1 0 ^ { - 4 } \mathrm { c m } .$ 

Assume the hole diffusion coeffi cient is $D _ { p } = 8$ cm2/s. Determine the hole diffusion current density at (a) x - 0, (b) x - 2  104 cm, and (c) $x = 1 0 ^ { - 3 } \mathrm { c m } .$ 

$$
[ \text { Ans. } (a) J _ {p} = 6 4 \text {   A / cm } ^ {2}; (b) J _ {p} = 2 3. 5 4 \text {   A / cm } ^ {2}; (c) J _ {p} = 0. 4 3 1 \text {   A / cm } ^ {2} ]
$$

# 5.2.2 Total Current Density

We now have four possible independent current mechanisms in a semiconductor. These components are electron drift and diffusion currents and hole drift and diffusion currents. The total current density is the sum of these four components, or, for the one-dimensional case, 

$$
J = e n \mu_ {n} \mathrm{E} _ {x} + e p \mu_ {p} \mathrm{E} _ {x} + e D _ {n} \frac {d n}{d x} - e D _ {p} \frac {d p}{d x} \tag {5.35}
$$

This equation may be generalized to three dimensions as 

$$
J = e n \mu_ {n} \mathrm{E} + e p \mu_ {p} \mathrm{E} + e D _ {n} \nabla n - e D _ {p} \nabla p \tag {5.36}
$$

The electron mobility gives an indication of how well an electron moves in a semiconductor as a result of the force of an electric fi eld. The electron diffusion coeffi cient gives an indication of how well an electron moves in a semiconductor as a result of a density gradient. The electron mobility and diffusion coeffi cient are not independent parameters. Similarly, the hole mobility and diffusion coeffi cient are not independent parameters. The relationship between mobility and the diffusion coeffi cient is developed in the next section. 

The expression for the total current in a semiconductor contains four terms. Fortunately in most situations, we will only need to consider one term at any one time at a particular point in a semiconductor. 

# TEST YOUR UNDERSTANDING

TYU 5.4 The electron concentration in silicon is given by $n ( x ) = 1 0 ^ { 1 5 } e ^ { - ( x / L n ) } \mathrm { c m } ^ { - 3 } \left( x \geq 0 \right)$ where $L _ { n } = 1 0 ^ { - 4 } \mathrm { c m }$ . The electron diffusion coeffi cient is $D _ { n } = 2 5 \mathrm { c m } ^ { 2 } / \mathrm { s }$ . Determine the electron diffusion current density at $( a ) x = 0 , ( b ) x = 1 0 ^ { - 4 } \mathrm { c m }$ , and (c) $x \to \infty . \ [ 0 \ ( \mathscr { o } ) \ _ { : \tau } ^ { * } \mathrm { u } \mathscr { o } / \forall \ L ^ { \cdot } \ d { \bar { \nu } } \mathrm { I } - ( q ) \ _ { : \tau } ^ { * } \mathrm { U } \mathscr { o } / \forall \ 0 \ d { \bar { \nu } } - \ ( \mathscr { o } ) \ ^ { \cdot } \mathrm { s u } \forall \} ]$ 

TYU 5.5 The hole concentration in silicon varies linearly from $x = 0 \mathrm { t o } x = 0 . 0 1$ cm. The hole diffusion coeffi cient is $D _ { p } = 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s }$ , the hole diffusion current density is $2 0 \mathrm { A } / \mathrm { c m } ^ { 2 } .$ , and the hole concentration at $x = 0 \mathrm { i s } p = 4 \times 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ . What is the value of the hole concentration at x - 0.01 cm? $( \boldsymbol { \varsigma } _ { - } \mathbf { U U } \boldsymbol { \mathsf { O } } _ { \mathsf { \tiny ~ L I } } 0 \mathsf { I } \times \mathsf { S } \boldsymbol { L } ^ { \prime } \boldsymbol { \tau } ^ { \cdot } \mathrm { s u v } )$ 

# 5.3 | GRADED IMPURITY DISTRIBUTION

In most cases so far, we have assumed that the semiconductor is uniformly doped. In many semiconductor devices, however, there may be regions that are nonuniformly doped. We will investigate how a nonuniformly doped semiconductor reaches thermal equilibrium and, from this analysis, we will derive the Einstein relation, which relates mobility and the diffusion coeffi cient. 

# 5.3.1 Induced Electric Field

Consider a semiconductor that is nonuniformly doped with donor impurity atoms. If the semiconductor is in thermal equilibrium, the Fermi energy level is constant through the crystal so the energy-band diagram may qualitatively look like that shown in Figure 5.12. The doping concentration decreases as x increases in this case. There will be a diffusion of majority carrier electrons from the region of high concentration to the region of low concentration, which is in the x direction. The fl ow of negative electrons leaves behind positively charged donor ions. The separation of positive and negative charge induces an electric fi eld that is in a direction to oppose the diffusion process. When equilibrium is reached, the mobile carrier concentration is not exactly equal to the fi xed impurity concentration and the induced electric fi eld prevents any further separation of charge. In most cases of interest, the space charge induced by this diffusion process is a small fraction of the impurity concentration, thus the mobile carrier concentration is not too different from the impurity dopant density. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/a759be2e76fb60df96e853311ce0b245636dcaee41595484dec837dd55ff9432.jpg)



Figure 5.12 | Energy-band diagram for a semiconductor in thermal equilibrium with a nonuniform donor impurity concentration.


The electric potential  is related to electron potential energy by the charge (e), so we can write 

$$
\phi = + \frac {1}{e} (E _ {F} - E _ {F i}) \tag {5.37}
$$

The electric fi eld for the one-dimensional situation is defi ned as 

$$
\mathrm{E} _ {x} = - \frac {d \phi}{d x} = \frac {1}{e} \frac {d E _ {F i}}{d x} \tag {5.38}
$$

If the intrinsic Fermi-level changes as a function of distance through a semiconductor in thermal equilibrium, an electric fi eld exists in the semiconductor. 

If we assume a quasi-neutrality condition in which the electron concentration is almost equal to the donor impurity concentration, then we can still write 

$$
n _ {0} = n _ {i} \exp \left[ \frac {E _ {F} - E _ {F i}}{k T} \right] \approx N _ {d} (x) \tag {5.39}
$$

Solving for $E _ { F } - E _ { F i } ,$ we obtain 

$$
E _ {F} - E _ {F i} = k T \ln \left(\frac {N _ {d} (x)}{n _ {i}}\right) \tag {5.40}
$$

The Fermi level is constant for thermal equilibrium so when we take the derivative with respect to x we obtain 

$$
- \frac {d E _ {F i}}{d x} = \frac {k T}{N _ {d} (x)} \frac {d N _ {d} (x)}{d x} \tag {5.41}
$$

The electric fi eld can then be written, combining Equations (5.41) and (5.38), as 

$$
\mathrm{E} _ {x} = - \left(\frac {k T}{e}\right) \frac {1}{N _ {d} (x)} \frac {d N _ {d} (x)}{d x} \tag {5.42}
$$

Since we have an electric fi eld, there will be a potential difference through the semiconductor due to the nonuniform doping. 

Objective: Determine the induced electric fi eld in a semiconductor in thermal equilibrium, given a linear variation in doping concentration. 

Assume that the donor concentration in an n-type semiconductor at T - 300 K is given by 

$$
N _ {d} (x) = 1 0 ^ {1 6} - 1 0 ^ {1 9} x \quad \left(\mathrm{cm} ^ {- 3}\right)
$$

where x is given in cm and ranges between $0 \leq x \leq 1$ m 

EXAMPLE 5.6 

# ■ Solution

Taking the derivative of the donor concentration, we have 

$$
\frac {d N _ {d} (x)}{d x} = - 1 0 ^ {1 9} \quad \left(\mathrm{cm} ^ {- 4}\right)
$$

The electric fi eld is given by Equation (5.42), so we have 

$$
\mathrm{E} _ {x} = \frac {- (0 . 0 2 5 9) (- 1 0 ^ {1 9})}{(1 0 ^ {1 6} - 1 0 ^ {1 9} x)}
$$

$\operatorname { A t } x = 0 .$ , for example, we fi nd 

$$
\mathrm{E} _ {x} = 2 5. 9 \mathrm{V/cm}
$$

# ■ Comment

We may recall from our previous discussion of drift current that fairly small electric fi elds can produce signifi cant drift current densities, so that an induced electric fi eld from nonuniform doping can signifi cantly infl uence semiconductor device characteristics. 

# ■ EXERCISE PROBLEM

Ex 5.6 Assume the donor concentration in an n-type semiconductor at T - 300 K is given by $N _ { d } \left( x \right) = 1 0 ^ { 1 6 } e ^ { - x / L }$ where $L = 2 \times 1 0 ^ { - 2 }$ cm. Determine the induced electric fi eld in the semiconductor at (a) x - 0 and (b) $x = 1 0 ^ { - 4 } \mathrm { c m }$ . 

)] b ) and ( a 1.295 V/cm for ( - [Ans. E 

# 5.3.2 The Einstein Relation

If we consider the nonuniformly doped semiconductor represented by the energyband diagram shown in Figure 5.12 and assume there are no electrical connections so that the semiconductor is in thermal equilibrium, then the individual electron and hole currents must be zero. We can write 

$$
J _ {n} = 0 = e n \mu_ {n} \mathrm{E} _ {x} + e D _ {n} \frac {d n}{d x} \tag {5.43}
$$

If we assume quasi-neutrality so that $n \approx N _ { d } ( x )$ , then we can rewrite Equation (5.43) as 

$$
J _ {n} = 0 = e \mu_ {n} N _ {d} (x) \mathrm{E} _ {x} + e D _ {n} \frac {d N _ {d} (x)}{d x} \tag {5.44}
$$

Substituting the expression for the electric fi eld from Equation (5.42) into Equation (5.44), we obtain 

$$
0 = - e \mu_ {n} N _ {d} (x) \left(\frac {k T}{e}\right) \frac {1}{N _ {d} (x)} \frac {d N _ {d} (x)}{d x} + e D _ {n} \frac {d N _ {d} (x)}{d x} \tag {5.45}
$$

Equation (5.45) is valid for the condition 

$$
\frac {D _ {n}}{\mu_ {n}} = \frac {k T}{e} \tag {5.46a}
$$

The hole current must also be zero in the semiconductor. From this condition, we can show that 

$$
\frac {D _ {p}}{\mu_ {p}} = \frac {k T}{e} \tag {5.46b}
$$

Combining Equations (5.46a) and (5.46b) gives 

$$
\boxed {\frac {D _ {n}}{\mu_ {n}} = \frac {D _ {p}}{\mu_ {p}} = \frac {k T}{e}} \tag {5.47}
$$

The diffusion coeffi cient and mobility are not independent parameters. This relation between the mobility and diffusion coeffi cient, given by Equation (5.47), is known as the Einstein relation. 

Objective: Determine the diffusion coeffi cient given the carrier mobility. 

Assume that the mobility of a particular carrier is 1000 cm2/V-s at $T = 3 0 0 \mathrm { K } .$ 

EXAMPLE 5.7 

# Solution

Using the Einstein relation, we have that 

$$
D = \left(\frac {k T}{e}\right) \mu = (0. 0 2 5 9) (1 0 0 0) = 2 5. 9 \mathrm{cm} ^ {2} / \mathrm{s}
$$

# ■ Comment

Although this example is fairly simple and straightforward, it is important to keep in mind the relative orders of magnitude of the mobility and diffusion coeffi cient. The diffusion coeffi cient is approximately 40 times smaller than the mobility at room temperature. 

# ■ EXERCISE PROBLEM

Ex 5.7 Assume the electron diffusion coeffi cient of a semiconductor at $T = 3 0 0 \mathrm { K }$ is $D _ { n } = 2 1 5 \mathrm { c m } ^ { 2 } / \mathrm { s } .$ . Determine the electron mobility. $( \mathrm { s } { - } \Lambda / \varsigma \mathrm { U U } \supset \mathrm { [ } 0 \varsigma 8 = \ l ^ { u } r / \cdot \mathrm { s u } \mathrm { v } )$ 

Table 5.2 shows the diffusion coeffi cient values at $T = 3 0 0 \mathrm { K }$ corresponding to the mobilities listed in Table 5.1 for silicon, gallium arsenide, and germanium. 

The relation between the mobility and diffusion coeffi cient given by Equation (5.47) contains temperature. It is important to keep in mind that the major temperature effects are a result of lattice scattering and ionized impurity scattering processes, as discussed in Section 5.1.2. As the mobilities are strong functions of temperature because of the scattering processes, the diffusion coeffi cients are also strong functions of temperature. The specifi c temperature dependence given in Equation (5.47) is a small fraction of the real temperature characteristic. 


Table 5.2 | Typical mobility and diffusion coeffi cient values at



$T = 3 0 0 \mathrm { K } ( \mu = \mathrm { c m ^ { 2 } / V \mathrm { - } s \ a n d \ } D = \mathrm { c m ^ { 2 } / s ) }$


<table><tr><td></td><td><eq>\mu_m</eq></td><td><eq>D_n</eq></td><td><eq>\mu_p</eq></td><td><eq>D_p</eq></td></tr><tr><td>Silicon</td><td>1350</td><td>35</td><td>480</td><td>12.4</td></tr><tr><td>Gallium arsenide</td><td>8500</td><td>220</td><td>400</td><td>10.4</td></tr><tr><td>Germanium</td><td>3900</td><td>101</td><td>1900</td><td>49.2</td></tr></table>

# *5.4 | THE HALL EFFECT

The Hall effect is a consequence of the forces that are exerted on moving charges by electric and magnetic fi elds. The Hall effect is used to distinguish whether a semiconductor is n type or p type3 and to measure the majority carrier concentration and majority carrier mobility. The Hall effect device, as discussed in this section, is used to experimentally measure semiconductor parameters. However, it is also used extensively in engineering applications as a magnetic probe and in other circuit applications. 

The force on a particle having a charge q and moving in a magnetic fi eld is given by 

$$
F = q v \times B \tag {5.48}
$$

where the cross product is taken between velocity and magnetic fi eld so that the force vector is perpendicular to both the velocity and magnetic fi eld. 

Figure 5.13 illustrates the Hall effect. A semiconductor with a current $I _ { x }$ is placed in a magnetic fi eld perpendicular to the current. In this case, the magnetic fi eld is in the z direction. Electrons and holes fl owing in the semiconductor will experience a force as indicated in the fi gure. The force on both electrons and holes is in the $( - y )$ direction. In a p-type semiconductor $( p _ { 0 } > n _ { 0 } )$ , there will be a buildup of positive charge on the $y = 0$ surface of the semiconductor and, in an n-type semiconductor $( n _ { 0 } > p _ { 0 } )$ , there will be a buildup of negative charge on the $y = 0$ surface. This net charge induces an electric fi eld in the y direction as shown in the fi gure. In steady state, the magnetic fi eld force will be exactly balanced by the induced electric fi eld force. This balance may be written as 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/f05ecbb2c589b9c4f7aa137c6c929bbea1af267eaedb145d443e84a5cee7f704.jpg)



Figure 5.13 | Geometry for measuring the Hall effect.


$$
F = q [ \mathrm{E} + v \times B ] = 0 \tag {5.49a}
$$

which becomes 

$$
q \mathrm{E} _ {\mathrm{y}} = q v _ {x} B _ {z} \tag {5.49b}
$$

The induced electric fi eld in the y direction is called the Hall fi eld. The Hall fi eld produces a voltage across the semiconductor which is called the Hall voltage. We can write 

$$
V _ {H} = + \mathrm{E} _ {H} W \tag {5.50}
$$

where $E _ { H }$ is assumed positive in the y direction and $V _ { H }$ is positive with the polarity shown. 

In a p-type semiconductor, in which holes are the majority carrier, the Hall voltage will be positive as defi ned in Figure 5.13. In an n-type semiconductor, in which electrons are the majority carrier, the Hall voltage will have the opposite polarity. The polarity of the Hall voltage is used to determine whether an extrinsic semiconductor is n type or p type. 

Substituting Equation (5.50) into Equation (5.49) gives 

$$
V _ {H} = v _ {x} W B _ {z} \tag {5.51}
$$

For a p-type semiconductor, the drift velocity of holes can be written as 

$$
v _ {d x} = \frac {J _ {x}}{e p} = \frac {I _ {x}}{(e p) (W d)} \tag {5.52}
$$

where e is the magnitude of the electronic charge. Combining Equations (5.52) and (5.50), we have 

$$
V _ {H} = \frac {I _ {x} B _ {z}}{e p d} \tag {5.53}
$$

or, solving for the hole concentration, we obtain 

$$
p = \frac {I _ {x} B _ {z}}{e d V _ {H}} \tag {5.54}
$$

The majority carrier hole concentration is determined from the current, magnetic fi eld, and Hall voltage. 

For an n-type semiconductor, the Hall voltage is given by 

$$
V _ {H} = - \frac {I _ {x} B _ {z}}{n e d} \tag {5.55}
$$

so that the electron concentration is 

$$
n = - \frac {I _ {x} B _ {z}}{e d V _ {H}} \tag {5.56}
$$

Note that the Hall voltage is negative for the n-type semiconductor; therefore, the electron concentration determined from Equation (5.56) is actually a positive quantity. 

Once the majority carrier concentration has been determined, we can calculate the low-fi eld majority carrier mobility. For a p-type semiconductor, we can write 

$$
J _ {x} = e p \mu_ {p} \mathrm{E} _ {x} \tag {5.57}
$$

The current density and electric fi eld can be converted to current and voltage so that Equation (5.57) becomes 

$$
\frac {I _ {x}}{W d} = \frac {e p \mu_ {p} V _ {x}}{L} \tag {5.58}
$$

The hole mobility is then given by 

$$
\mu_ {p} = \frac {I _ {x} L}{e p V _ {x} W d} \tag {5.59}
$$

Similarly for an n-type semiconductor, the low-fi eld electron mobility is determined from 

$$
\mu_ {n} = \frac {I _ {x} L}{e n V _ {x} W d} \tag {5.60}
$$

# EXAMPLE 5.8

Objective: Determine the majority carrier concentration and mobility, given Hall effect parameters. 

Consider the geometry shown in Figure 5.13. Let L - 101 cm, W - 102 cm, and d - 103 cm. Also assume that Ix - 1.0 mA, Vx - 12.5 V, Bz - 500 gauss - 5  102 tesla, and $V _ { H } = - 6 . 2 5 \ : \mathrm { m V } .$ . 

# ■ Solution

A negative Hall voltage for this geometry implies that we have an n-type semiconductor. Using Equation (5.56), we can calculate the electron concentration as 

$$
n = \frac {- (1 0 ^ {- 3}) (5 \times 1 0 ^ {- 2})}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {- 5}) (- 6 . 2 5 \times 1 0 ^ {- 3})} = 5 \times 1 0 ^ {2 1} \mathrm{m} ^ {- 3} = 5 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}
$$

The electron mobility is then determined from Equation (5.60) as 

$$
\mu_ {n} = \frac {(1 0 ^ {- 3}) (1 0 ^ {- 3})}{(1 . 6 \times 1 0 ^ {- 1 9}) (5 \times 1 0 ^ {2 1}) (1 2 . 5) (1 0 ^ {- 4}) (1 0 ^ {- 5})} = 0. 1 0 \mathrm{m} ^ {2} / \mathrm{V} - \mathrm{s}
$$

or 

$$
\mu_ {n} = 1 0 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}
$$

# ■ Comment

It is important to note that the MKS units must be used consistently in the Hall effect equations to yield correct results. 

# ■ EXERCISE PROBLEM

Ex 5.8 A p-type silicon sample with the geometry shown in Figure 5.13 has parameters L - 0.2 cm, W - 102 cm, and $d = 8 \times 1 0 ^ { - 4 }$ cm. The semiconductor parameters are $p = 1 0 ^ { 1 6 } \thinspace \mathrm { c m } ^ { - 3 }$ and $\mu _ { p } = 3 2 0$ cm2/V-s. For $V _ { x } = 1 0 \mathrm { V }$ and Bz - 500 gauss - $5 \times 1 0 ^ { - 2 }$ tesla, determine $I _ { x }$ and VH . 0.80 mV) - H V 0.2048 mA, - x I (Ans. 

# 5.5 | SUMMARY

The two basic transport mechanisms are drift, due to an applied electric fi eld, and diffusion, due to a density gradient. 

■ Carriers reach an average drift velocity in the presence of an applied electric fi eld, due to scattering events. Two scattering processes within a semiconductor are lattice scattering and impurity scattering. 

■ The average drift velocity is a linear function of the applied electric fi eld for small values of electric fi eld, but the drift velocity reaches a saturation limit that is on the order of 107 cm/s at high electric fi elds. 

■ Carrier mobility is the ratio of the average drift velocity and applied electric fi eld. The electron and hole mobilities are functions of temperature and of the ionized impurity concentration. 

■ The drift current density is the product of conductivity and electric fi eld (a form of Ohm’s law). Conductivity is a function of the carrier concentrations and mobilities. Resistivity is the inverse of conductivity. 

■ The diffusion current density is proportional to the carrier diffusion coeffi cient and the carrier density gradient. 

■ The diffusion coeffi cient and mobility are related through the Einstein relation. 

■ The Hall effect is a consequence of a charged carrier moving in the presence of perpendicular electric and magnetic fi elds. The charged carrier is defl ected, inducing a Hall voltage. The polarity of the Hall voltage is a function of the semiconductor conductivity type. The majority carrier concentration and mobility can be determined from the Hall voltage. 

# GLOSSARY OF IMPORTANT TERMS

conductivity A material parameter related to carrier drift; quantitatively, the ratio of drift current density to electric fi eld. 

diffusion The process whereby particles fl ow from a region of high concentration to a region of low concentration. 

diffusion coeffi cient The parameter relating particle fl ux to the particle density gradient. 

diffusion current The current that results from the diffusion of charged particles. 

drift The process whereby charged particles move while under the infl uence of an electric fi eld. 

drift current The current that results from the drift of charged particles. 

drift velocity The average velocity of charged particles in the presence of an electric fi eld. 

Einstein relation The relation between the mobility and the diffusion coeffi cient. 

Hall voltage The voltage induced across a semiconductor in a Hall effect measurement. 

ionized impurity scattering The interaction between a charged carrier and an ionized impurity center. 

lattice scattering The interaction between a charged carrier and a thermally vibrating lattice atom. 

mobility The parameter relating carrier drift velocity and electric fi eld. 

resistivity The reciprocal of conductivity; a material parameter that is a measure of the resistance to current. 

velocity saturation The saturation of carrier drift velocity with increasing electric fi eld. 

# CHECKPOINT

After studying this chapter, the reader should have the ability to: 

■ Discuss carrier drift current density. 

■ Explain why carriers reach an average drift velocity in the presence of an applied electric fi eld. 

■ Discuss the mechanisms of lattice scattering and impurity scattering. 

■ Defi ne mobility and discuss the temperature and ionized impurity concentration dependence on mobility. 

■ Defi ne conductivity and resistivity. 

■ Discuss velocity saturation. 

■ Discuss carrier diffusion current density. 

■ State the Einstein relation. 

■ Describe the Hall effect. 

# REVIEW QUESTIONS

1. Write the equation for the total drift current density. Is the linear relationship between drift current density and electric fi eld always valid? Why or why not. 

2. Defi ne electron and hole mobility. What is the unit of mobility? 

3. Explain the temperature dependence of mobility. Why is the carrier mobility a function of the ionized impurity concentrations? 

4. Defi ne conductivity. Defi ne resistivity. What are the units of conductivity and resistivity? 

5. Sketch the drift velocity of electrons in silicon versus electric fi eld. Repeat for GaAs. 

6. Write the equations for the diffusion current densities of electrons and holes. 

7. What is the Einstein relation? 

8. What is the direction of the induce electric fi eld in a semiconductor with a graded donor impurity concentration? Repeat for a graded acceptor impurity concentration. 

9. Describe the Hall effect. 

10. Explain why the polarity of the Hall voltage changes depending on the conductivity type (n type or p type) of the semiconductor. 

# PROBLEMS

(Note: Use the semiconductor parameters given in Appendix B if the parameters are not specifi cally given in a problem.) 

# Section 5. 1 Carrier Drift

5.1 The concentration of donor impurity atoms in silicon is $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Assume an electron mobility of $\mu _ { n } = 1 3 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ and a hole mobility of $\mu _ { p } = 4 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ . (a) Calculate the resistivity of the material. (b) What is the conductivity of the material? 

5.2 A p-type silicon material is to have a conductivity of $\sigma = 1 . 8 0 ( \Omega { - } \mathrm { c m } ) ^ { - 1 }$ . If the mobility values are $\mu _ { n } = 1 2 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ and $\mu _ { p } = 3 8 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { - } \mathrm { s } ,$ what must be the acceptor impurity concentration in the material? 

5.3 (a) The required conductivity of an n-type silicon sample at $T = 3 0 0 \mathrm { K }$ is to be $\sigma = 1 0 ( \Omega { \mathrm { - c m } } ) ^ { - 1 }$ . What donor impurity concentration is required? What is the electron mobility corresponding to this impurity concentration? (b) A p-type silicon material is required to have a resistivity of $\rho = 0 . 2 0 ( \Omega { \cdot } \mathrm { c m } )$ . What acceptor impurity concentration is required and what is the corresponding hole mobility? 

5.4 (a) The resistivity of a p-type GaAs material at $T = 3 0 0 \mathrm { K }$ is required to be $\rho = 0 . 3 5 ( \Omega { \cdot } \mathrm { c m } )$ . Determine the acceptor impurity concentration that is required. What is the hole mobility corresponding to this impurity concentration? (b) An n-type GaAs material is required to have a conductivity of $\sigma = 1 2 0 ( \Omega { \mathrm { - c m } } ) ^ { - 1 }$ . What donor impurity concentration is required and what is the corresponding electron mobility? 

5.5 A silicon sample is 2.5 cm long and has a cross-sectional area of 0.1 cm2. The silicon is n type with a donor impurity concentration of $N _ { d } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The resistance of the sample is measured and found to be 70 
. What is the electron mobility? 

5.6 Consider a homogeneous gallium arsenide semiconductor at $T = 3 0 0 \mathrm { K }$ with $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 0$ . (a) Calculate the thermal-equilibrium values of electron and hole concentrations. (b) For an applied E-fi eld of 10 V/cm, calculate the drift current density. (c) Repeat parts (a) and (b) if $N _ { d } = 0$ and $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . 

5.7 A silicon crystal having a cross-sectional area of 0.001 cm2 and a length of $1 0 ^ { - 3 }$ cm is connected at its ends to a 10-V battery. At $T = 3 0 0 \mathrm { K } ,$ , we want a current of 100 mA in the silicon. Calculate (a) the required resistance R, (b) the required conductivity, (c) the density of donor atoms to be added to achieve this conductivity, and (d) the concentration of acceptor atoms to be added to form a compensated p-type material with the conductivity given from part (b) if the initial concentration of donor atoms is $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } .$ . 

5.8 (a) A silicon semiconductor resistor is in the shape of a rectangular bar with a crosssectional area of $8 . 5 \times 1 0 ^ { - 4 } \mathrm { c m } ^ { 2 }$ , a length of 0.075 cm, and is doped with a concentration of $2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ boron atoms. Let $T = 3 0 0 \mathrm { K }$ . A bias of 2 volts is applied across the length of the silicon device. Calculate the current in the resistor. (b) Repeat part (a) if the length is increased by a factor of three. (c) Determine the average drift velocity of holes in parts (a) and (b). 

5.9 (a) A GaAs semiconductor resistor is doped with donor impurities at a concentration of $N _ { d } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and has a cross-sectional area of $5 \times 1 0 ^ { - 5 } \mathrm { c m } ^ { 2 }$ . A current of $I = 2 5$ mA is induced in the resistor with an applied bias of 5 V. Determine the length of the resistor. (b) Using the results of part (a), calculate the drift velocity of the electrons. (c) If the bias applied to the resistor in part (a) increases to 20 V, determine the resulting current if the electrons are traveling at their saturation velocity of $5 \times 1 0 ^ { 6 } \mathrm { c m / s }$ . 

5.10 (a) Three volts is applied across a 1-cm-long semiconductor bar. The average electron drift velocity is 104 cm/s. Find the electron mobility. (b) If the electron mobility in part (a) were $8 0 0 \mathrm { c m } ^ { 2 } N \mathrm { - s }$ , what is the average electron drift velocity? 

5.11 Use the velocity–fi eld relations for silicon and gallium arsenide shown in Figure 5.7 to determine the transit time of electrons through a 1-m distance in these materials for an electric fi eld of (a) 1 kV/cm and (b) 50 kV/cm. 

5.12 A perfectly compensated semiconductor is one in which the donor and acceptor impurity concentrations are exactly equal. Assuming complete ionization, determine the resistivity of silicon at T - 300 K in which the impurity concentrations are (a) $N _ { a } = N _ { d } = 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ , (b) $N _ { a } = N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , and (c) $N _ { a } = N _ { d } = 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 } .$ . 

5.13 (a) In a p-type gallium arsenide semiconductor, the conductivity is $\sigma = 5 ( \Omega \mathrm { - c m } ) ^ { - 1 }$ at $T = 3 0 0 \mathrm { K }$ . Calculate the thermal-equilibrium values of the electron and hole concentrations. (b) Repeat part (a) for n-type silicon if the resistivity is $\rho = 8 \Omega \mathrm { - c m } .$ 

5.14 In a particular semiconductor material, $\mu _ { n } = 1 0 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } , \mu _ { p } = 6 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } ,$ , and $N _ { C } = N _ { V } = 1 0 ^ { 1 9 } \mathrm { c m } ^ { - 3 }$ . These parameters are independent of temperature. The measured conductivity of the intrinsic material is $\sigma = 1 0 ^ { - 6 } ( \Omega { - } \mathrm { c m } ) ^ { - 1 } \mathrm { a t } T = 3 0 0 \mathrm { K }$ . Find the conductivity at $T = 5 0 0 \mathrm { K }$ . 

5.15 (a) Calculate the resistivity at $T = 3 0 0$ K of intrinsic (i) silicon, (ii) germanium, and (iii) gallium arsenide. (b) If rectangular semiconductor bars are fabricated using the materials in part (a), determine the resistance of each bar if its cross-sectional area is $8 5 \mu \mathrm { m } ^ { 2 }$ and length is 200 m. 

5.16 An n-type silicon material at $T = 3 0 0 \mathrm { K }$ has a conductivity of $0 . 2 5 ( \Omega { \cdot } \mathrm { c m } ) ^ { - 1 } .$ . (a) What is the donor impurity concentration and the corresponding electron mobility? (b) Determine the expected conductivity of the material at $( i ) \ : T = 2 5 0 \ : \mathrm { K }$ and $( i i ) T = 4 0 0 { \mathrm { K } }$ . 

5.17 The conductivity of a semiconductor layer varies with depth as $\sigma ( x ) = \sigma _ { o } \exp ( - x / d )$ where $\sigma _ { o } = 2 0 ( \Omega \mathrm { - c m } ) ^ { - 1 }$ and $d = 0 . 3 \ \mu \mathrm { m }$ . If the thickness of the semiconductor layer is t - 1.5 m, determine the average conductivity of this layer. 

5.18 An n-type silicon resistor has a length $L = 1 5 0 \mu \mathrm { m }$ , width $W = 7 . 5 \ \mu \mathrm { m }$ , and thickness $T = 1 \ \mu \mathrm { m }$ . A voltage of 2 V is applied across the length of the resistor. The donor impurity concentration varies linearly through the thickness of the resistor with $N _ { d } =$ $2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ at the top surface and $N _ { d } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ at the bottom surface. Assume an average carrier mobility of $\mu _ { n } = 7 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - } \mathrm { s } . ( a )$ What is the electric fi eld in the resistor? (b) Determine the average conductivity of the silicon. (c) Calculate the current in the resistor. (d) Determine the current density near the top surface and the current density near the bottom surface. 

5.19 Consider silicon doped at impurity concentrations of $N _ { d } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 0$ . An empirical expression relating electron drift velocity to electric fi eld is given by 

$$
v _ {d} = \frac {\mu_ {n 0} \mathrm{E}}{\sqrt {1 + \left(\frac {\mu_ {n 0} \mathrm{E}}{v _ {s a t}}\right) ^ {2}}}
$$

where $\mu _ { n 0 } = 1 3 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } , v _ { s a t } = 1 . 8 \times 1 0 ^ { 7 }$ cm /s, and E is given in V/cm. Plot electron drift current density (magnitude) versus electric fi eld (log–log scale) over the range $0 \leq \mathrm { E } \leq 1 0 ^ { 6 } \mathrm { V / c m }$ . 

5.20 Consider silicon at $T = 3 0 0 \mathrm { K } .$ . Assume the electron mobility is $\mu _ { n } = 1 3 5 0 \mathrm { c m ^ { 2 } / V { - s } }$ . The kinetic energy of an electron in the conduction band is $( 1 / 2 ) m _ { n } ^ { * } v _ { d } ^ { 2 } ,$ where $m _ { n } ^ { * }$ is the effective mass and $v _ { d }$ is the drift velocity. Determine the kinetic energy of an electron in the conduction band if the applied electric fi eld is (a) 10 V/cm and (b) 1 kV/cm. 

5.21 Consider a semiconductor that is uniformly doped with $N _ { d } = 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 0$ , with an applied electric fi eld of $\mathrm { E } = 1 0 0 \mathrm { V } / \mathrm { c m } .$ Assume that $\mu _ { n } = 1 0 0 0 \mathrm { c m ^ { 2 } / V \mathrm { - s } }$ and $\mu _ { p } = 0$ . Also assume the following parameters: 

$$
N _ {c} = 2 \times 1 0 ^ {1 9} (T / 3 0 0) ^ {3 / 2} \mathrm{cm} ^ {- 3}
$$

$$
N _ {v} = 1 \times 1 0 ^ {1 9} (T / 3 0 0) ^ {3 / 2} \mathrm{cm} ^ {- 3}
$$

$$
E _ {g} = 1. 1 0 \mathrm{eV}
$$

(a) Calculate the electric-current density at $T = 3 0 0 \mathrm { K } . ( b )$ At what temperature will this current increase by 5 percent? (Assume the mobilities are independent of temperature.) 

5.22 A semiconductor material has electron and hole mobilities $\mu _ { n }$ and $\mu _ { p } ,$ respectively. When the conductivity is considered as a function of the hole concentration $p _ { 0 } ,$ (a) show that the minimum value of conductivity, $\sigma _ { \mathrm { { m i n } } } ,$ can be written as 

$$
\sigma_ {\min} = \frac {2 \sigma_ {i} (\mu_ {n} \mu_ {p}) ^ {1 / 2}}{(\mu_ {n} + \mu_ {p})}
$$

where $\sigma _ { i }$ is the intrinsic conductivity, and (b) show that the corresponding hole concen tration is $p _ { 0 } = n _ { i } ( \mu _ { n } / \mu _ { p } ) ^ { 1 / 2 }$ . 

5.23 Consider three samples of silicon at $T = 3 0 0 \mathrm { K }$ . The n-type sample is doped with arsenic atoms to a concentration of $N _ { d } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The p-type sample is doped with boron atoms to a concentration of $N _ { a } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The compensated sample is doped with both the donors and acceptors described in the n-type and p-type samples. (a) Find the equilibrium electron and hole concentrations in each sample, (b) determine the majority carrier mobility in each sample, (c) calculate the conductivity of each sample, (d) and determine the electric fi eld required in each sample to induce a drift current density of $J = 1 2 0 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . 

5.24 Three scattering mechanisms are present in a particular semiconductor material. If only the fi rst scattering mechanism were present, the mobility would be $\mu _ { 1 } = 2 0 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ , if only the second mechanism were present, the mobility would be $\mu _ { 2 } = 1 5 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ , and if only the third mechanism were present, the mobility would be $\mu _ { 3 } = 5 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ . What is the net mobility? 

5.25 Assume that the mobility of electrons in silicon at $T = 3 0 0 \mathrm { K }$ is $\mu _ { n } = 1 3 0 0 \mathrm { c m ^ { 2 } / V \mathrm { - s } }$ . Also assume that the mobility is limited by lattice scattering and varies as $T ^ { - 3 / 2 }$ . Determine the electron mobility at (a) T - 200 K and (b) $T = 4 0 0 \mathrm { K }$ . 

5.26 Two scattering mechanisms exist in a semiconductor. If only the fi rst mechanism were present, the mobility would be 250 cm2/V-s. If only the second mechanism were present, the mobility would be 500 cm2/V-s. Determine the mobility when both scattering mechanisms exist at the same time. 

5.27 The effective density of states functions in silicon can be written in the form 

$$
N _ {c} = 2. 8 \times 1 0 ^ {1 9} \left(\frac {T}{3 0 0}\right) ^ {3 / 2} \quad N _ {v} = 1. 0 4 \times 1 0 ^ {1 9} \left(\frac {T}{3 0 0}\right) ^ {3 / 2}
$$

Assume the mobilities are given by 

$$
\mu_ {n} = 1 3 5 0 \left(\frac {T}{3 0 0}\right) ^ {- 3 / 2} \quad \mu_ {p} = 4 8 0 \left(\frac {T}{3 0 0}\right) ^ {- 3 / 2}
$$

Assume the bandgap energy is $E _ { g } = 1 . 1 2 \mathrm { e V }$ and independent of temperature. Plot the intrinsic conductivity as a function of T over the range $2 0 0 \leq T \leq 6 0 0 \mathrm { \ K }$ . 

5.28 (a) Assume that the electron mobility in an n-type semiconductor is given by 

$$
\mu_ {n} = \frac {1 3 5 0}{\left(1 + \frac {N _ {d}}{5 \times 1 0 ^ {1 6}}\right) ^ {1 / 2}} \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}
$$

where $N _ { d }$ is the donor concentration in $\mathrm { c m } ^ { - 3 }$ . Assuming complete ionization, plot the conductivity as a function of $N _ { d }$ over the range $1 0 ^ { 1 5 } \leq N _ { d } \leq 1 0 ^ { 1 8 } \mathrm { c m } ^ { - 3 } .$ (b) Compare the results of part (a) to that if the mobility were assumed to be a constant equal to $1 3 5 0 \mathrm { c m } ^ { 2 } N \mathrm { - s . } ( c )$ If an electric fi eld of $E = 1 0$ V/cm is applied to the semiconductor, plot the electron drift current density of parts (a) and (b). 

# Section 5.2 Carrier Diffusion

5.29 Consider a sample of silicon at $T = 3 0 0 \mathrm { K }$ . Assume that the electron concentration varies linearly with distance, as shown in Figure P5.29. The diffusion current density is found to be $J _ { n } = 0 . 1 9 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . If the electron diffusion coeffi cient is $D _ { n } = 2 5 \mathrm { c m } ^ { 2 } / \mathrm { s } .$ , determine the electron concentration at $x = 0 .$ . 

5.30 The steady-state electron distribution in silicon can be approximated by a linear function of x. The maximum electron concentration occurs at $x = 0$ and is $n ( 0 ) = 2 \times$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } . \mathrm { A t } x = 0 . 0 1 2$ cm, the electron concentration is $5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . If the electron diffusion coeffi cient is $D _ { n } = 2 7$ cm2/s, determine the electron diffusion current density. 

5.31 The electron diffusion current density in a semiconductor is a constant and is given by $J _ { n } = - 2 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . The electron concentration at $x = 0$ is $n ( 0 ) = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } ,$ . (a) Calculate the electron concentration at $x = 2 0$ m if the material is silicon with $D _ { n } = 3 0 \mathrm { c m } ^ { 2 } / \mathrm { s }$ . (b) Repeat part (a) if the material is GaAs with $D _ { n } = 2 3 0$ cm2/s. 

5.32 The hole concentration in p-type GaAs is given by $p ( x ) = 1 0 ^ { 1 6 } ( 1 + x / L ) ^ { 2 } \mathrm { c m } ^ { - 3 }$ for $- L \leq x \leq 0$ where $L = 1 2 \mu \mathrm { m }$ . The hole diffusion coeffi cient is $D _ { p } = 1 0$ cm2/s. Calculate the hole diffusion current density at $( a ) x = 0 , ( b ) x = - 6 \mu \mathrm { m }$ , and $( c ) x = - 1 2 \mu \mathrm { m }$ . 

5.33 In silicon, the electron concentration is given by $n ( x ) = 1 0 ^ { 1 5 } e ^ { - x / L _ { n } } \mathrm { c m } ^ { - 3 }$ for $x \geq 0$ and the hole concentration is given by $p ( x ) = 5 \times 1 0 ^ { 1 5 } e ^ { + x / L _ { p } } \mathrm { c m } ^ { - 3 }$ for $x \le 0$ . The parameter values are $L _ { n } = 2 \times 1 0 ^ { - 3 }$ cm and $L _ { P } = 5 \times 1 0 ^ { - 4 } \mathrm { c m }$ . The electron and hole diffusion coeffi cients are $D _ { n } = 2 5$ cm2/s and $D _ { P } = 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s } .$ , respectively. The total current density is defi ned as the sum of the electron and hole diffusion current densities at $x = 0 .$ . Calculate the total current density. 

5.34 The concentration of holes in a semiconductor is given by $p ( x ) = 5 \times 1 0 ^ { 1 5 } e ^ { - x / L _ { p } } \mathrm { c m } ^ { - 3 }$ for $x \geq 0$ . Determine the hole diffusion current density at $( a ) x = 0$ and $( b ) x = L _ { p }$ if the material is (i) silicon with $D _ { p } = 1 0$ cm2/s and $L _ { p } = 5 0 \mu \mathrm { m }$ , and (ii) germanium with $D _ { p } = 4 8 \mathrm { c m } ^ { 2 } / \mathrm { s }$ and $L _ { p } = 2 2 . 5 \mu \mathrm { m }$ . 

5.35 The electron concentration in silicon at $T = 3 0 0 \mathrm { K }$ is given by 

$$
n (x) = 1 0 ^ {1 6} \exp \left(\frac {- x}{1 8}\right) \mathrm{cm} ^ {- 3}
$$

where x is measured in m and is limited to $0 \leq x \leq 2 5 \mu \mathrm { m }$ . The electron diffusion coeffi cient is $D _ { n } = 2 5$ cm2/s and the electron mobility is $\mu _ { n } = 9 6 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - } \mathrm { s } .$ . The total electron current density through the semiconductor is constant and equal to 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-19/bde4e35a-310d-424f-8322-52a0ba74d9c0/75868b8628305b7d61c488f082d7bc323c27890a7c2d578c68ab44cc6fd9c1b3.jpg)



Figure P5.29 | Figure for Problem 5.29.


$J _ { n } = - 4 0 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . The electron current has both diffusion and drift current components. Determine the electric fi eld as a function of x which must exist in the semiconductor. 

5.36 The total current in a semiconductor is constant and equal to $J = - 1 0 \mathrm { A } / \mathrm { c m } ^ { 2 } .$ . The total current is composed of a hole drift current and electron diffusion current. Assume that the hole concentration is a constant and equal to $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and assume that the electron concentration is given by $n ( x ) = 2 \times 1 0 ^ { 1 5 } e ^ { - x / L } \mathrm { c m } ^ { - 3 }$ where $L = 1 5 \mu \mathrm { m }$ . The electron diffusion coeffi cient is $D _ { n } = 2 7$ cm2/s and the hole mobility is $\mu _ { p } = 4 2 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { - \mathrm { s } }$ . Calculate (a) the electron diffusion current density for $x > 0 , ( b )$ the hole drift current density for $x > 0 ,$ and (c) the required electric fi eld for $x > 0$ . 

*5.37 A constant electric fi eld, $\mathrm { E } = 1 2 \mathrm { V } / \mathrm { c m } .$ exists in the x direction of an n-type gallium arsenide semiconductor for $0 \leq x \leq 5 0 \mu \mathrm { m }$ . The total current density is a constant and is $J = 1 0 0 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . $\mathbf { A } \mathbf { t } x = 0$ , the drift and diffusion currents are equal. Let $T = 3 0 0 \mathrm { K }$ and $\mu _ { n } = 8 0 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } .$ (a) Determine the expression for the electron concentration n(x). (b) Calculate the electron concentration at x - 0 and at $x = 5 0 \mu \mathrm { m } .$ . (c) Calculate the drift and diffusion current densities at $x = 5 0 \mu \mathrm { m }$ . 

*5.38 In n-type silicon, the Fermi energy level varies linearly with distance over a short range. $\mathrm { A t } x = 0 , E _ { F } - E _ { F i } = 0 . 4 \ : \mathrm { e V }$ and, at $x = 1 0 ^ { - 3 } \mathrm { c m } , E _ { F } - E _ { F i } = 0 . 1 5 \mathrm { e V . } ( a )$ Write the expression for the electron concentration over the distance. (b) If the electron diffusion coeffi cient is $D _ { n } = 2 5$ cm2/s, calculate the electron diffusion current density at (i) x - 0 and $( i i ) x = 5 \times 1 0 ^ { - 4 } \mathrm { c m }$ . 

*5.39 (a) The electron concentration in a semiconductor is given by $n = 1 0 ^ { 1 6 } ( 1 - x / L ) \mathrm { c m } ^ { - 3 }$ for $0 \le x \le L$ , where $L = 1 0 \mu \mathrm { m }$ . The electron mobility and diffusion coeffi cient are $\mu _ { n } =$ 1000 cm2/V-s and $D _ { n } = 2 5 . 9$ cm2/s. An electric fi eld is applied such that the total electron current density is a constant over the given range of x and is $J _ { n } = - 8 0 \mathrm { A } / \mathrm { c m } ^ { 2 } $ . Determine the required electric fi eld versus distance function. (b) Repeat part (a) if $J _ { n } = - 2 0 \mathrm { A } / \mathrm { c m } ^ { 2 }$ . 

# Section 5.3 Graded Impurity Distribution

5.40 Consider an n-type semiconductor at $T = 3 0 0 \mathrm { K }$ in thermal equilibrium (no current). Assume that the donor concentration varies as $N _ { d } ( x ) = N _ { d 0 } e ^ { - x / L }$ over the range $0 \le x \le L$ where $N _ { d 0 } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $L = 1 0 \mu \mathrm { m . } \left( a \right)$ Determine the electric fi eld as a function of x for $0 \leq x \leq L . \left( b \right)$ Calculate the potential difference between $x = 0$ and $x = L$ (with the potential at $x = 0$ being positive with respect to that at $x = L )$ . 

5.41 Using the data in Example 5.6, calculate the potential difference between $x = 0$ and $x = 1 \ \mu \mathrm { m }$ . 

5.42 Determine the doping profi le in a semiconductor at T - 300 K that will induce a constant electric fi eld of 500 V/cm over a length of 0.1 cm. 

*5.43 In GaAs, the donor impurity concentration varies as $N _ { d 0 }$ exp $( - x / L )$ for $0 \leq x \leq L$ , where $L = 0 .$ 1 m and $N _ { d 0 } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Assume $\mu _ { n } = 6 0 0 0 \mathrm { c m ^ { 2 } / V \mathrm { - s } }$ and T - 300 K. (a) Derive the expression for the electron diffusion current density versus distance over the given range of x. (b) Determine the induced electric fi eld that generates a drift current density that compensates the diffusion current density. 

5.44 (a) Consider the electron mobility in silicon for $N _ { d } = 1 0 ^ { 1 7 } \mathrm { c m } ^ { - 3 }$ from Figure 5.2a. Calculate and plot the electron diffusion coeffi cient versus temperature over the range $- 5 0 \leq T \leq 2 0 0 ^ { \circ } \mathrm { C } .$ . (b) Repeat part (a) if the electron diffusion coeffi cient is given by $D _ { n } = ( 0 . 0 2 5 9 ) \mu _ { n }$ for all temperatures. What conclusion can be made about the temperature dependence of the diffusion coeffi cient? 

5.45 Consider a semiconductor at $T = 3 0 0 \mathrm { K } .$ . (a) (i) Determine the electron diffusion coeffi cient if the electron mobility is $\mu _ { n } = 1 1 5 0$ cm2/V-s. (ii) Repeat (i) of part (a) if the electron mobility is $\mu _ { n } = 6 2 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } . \left( b \right) ( i )$ Determine the hole mobility if the hole diffusion coeffi cient is $D _ { p } = 8 \mathrm { c m } ^ { 2 } / \mathrm { s } .$ (ii) Repeat (i) of part (b) if the hole diffusion coeffi cient is $D _ { p } = 3 5 \mathrm { c m } ^ { 2 } / \mathrm { s }$ . 

# Section 5.4 The Hall Effect

(Note: Refer to Figure 5.13 for the geometry of the Hall effect.) 

5.46 Silicon, at $T = 3 0 0 \mathrm { K }$ , is uniformly doped with phosphorus atoms at a concentration of $2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . A Hall device has the same geometrical dimensions as given in Example 5.8. The current is $I _ { x } = 1 . 2$ mA and the magnetic fi eld is $B _ { Z } = 5 0 0 \mathrm { g a u s s } =$ $5 \times 1 0 ^ { - 2 }$ tesla. Determine (a) the Hall voltage and (b) the Hall fi eld. 

5.47 Germanium is doped with $5 \times 1 0 ^ { 1 5 }$ donor atoms per cm3 at $T = 3 0 0 \mathrm { K }$ . The dimensions of the Hall device are $d = 5 \times 1 0 ^ { - 3 }$ cm, $W = 2 \times 1 0 ^ { - 2 }$ cm, and $L = 1 0 ^ { - 1 } \mathrm { c m }$ . The current is $I _ { x } = 2 5 0 \mu A$ , the applied voltage is $V _ { x } = 1 0 0 \mathrm { m V } ,$ and the magnetic fl ux density is $B _ { z } = 5 0 0 \mathrm { g a u s s } = 5 \times 1 0 ^ { - 2 }$ tesla. Calculate: (a) the Hall voltage, (b) the Hall fi eld, and (c) the carrier mobility. 

5.48 A semiconductor Hall device at T - 300 K has the following geometry: $d = 1 0 ^ { - 3 } \mathrm { c m }$ , $W = 1 0 ^ { - 2 } \mathrm { c m }$ , and $L = 1 0 ^ { - 1 } \mathrm { c m }$ . The following parameters are measured: $I _ { X } = 0 . 5 0 \mathrm { m A }$ $V _ { X } = 1 5 \mathrm { { V } } , V _ { H } = - 5 . 2 \mathrm { { m V } } ,$ and $B z = 0 . 1 0$ tesla. Determine the (a) conductivity type, (b) majority carrier concentration, and (c) majority carrier mobility. 

5.49 Consider silicon at T - 300 K. A Hall effect device is fabricated with the following geometry: $d = 5 \times 1 0 ^ { - 3 }$ cm, $W = 5 \times 1 0 ^ { - 2 }$ cm, and L - 0.50 cm. The electrical parameters measured are: $I _ { x } = 0 . 5 0 \mathrm { m A }$ , $V _ { x } = 1 . 2 5 \ : \mathrm { V } ,$ and $B _ { z } = 6 5 0 \mathrm { g a u s s } =$ $6 . 5 \times 1 0 ^ { - 2 }$ tesla. The Hall fi eld is ${ \cal E } _ { H } = - 1 6 . 5$ mV/cm. Determine (a) the Hall voltage, (b) the conductivity type, (c) the majority carrier concentration, and (d) the majority carrier mobility. 

5.50 Consider a gallium arsenide sample at T - 300 K. A Hall effect device has been fabricated with the following geometry: d - 0.0 1 cm, $W = 0 . 0 5$ cm, and $L = 0 . 5 \mathrm { c m }$ . The electrical parameters are: Ix - 2.5 mA, $V _ { x } = 2 . 2 \ V ,$ and $B _ { z } = 2 . 5 \times 1 0 ^ { - 2 }$ tesla. The Hall voltage is $V _ { H } = - 4 . 5 \mathrm { m V }$ Find: (a) the conductivity type, (b) the majority carrier concentration, (c) the mobility, and (d) the resistivity. 

# Summary and Review

5.51 An n-type silicon semiconductor resistor is to be designed so that it carries a current of 5 mA with an applied voltage of 5 V. (a) If $N _ { d } = 3 \times 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 0 .$ , design a resistor to meet the required specifi cations. (b) If $N _ { d } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 2 . 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , redesign the resistor. (c) Discuss the relative lengths of the two designs compared to the doping concentration. Is there a linear relationship? 

5.52 In fabricating a Hall effect device, the two points at which the Hall voltage is measured may not be lined up exactly perpendicular to the current $I _ { x }$ (see Figure 5.13). Discuss the effect this misalignment will have on the Hall voltage. Show that a valid Hall voltage can be obtained from two measurements: fi rst with the magnetic fi eld in the z direction, and then in the z direction. 

5.53 Another technique for determining the conductivity type of a semiconductor is called the hot probe method. It consists of two probes and an ammeter that indicates the 

direction of current. One probe is heated and the other is at room temperature. No voltage is applied, but a current will exist when the probes touch the semiconductor. Explain the operation of this hot probe technique and sketch a diagram indicating the direction of current for p- and n-type semiconductor samples. 

# READING LIST



*1. Bube, R. H. Electrons in Solids: An Introductory Survey, 3rd ed. San Diego, CA: Academic Press, 1992. 





2. Caughey, D. M., and R. E. Thomas. “Carrier Mobilities in Silicon Empirically, Related to Doping and Field.” Proc. IEEE 55 (1967), p. 2192. 





3. Dimitrijev, S. Principles of Semiconductor Devices. New York: Oxford University, 2006. 





4. Kano, K. Semiconductor Devices. Upper Saddle River, NJ: Prentice Hall, 1998. 





*5. Lundstrom, M. Fundamentals of Carrier Transport. Vol. X of Modular Series on Solid State Devices. Reading, MA: Addison-Wesley, 1990. 





6. Muller, R. S., and T. I. Kamins. Device Electronics for Integrated Circuits, 2nd ed. New York: Wiley, 1986. 





7. Navon, D. H. Semiconductor Microdevices and Materials. New York: Holt, Rinehart & Winston, 1986. 





8. Pierret, R. F. Semiconductor Device Fundamentals. Reading, MA: Addison-Wesley, 1996. 





9. Shur, M. Introduction to Electronic Devices. New York: John Wiley and Sons, 1996. 





*10. Shur, M. Physics of Semiconductor Devices. Englewood Cliffs, NJ: Prentice Hall, 1990. 





11. Singh, J. Semiconductor Devices: An Introduction. New York: McGraw-Hill, 1994. 





12. Singh, J. Semiconductor Devices: Basic Principles. New York: John Wiley and Sons, 2001. 





13. Streetman, B. G., and S. K. Banerjee. Solid State Electronic Devices, 6th ed. Upper Saddle River, NJ: Pearson Prentice Hall, 2006. 





14. Sze, S. M. and K. K. Ng. Physics of Semiconductor Devices, 3rd ed. Hoboken, NJ: John Wiley and Sons, 2007. 





15. Sze, S. M. Semiconductor Devices: Physics and Technology, 2nd ed. New York: John Wiley and Sons, 2001. 





*16. van der Ziel, A. Solid State Physical Electronics, 2nd ed. Englewood Cliffs, NJ: Prentice Hall, 1968. 





17. Wang, S. Fundamentals of Semiconductor Theory and Device Physics. Englewood Cliffs, NJ: Prentice Hall, 1989. 





18. Yang, E. S. Microelectronic Devices. New York: McGraw-Hill, 1988. 

