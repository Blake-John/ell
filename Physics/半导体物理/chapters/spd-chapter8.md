# The pn Junction Diode

n the last chapter, we discussed the electrostatics of the pn junction in thermal equilibrium and under reverse bias. We determined the built-in potential barrier at thermal equilibrium and calculated the electric fi eld in the space charge region. We also considered the junction capacitance. 

In this chapter, we consider the pn junction with a forward-bias voltage applied and determine the current–voltage characteristics. The potential barrier of the pn junction is lowered when a forward-bias voltage is applied, allowing electrons and holes to fl ow across the space charge region. When holes fl ow from the p region across the space charge region into the n region, they become excess minority carrier holes and are subject to the excess minority carrier diffusion, drift, and recombination processes discussed in Chapter 6. Likewise, when electrons from the n region fl ow across the space charge region into the p region, they become excess minority carrier electrons and are subject to these same processes. ■ 

# 8.0 | PREVIEW

In this chapter, we will: 

■ Consider the process by which the potential barrier of a pn junction is lowered when a forward-bias voltage is applied, so holes and electrons can fl ow across the junction generating a diode current. 

■ Derive the boundary conditions for excess holes in the n region and excesselectrons in the p region, and analyze the behavior of these excess carriers under a forward bias. 

Derive the ideal current–voltage relation of the forward-biased pn junction diode. 

■ Describe and analyze nonideal effects in the pn junction diode such as highlevel injection, and generation and recombination currents. 

■ Develop a small-signal equivalent circuit of the pn junction diode. This equivalent circuit is used to relate small time-varying currents and voltages in the pn junction. 

■ Discuss large signal diode switching characteristics. 

■ Describe a specialized pn junction called a tunnel diode. 

# 8.1 | pn JUNCTION CURRENT

When a forward-bias voltage is applied to a pn junction, a current will be induced in the device. We initially consider a qualitative discussion of how charges fl ow in the pn junction and then consider the mathematical derivation of the current–voltage relationship. 

## 8.1.1 Qualitative Description of Charge Flow in a pn Junction

We can qualitatively understand the mechanism of the current in a pn junction by again considering the energy-band diagrams. Figure 8.1a shows the energy-band diagram of a pn junction in thermal equilibrium that was developed in the last chapter. We argued that the potential barrier seen by the electrons, for example, holds back the large concentration of electrons in the n region and keeps them from fl owing into the p region. Similarly, the potential barrier seen by the holes holds back the large concentration of holes in the p region and keeps them from fl owing into the n region. The potential barrier, then, maintains thermal equilibrium. 

Figure 8.1b shows the energy-band diagram of a reverse-biased pn junction. The potential of the n region is positive with respect to the p region so the Fermi energy in the n region is lower than that in the p region. The total potential barrier is now larger than that for the zero-bias case. We argued in the last chapter that the increased potential barrier continues to hold back the electrons and holes so that there is still essentially no charge fl ow and hence essentially no current. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/325ab6465cb314493b30640fa1afa03718e05ac023cff9743a14824f7eedb363.jpg)



Figure 8.1 - A pn junction and its associated energy-band diagram for (a) zero bias, (b) reverse bias, and (c) forward bias.


Figure 8.1c shows the energy-band diagram for the case when a positive voltage is applied to the p region with respect to the n region. The Fermi level in the p region is now lower than that in the n region. The total potential barrier is now reduced. The smaller potential barrier means that the electric fi eld in the depletion region is also reduced. The smaller electric fi eld means that the electrons and holes are no longer held back in the n and p regions, respectively. There will be a diffusion of holes from the p region across the space charge region where they will fl ow into the n region. Similarly, there will be a diffusion of electrons from the n region across the space charge region where they will fl ow into the p region. The fl ow of charge generates a current through the pn junction. 

The injection of holes into the n region means that these holes are minority carriers. Likewise, the injection of electrons into the p region means that these electrons are minority carriers. The behavior of these minority carriers is described by the ambipolar transport equations that were discussed in Chapter 6. There will be diffusion as well as recombination of excess carriers in these regions. The diffusion of carriers implies that there will be diffusion currents. The mathematical derivation of the pn junction current–voltage relationship is considered in the next section. 

## 8.1.2 Ideal Current–Voltage Relationship

The ideal current–voltage relationship of a pn junction is derived on the basis of four assumptions. (The last assumption has three parts, but each part deals with current.) They are: 

1. The abrupt depletion layer approximation applies. The space charge regions have abrupt boundaries, and the semiconductor is neutral outside of the depletion region. 

2. The Maxwell–Boltzmann approximation applies to carrier statistics. 

3. The concepts of low injection and complete ionization apply. 

4a. The total current is a constant throughout the entire pn structure. 

4b. The individual electron and hole currents are continuous functions through the pn structure. 

4c. The individual electron and hole currents are constant throughout the depletion region. 

Notation can sometimes appear to be overwhelming in the equations in this chapter. Table 8.1 lists some of the various electron and hole concentration terms that appear. Many terms have already been used in previous chapters but are repeated here for convenience. 


Table 8.1 | Commonly used terms and notation for this chapter


<table><tr><td>Term</td><td>Meaning</td></tr><tr><td><eq>N_{a}</eq></td><td>Acceptor concentration in the p region of the pn junction</td></tr><tr><td><eq>N_{d}</eq></td><td>Donor concentration in the n region of the pn junction</td></tr><tr><td><eq>n_{n0} = N_{d}</eq></td><td>Thermal-equilibrium majority carrier electron concentration in the n region</td></tr><tr><td><eq>p_{p0} = N_{a}</eq></td><td>Thermal-equilibrium majority carrier hole concentration in the p region</td></tr><tr><td><eq>n_{p0} = n_{i}^{2}/N_{a}</eq></td><td>Thermal-equilibrium minority carrier electron concentration in the p region</td></tr><tr><td><eq>p_{n0} = n_{i}^{2}/N_{d}</eq></td><td>Thermal-equilibrium minority carrier hole concentration in the n region</td></tr><tr><td><eq>n_{p}</eq></td><td>Total minority carrier electron concentration in the p region</td></tr><tr><td><eq>p_{n}</eq></td><td>Total minority carrier hole concentration in the n region</td></tr><tr><td><eq>n_{p}(-x_{p})</eq></td><td>Minority carrier electron concentration in the p region at the space charge edge</td></tr><tr><td><eq>p_{n}(x_{n})</eq></td><td>Minority carrier hole concentration in the n region at the space charge edge</td></tr><tr><td><eq>\delta n_{p} = n_{p} - n_{p0}</eq></td><td>Excess minority carrier electron concentration in the p region</td></tr><tr><td><eq>\delta p_{n} = p_{n} - p_{n0}</eq></td><td>Excess minority carrier hole concentration in the n region</td></tr></table>

## 8.1.3 Boundary Conditions

Figure 8.2 shows the conduction-band energy through the pn junction in thermal equilibrium. The n region contains many more electrons in the conduction band than the p region; the built-in potential barrier prevents this large density of electrons from fl owing into the p region. The built-in potential barrier maintains equilibrium between the carrier distributions on either side of the junction. 

An expression for the built-in potential barrier was derived in the last chapter and was given by Equation (7.10) as 

$$
V _ {b i} = V _ {t} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right)
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/9b5163dcf5efa242c0db364cd9ba65bb905a974b624065489c9dfb015f24f04b.jpg)



Figure 8.2 | Conduction-band energy through a pn junction.


If we divide the equation by $V _ { t } = k T / e$ , take the exponential of both sides, and then take the reciprocal, we obtain 

$$
\frac {n _ {i} ^ {2}}{N _ {a} N _ {d}} = \exp \left(\frac {- e V _ {b i}}{k T}\right) \tag {8.1}
$$

If we assume complete ionization, we can write 

$$
n _ {n 0} \approx N _ {d} \tag {8.2}
$$

where $n _ { n 0 }$ is the thermal-equilibrium concentration of majority carrier electrons in the n region. In the p region, we can write 

$$
n _ {p 0} \approx \frac {n _ {i} ^ {2}}{N _ {a}} \tag {8.3}
$$

where $n _ { p 0 }$ is the thermal-equilibrium concentration of minority carrier electrons. Substituting Equations (8.2) and (8.3) into Equation (8.1), we obtain 

$$
n _ {p 0} = n _ {n 0} \exp \left(\frac {- e V _ {b i}}{k T}\right) \tag {8.4}
$$

This equation relates the minority carrier electron concentration on the p side of the junction to the majority carrier electron concentration on the n side of the junction in thermal equilibrium. 

If a positive voltage is applied to the p region with respect to the n region, the potential barrier is reduced. Figure 8.3a shows a pn junction with an applied voltage $V _ { a } .$ The electric fi eld in the bulk p and n regions is normally very small. Essentially all of the applied voltage is across the junction region. The electric fi eld $\mathrm { E _ { a p p } }$ induced by the applied voltage is in the opposite direction to the thermal-equilibrium space charge electric fi eld, so the net electric fi eld in the space charge region is reduced below the equilibrium value. The delicate balance between diffusion and the E-fi eld force achieved at thermal equilibrium is upset. The electric fi eld force that prevented majority carriers from crossing the space charge region is reduced; majority carrier electrons from the n side are now injected across the depletion region into the p material, and majority carrier holes from the p side are injected across the depletion region into the n material. As long as the bias $V _ { a }$ is applied, the injection of carriers across the space charge region continues and a current is created in the pn junction. This bias condition is known as forward bias; the energy-band diagram of the forwardbiased pn junction is shown in Figure 8.3b. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/c0d0e6792842eeea159b53af30f9714b40c4c9863b4b581f2cd5d5ade70c6e83.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/8cc40f7d14da0553f01192808a4f79f1ecae26b0cac7a4776fca69dff1401995.jpg)



(b)



Figure 8.3 | (a) A pn junction with an applied forward-bias voltage showing the directions of the electric fi eld induced by $V _ { a }$ and the space charge electric fi eld. (b) Energy-band diagram of the forward- biased pn junction.


The potential barrier $V _ { b i }$ in Equation (8.4) can be replaced by $( V _ { b i } - V _ { a } )$ when the junction is forward biased. Equation (8.4) becomes 

$$
n _ {p} = n _ {n 0} \exp \left(\frac {- e (V _ {b i} - V _ {a})}{k T}\right) = n _ {n 0} \exp \left(\frac {- e V _ {b i}}{k T}\right) \exp \left(\frac {+ e V _ {a}}{k T}\right) \tag {8.5}
$$

If we assume low injection, the majority carrier electron concentration $n _ { n 0 } ,$ for example, does not change signifi cantly. However, the minority carrier concentration, $n _ { p } ,$ can deviate from its thermal-equilibrium value $n _ { p 0 }$ by orders of magnitude. Using Equation (8.4), we can write Equation (8.5) as 

$$
n _ {p} = n _ {p 0} \exp \left(\frac {e V _ {a}}{k T}\right) \tag {8.6}
$$

When a forward-bias voltage is applied to the pn junction, the junction is no longer in thermal equilibrium. The left side of Equation (8.6) is the total minority carrier electron concentration in the p region, which is now greater than the thermal equilibrium value. The forward-bias voltage lowers the potential barrier so that majority carrier electrons from the n region are injected across the junction into the p region, thereby increasing the minority carrier electron concentration. We have produced excess minority carrier electrons in the p region. 

When the electrons are injected into the p region, these excess carriers are subject to the diffusion and recombination processes we discussed in Chapter 6. Equation (8.6), then, is the expression for the minority carrier electron concentration at the edge of the space charge region in the p region. 

Exactly the same process occurs for majority carrier holes in the p region, which are injected across the space charge region into the n region under a forward-bias voltage. We can write that 

$$
p _ {n} = p _ {n 0} \exp \left(\frac {e V _ {a}}{k T}\right) \tag {8.7}
$$

where $p _ { n }$ is the concentration of minority carrier holes at the edge of the space charge region in the n region. Figure 8.4 shows these results. By applying a forward-bias voltage, we create excess minority carriers in each region of the pn junction. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/a8edb963281e05fa916227ec429f9fb3ed9954d1d6aea8c4f1d285c2b635bf94.jpg)



Figure 8.4 | Excess minority carrier concentrations at the space charge edges generated by the forward-bias voltage.


### EXAMPLE 8.1

Objective: Calculate the minority carrier concentrations at the edge of the space charge regions in a forward-biased pn junction. 

Consider a silicon pn junction at T  300 K. Assume the doping concentration in the n region is $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and the doping concentration in the p region is $\mathrm { N } _ { a } = 6 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and assume that a forward bias of 0.60 V is applied to the pn junction. 

#### ■ Solution

From Equations (8.6) and (8.7) and from Figure 8.4, we have 

$$
n _ {p} \left(- x _ {p}\right) = n _ {p o} \exp \left(\frac {e V _ {a}}{k T}\right) \quad \text { and } \quad p _ {n} (x _ {n}) = p _ {n o} \exp \left(\frac {e V _ {a}}{k T}\right)
$$

The thermal-equilibrium minority carrier concentrations are 

$$
n _ {p o} = \frac {n _ {i} ^ {2}}{N _ {a}} = \frac {(1 . 5 \times 1 0 ^ {1 0}) ^ {2}}{6 \times 1 0 ^ {1 5}} = 3. 7 5 \times 1 0 ^ {4} \mathrm{cm} ^ {- 3}
$$

and 

$$
p _ {n o} = \frac {n _ {i} ^ {2}}{N _ {d}} = \frac {(1 . 5 \times 1 0 ^ {1 0}) ^ {2}}{1 0 ^ {1 6}} = 2. 2 5 \times 1 0 ^ {4} \mathrm{cm} ^ {- 3}
$$

We then have 

$$
n _ {p} \left(- x _ {p}\right) = 3. 7 5 \times 1 0 ^ {4} \exp \left(\frac {0 . 6 0}{0 . 0 2 5 9}\right) = 4. 3 1 \times 1 0 ^ {1 4} \mathrm{cm} ^ {- 3}
$$

and 

$$
p _ {n} \left(x _ {n}\right) = 2. 2 5 \times 1 0 ^ {4} \exp \left(\frac {0 . 6 0}{0 . 0 2 5 9}\right) = 2. 5 9 \times 1 0 ^ {1 4} \mathrm{cm} ^ {- 3}
$$

#### ■ Comment

The minority carrier concentrations can increase by many orders of magnitude when a relatively small forward-bias voltage is applied. Low injection still applies, however, since the excess minority carrier concentrations at the space-charge edges are much less than the thermal-equilibrium majority carrier concentrations. 

#### ■ EXERCISE PROBLEM

Ex 8.1 A silicon pn junction at $T = 3 0 0 \mathrm { K }$ is doped with impurity concentrations of 

$N _ { d } = 2 \times 1 0 ^ { 1 6 }$ cm3 and $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The junction is forward biased at $V _ { a } = 0 . 6 5 0 \mathrm { V } .$ . Determine the minority carrier concentrations at the space charge edges. Does low injection still apply? 

$$
[ \text { Ans. } n _ {i} (- x _ {i}) = 3. 5 7 \times 1 0 ^ {1 4} \mathrm{cm} ^ {- 3}, p _ {n} (x _ {n}) = 8. 9 2 \times 1 0 ^ {1 4} \mathrm{cm} ^ {- 3}, \text { yes } ]
$$

The minority carrier concentrations at the space charge edges, given by Equations (8.6) and (8.7), were derived assuming that a forward-bias voltage $( V _ { a } > 0 )$ was applied across the pn junction. However, nothing in the derivation prevents $V _ { a }$ from being negative (reverse bias). If a reverse-biased voltage greater than a few tenths of a volt is applied to the pn junction, then we see from Equations (8.6) and (8.7) that the minority carrier concentrations at the space charge edge are essentially zero. The mino rity carrier concentrations for the reverse-biased condition drop below the thermal-equilibrium values. 

## 8.1.4 Minority Carrier Distribution

We developed, in Chapter 6, the ambipolar transport equation for excess minority carrier holes in an n region. This equation, in one dimension, is 

$$
D _ {p} \frac {\partial^ {2} (\delta p _ {n})}{\partial x ^ {2}} - \mu_ {p} \mathrm{E} \frac {\partial (\delta p _ {n})}{\partial x} + g ^ {\prime} - \frac {\delta p _ {n}}{\tau_ {p 0}} = \frac {\partial (\delta p _ {n})}{\partial t} \tag {8.8}
$$

where $\delta p _ { n } = p _ { n } - p _ { n 0 }$ is the excess minority carrier hole concentration and is the difference between the total and thermal equilibrium minority carrier concentrations. The ambipolar transport equation describes the behavior of excess carriers as a function of time and spatial coordinates. 

In Chapter 5, we calculated drift current densities in a semiconductor. We determined that relatively large currents could be created with fairly small electric fi elds. As a fi rst approximation, we assume that the electric fi eld is zero in both the neutral p and n regions. In the n region for $x > x _ { n } ,$ we have that E  0 and $g ^ { \prime } = 0$ . If we also assume steady state so $\partial ( \delta p _ { n } ) / \partial t = 0$ , then Equation (8.8) reduces to 

$$
\frac {d ^ {2} (\delta p _ {n})}{d x ^ {2}} - \frac {\delta p _ {n}}{L _ {p} ^ {2}} = 0 \quad (x > x _ {n}) \tag {8.9}
$$

where $L _ { p } ^ { 2 } = D _ { p } \tau _ { p 0 } .$ For the same set of conditions, the excess minority carrier electron concentration in the p region is determined from 

$$
\frac {d ^ {2} (\delta n _ {p})}{d x ^ {2}} - \frac {\delta n _ {p}}{L _ {n} ^ {2}} = 0 \quad (x <   x _ {p}) \tag {8.10}
$$

where $L _ { n } ^ { 2 } = D _ { n } \tau _ { n 0 }$ . 

The boundary conditions for the total minority carrier concentrations are 

$$
p _ {n} (x _ {n}) = p _ {n 0} \exp \left(\frac {e V _ {a}}{k T}\right) \tag {8.11a}
$$

$$
n _ {p} (- x _ {p}) = n _ {p 0} \exp \left(\frac {e V _ {a}}{k T}\right) \tag {8.11b}
$$

$$
p _ {n} (x \rightarrow + \infty) = p _ {n 0} \tag {8.11c}
$$

$$
n _ {p} (x \rightarrow - \infty) = n _ {p 0} \tag {8.11d}
$$

As minority carriers diffuse from the space charge edge into the neutral semiconductor regions, they recombine with majority carriers. We assume that the lengths $W _ { n }$ and $W _ { p }$ shown in Figure 8.3a are very long, meaning in particular that $W _ { n } \gg L _ { p }$ and $W _ { p } \gg L _ { n }$ . The excess minority carrier concentrations must approach zero at distances far from the space charge region. The structure is referred to as a long pn junction. 

The general solution to Equation (8.9) is 

$$
\delta p _ {n} (x) = p _ {n} (x) - p _ {n 0} = A e ^ {x / L _ {p}} + B e ^ {- x / L _ {p}} \quad (x \geq x _ {n}) \tag {8.12}
$$

and the general solution to Equation (8.10) is 

$$
\delta n _ {p} (x) = n _ {p} (x) - n _ {p 0} = C e ^ {x / L _ {n}} + D e ^ {- x / L _ {n}} \quad (x \leq - x _ {p}) \tag {8.13}
$$

Applying the boundary conditions from Equations (8.11c) and (8.11d), the coeffi cients A and D must be zero. The coeffi cients B and C may be determined from the boundary conditions given by Equations (8.11a) and (8.11b). The excess carrier concentrations are then found to be, for $( x \geq x _ { n } )$ , 

$$
\delta p _ {n} (x) = p _ {n} (x) - p _ {n 0} = p _ {n 0} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \exp \left(\frac {x _ {n} - x}{L _ {p}}\right) \tag {8.14}
$$

and, for $( x \leq - x _ { p } )$ , 

$$
\delta n _ {p} (x) = n _ {p} (x) - n _ {p 0} = n _ {p 0} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \exp \left(\frac {x _ {p} + x}{L _ {n}}\right) \tag {8.15}
$$

The minority carrier concentrations decay exponentially with distance away from the junction to their thermal-equilibrium values. Figure 8.5 shows these results. Again, we have assumed that both the n-region and the p-region lengths are long compared to the minority carrier diffusion lengths. 

In Chapter 6, we discussed the concept of quasi-Fermi levels, which apply to excess carriers in a nonequilibium condition. Since excess electrons exist in the neutral p region and excess holes exist in the neutral n region, we can apply quasi-Fermi levels to these regions. We had defi ned quasi-Fermi levels in terms of carrier concentrations as 

$$
p = p _ {o} + \delta p = n _ {i} \exp \left(\frac {E _ {F i} - E _ {F p}}{k T}\right) \tag {8.16}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/a0d71f6af394282c803e7a7d4e0b4e223a760627b534bed1b8f0a2d72ca85e23.jpg)



Figure 8.5 | Steady-state minority carrier concentrations in a pn junction under forward bias.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/542fbbf9461d5bd6a66a986b5cef0ef804fdb3b363e364991ddf460e27f54f51.jpg)



Figure 8.6 | Quasi-Fermi levels through a forward-biased pn junction.


and 

$$
n = n _ {o} + \delta n = n _ {i} \exp \left(\frac {E _ {F n} - E _ {F i}}{k T}\right) \tag {8.17}
$$

Figure 8.6 shows the quasi-Fermi levels through the pn junction. From Equations (8.14) and (8.15), the carrier concentrations are exponential functions of distance, and from Equations (8.16) and (8.17), the carrier concentrations are exponential functions of the quasi-Fermi levels. The quasi-Fermi levels are then linear functions of distance in the neutral p and n regions as shown in Figure 8.6. 

We may note that close to the space charge edge in the p region, $E _ { F n } - E _ { F i } > 0$ which means that $\delta n > n _ { i } .$ Further from the space charge edge, $E _ { F n } - E _ { F i } < 0$ which means that $\delta n < n _ { i }$ and the excess electron concentration is approaching zero. The same discussion applies to the excess hole concentration in the n region. 

At the space charge edge at $x = x _ { n } ,$ we can write, for low injection 

$$
n _ {o} p _ {n} (x _ {n}) = n _ {o} p _ {n o} \exp \left(\frac {V _ {a}}{V _ {t}}\right) = n _ {i} ^ {2} \exp \left(\frac {V _ {a}}{V _ {t}}\right) \tag {8.18}
$$

Combining Equations (8.16) and (8.17), we can write 

$$
n p = n _ {i} ^ {2} \exp \left(\frac {E _ {F n} - E _ {F p}}{k T}\right) \tag {8.19}
$$

Comparing Equations (8.18) and (8.19), the difference in quasi-Fermi levels is related to the applied bias $V _ { a }$ and represents the deviation from thermal equilibrium. The difference between $E _ { F n }$ and $E _ { F p }$ is nearly constant through the depletion region. 

To review, a forward-bias voltage lowers the built-in potential barrier of a pn junction so that electrons from the n region are injected across the space charge region, creating excess minority carriers in the p region. These excess electrons begin diffusing into the bulk p region where they can recombine with majority carrier holes. The excess minority carrier electron concentration then decreases with distance from the junction. The same discussion applies to holes injected across the space charge region into the n region. 

## 8.1.5 Ideal pn Junction Current

The approach we use to determine the current in a pn junction is based on the three parts of the fourth assumption stated earlier in this section. The total current in the junction is the sum of the individual electron and hole currents that are constant through the depletion region. Since the electron and hole currents are continuous functions through the pn junction, the total pn junction current will be the minority carrier hole diffusion current at $x = x _ { n }$ plus the minority carrier electron diffusion current at $x = - x _ { p }$ . The gradients in the minority carrier concentrations, as shown in Figure 8.5, produce diffusion currents, and since we are assuming the electric fi eld to be zero at the space charge edges, we can neglect any minority carrier drift current component. This approach in determining the pn junction current is shown in Figure 8.7. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/1735b28257c595bad3fe04b222dbdb2c4347f931267b7499ff30edf2a461f721.jpg)



Figure 8.7 | Electron and hole current densities through the space charge region of a pn junction.


We can calculate the minority carrier hole diffusion current density at $x = x _ { n }$ from the relation 

$$
J _ {p} (x _ {n}) = - e D _ {p} \frac {d p _ {n} (x)}{d x} \bigg | _ {x = x _ {n}} \tag {8.20}
$$

Since we are assuming uniformly doped regions, the thermal-equilibrium carrier concentration is constant, so the hole diffusion current density may be written as 

$$
J _ {p} (x _ {n}) = - e D _ {p} \frac {d (\delta p _ {n} (x))}{d x} \bigg | _ {x = x _ {n}} \tag {8.21}
$$

Taking the derivative of Equation (8.14) and substituting into Equation (8.21), we obtain 

$$
J _ {p} (x _ {n}) = \frac {e D _ {p} p _ {n 0}}{L _ {p}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.22}
$$

The hole current density for this forward-bias condition is in the x direction, which is from the p to the n region. 

Similarly, we may calculate the electron diffusion current density at $x = - x _ { p } ,$ This may be written as 

$$
J _ {n} (- x _ {p}) = e D _ {n} \left. \frac {d (\delta n _ {p} (x))}{d x} \right| _ {x = - x _ {p}} \tag {8.23}
$$

Using Equation (8.15), we obtain 

$$
J _ {n} (- x _ {p}) = \frac {e D _ {n} n _ {p 0}}{L _ {n}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.24}
$$

The electron current density is also in the x direction. 

An assumption we made at the beginning was that the individual electron and hole currents were continuous functions and constant through the space charge region. The total current is the sum of the electron and hole currents and is constant through the entire junction. Figure 8.7 again shows a plot of the magnitudes of these currents. 

The total current density in the pn junction is then 

$$
J = J _ {p} (x _ {n}) + J _ {n} (- x _ {p}) = \left[ \frac {e D _ {p} p _ {n 0}}{L _ {p}} + \frac {e D _ {n} n _ {p 0}}{L _ {n}} \right] \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.25}
$$

Equation (8.25) is the ideal current–voltage relationship of a pn junction. 

We may defi ne a parameter Js as 

$$
J _ {s} = \left[ \frac {e D _ {p} p _ {n 0}}{L _ {p}} + \frac {e D _ {n} n _ {p 0}}{L _ {n}} \right] \tag {8.26}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/04cb5458f785e36a0082f7434fb4f55c2d7c993b43c7779293c06801f6dced1d.jpg)



Figure 8.8 | Ideal I–V characteristic of a pn junction diode.


so that Equation (8.25) may be written as 

$$
J = J _ {s} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.27}
$$

Equation (8.27), known as the ideal-diode equation, gives a good description of the current–voltage characteristics of the pn junction over a wide range of currents and voltages. Although Equation (8.27) was derived assuming a forward-bias voltage $( V _ { a } > 0 )$ , there is nothing to prevent $V _ { a }$ from being negative (reverse bias). Equation (8.27) is plotted in Figure 8.8 as a function of forward-bias voltage $V _ { a } .$ If the voltage $V _ { a }$ becomes negative (reverse bias) by a few $k T / e \mathrm { V }$ , then the reverse-biased current density becomes independent of the reverse-biased voltage. The parameter $J _ { s }$ is then referred to as the reverse-saturation current density. The current–voltage characteristics of the pn junction diode are obviously not bilateral. 

## EXAMPLE 8.2

Objective: Determine the ideal reverse-saturation current density in a silicon pn junction at T  300 K. 

Consider the following parameters in a silicon pn junction: 

$$
N _ {a} = N _ {d} = 1 0 ^ {1 6} \mathrm{cm} ^ {- 3} \quad n _ {i} = 1. 5 \times 1 0 ^ {1 0} \mathrm{cm} ^ {- 3}
$$

$$
D _ {n} = 2 5 \mathrm{cm} ^ {2} / \mathrm{s} \quad \tau_ {p 0} = \tau_ {n 0} = 5 \times 1 0 ^ {- 7} \mathrm{s}
$$

$$
D _ {p} = 1 0 \mathrm{cm} ^ {2} / \mathrm{s} \quad \epsilon_ {r} = 1 1. 7
$$

#### ■ Solution

The ideal reverse-saturation current density is given by 

$$
J _ {s} = \frac {e D _ {n} n _ {p 0}}{L _ {n}} + \frac {e D _ {p} p _ {n 0}}{L _ {p}}
$$

which may be rewritten as 

$$
J _ {s} = e n _ {i} ^ {2} \left(\frac {1}{N _ {a}} \sqrt {\frac {D _ {n}}{\tau_ {n 0}}} + \frac {1}{N _ {d}} \sqrt {\frac {D _ {p}}{\tau_ {p 0}}}\right)
$$

Then 

$$
J _ {s} = (1. 6 \times 1 0 ^ {- 1 9}) (1. 5 \times 1 0 ^ {1 0}) ^ {2} \left(\frac {1}{1 0 ^ {1 6}} \sqrt {\frac {2 5}{5 \times 1 0 ^ {- 7}}} + \frac {1}{1 0 ^ {1 6}} \sqrt {\frac {1 0}{5 \times 1 0 ^ {- 7}}}\right)
$$

or $J _ { s } = 4 . 1 6 \times 1 0 ^ { - 1 1 } \mathrm { A / c m } ^ { 2 }$ 

#### ■ Comment

The ideal reverse-biased saturation current density is very small. If the pn junction crosssectional area were $\mathrm { A } = 1 0 ^ { - 4 } ~ \mathrm { c m } ^ { 2 }$ , for example, then the ideal reverse-biased diode current would be $I _ { s } = 4 . 1 5 \times 1 0 ^ { - 1 5 } \mathrm { A } .$ 

#### ■ EXERCISE PROBLEM

Ex 8.2 Consider a GaAs pn junction diode at $T = 3 0 0 \mathrm { K }$ . The parameters of the device are $N _ { d } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } , N _ { a } = 8 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } , D _ { n } = 2 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s } , D _ { p } = 8 \mathrm { c m } ^ { 2 } / \mathrm { s } , \tau _ { n o } = 1 0 ^ { - 7 } \mathrm { s } ,$ and ${ \tau _ { p o } } = 5 \times { 1 0 ^ { - 8 } } \mathrm { { s } }$ . Determine the ideal reverse-saturation current density. 

$$
(\text { Ans. } J _ {s} = 3. 3 0 \times 1 0 ^ {- 1 8} \text { A / cm } ^ {2})
$$

If the forward-bias voltage in Equation (8.27) is positive by more than a few $k T / e \mathrm { V }$ , then the (1) term in Equation (8.27) becomes negligible. Figure 8.9 shows the forward-bias current–voltage characteristic when the current is plotted on a log scale. Ideally, this plot yields a straight line when $V _ { a }$ is greater than a few $k T / e \mathrm { V }$ . The forward-bias current is an exponential function of the forward-bias voltage. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/45358225ab79bdc89d5d5ce95682b9ea44f04e7abfd5cad76a0941e0c0df57a4.jpg)



Figure 8.9 | Ideal I–V characteristic of a pn junction diode with the current plotted on a log scale.


## EXAMPLE 8.3

Objective: Design a pn junction diode to produce particular electron and hole current densities at a given forward-bias voltage. 

Consider a silicon pn junction diode at $T = 3 0 0 \mathrm { K }$ . Design the diode such that $J _ { n } { = } 2 0 \mathrm { A } / \mathrm { c m } ^ { 2 }$ and $J _ { p } = 5 ~ \mathrm { A } / \mathrm { c m } ^ { 2 }$ at $V _ { a } = 0 . 6 5$ V. Assume the remaining semiconductor parameters are as given in Example 8.2. 

#### ■ Solution

The electron diffusion current density is given by Equation (8.24) as 

$$
J _ {n} = \frac {e D _ {n} n _ {p 0}}{L _ {n}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] = e \sqrt {\frac {D _ {n}}{\tau_ {n 0}}} \cdot \frac {n _ {i} ^ {2}}{N _ {a}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right]
$$

Substituting the numbers, we have 

$$
2 0 = (1. 6 \times 1 0 ^ {- 1 9}) \sqrt {\frac {2 5}{5 \times 1 0 ^ {- 7}}} \cdot \frac {(1 . 5 \times 1 0 ^ {1 0}) ^ {2}}{N _ {a}} \left[ \exp \left(\frac {0 . 6 5}{0 . 0 2 5 9}\right) - 1 \right]
$$

which yields 

$$
N _ {a} = 1. 0 1 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}
$$

The hole diffusion current density is given by Equation (8.22) as 

$$
J _ {p} = \frac {e D _ {p} p _ {n 0}}{L _ {p}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] = e \sqrt {\frac {D _ {p}}{\tau_ {p 0}}} \cdot \frac {n _ {i} ^ {2}}{N _ {d}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right]
$$

Substituting the numbers, we have 

$$
5 = (1. 6 \times 1 0 ^ {- 1 9}) \sqrt {\frac {1 0}{5 \times 1 0 ^ {- 7}}} \cdot \frac {(1 . 5 \times 1 0 ^ {1 0}) ^ {2}}{N _ {d}} \left[ \exp \left(\frac {0 . 6 5}{0 . 0 2 5 9}\right) - 1 \right]
$$

which yields 

$$
N _ {d} = 2. 5 5 \times 1 0 ^ {1 5} \mathrm{cm} ^ {- 3}
$$

#### ■ Comment

The relative magnitude of the electron and hole current densities through a diode can be varied by changing the doping concentrations in the device. 

#### ■ EXERCISE PROBLEM

Ex 8.3 Using the parameters given in Ex 8.2 for the GaAs diode, determine the electron and hole current densities at the space charge edges, and determine the total current density in the diode for a forward-bias voltage of $V _ { a } = 1 . 0 5 \ : \mathrm { V }$ 

$$
[ \text { Ans. } f _ {i} (- x ^ {d}) = 1. 2 0   \text { A / cm } ^ {2}, f _ {j} (x _ {i}) = 0. 1 3 2 5   \text { A / cm } ^ {2}, J _ {T} = 1. 3 3   \text { A / cm } ^ {2} ]
$$

## 8.1.6 Summary of Physics

We have been considering the case of a forward-bias voltage being applied to a pn junction. The forward-bias voltage lowers the potential barrier so that electrons and holes are injected across the space charge region. The injected carriers become minority carriers which then diffuse from the junction and recombine with majority carriers. 

We calculated the minority carrier diffusion current densities at the edge of the space charge region. We can reconsider Equations (8.14) and (8.15) and determine the minority carrier diffusion current densities as a function of distance through the p and n regions. These results are 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/67669d1b2e93db8e996e7ec83a1c249ff7a076fc18c26535c54bad812bccae51.jpg)



Figure 8.10 | Ideal electron and hole current components through a pn junction under forward bias.


$$
J _ {p} (x) = \frac {e D _ {p} p _ {n 0}}{L _ {p}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \exp \left(\frac {x _ {n} - x}{L _ {p}}\right) \quad (x \geq x _ {n}) \tag {8.28}
$$

and 

$$
J _ {n} (x) = \frac {e D _ {n} n _ {p 0}}{L _ {n}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \exp \left(\frac {x _ {p} + x}{L _ {n}}\right) \quad (x \leq - x _ {p}) \tag {8.29}
$$

The minority carrier diffusion current densities decay exponentially in each region. However, the total current through the pn junction is constant. The difference between total current and minority carrier diffusion current is a majority carrier current. Figure 8.10 shows the various current components through the pn structure. The drift of majority carrier holes in the p region far from the junction, for example, is to supply holes that are being injected across the space charge region into the n region and also to supply holes that are lost by recombination with excess minority carrier electrons. The same discussion applies to the drift of electrons in the n region. 

We have seen that excess carriers are created in a forward-biased pn junction. From the results of the ambipolar transport theory derived in Chapter 6, the behavior of the excess carriers is determined by the minority carrier parameters for low injection. In determining the current–voltage relationship of the pn junction, we consider the fl ow of minority carriers since we know the behavior and characteristics of these particles. It may seem strange, at times, that we concern ourselves so much with minority carriers rather than with the vast number of majority carriers, but the reason for this can be found in the results derived from the ambipolar transport theory. 

The fact that we now have drift current densities in the p and n regions implies that the electric fi eld in these regions is not zero as we had originally assumed. We can calculate the electric fi eld in the neutral regions and determine the validity of our zero-fi eld approximation. 

### EXAMPLE 8.4

Objective: Calculate the electric fi eld in a neutral region of a silicon diode to produce a given majority carrier drift current density. 

Consider a silicon pn junction at T  300 K with the parameters given in Example 8.2 and with an applied forward-bias voltage $V _ { a } = 0 . 6 5 \mathrm { \ : V } .$ . 

#### ■ Solution

The total forward-bias current density is given by 

$$
J = J _ {s} \left[ \exp \left(\frac {e V}{k T}\right) - 1 \right]
$$

We determined the reverse-saturation current density in Example 8.2, so we can write 

$$
J = (4. 1 5 5 \times 1 0 ^ {- 1 1}) \left[ \exp \left(\frac {0 . 6 5}{0 . 0 2 5 9}\right) - 1 \right] = 3. 2 9 5 \mathrm{A} / \mathrm{cm} ^ {2}
$$

The total current far from the junction in the n region will be majority carrier electron drift current, so we can write 

$$
J = J _ {n} \approx e \mu_ {n} N _ {d} \mathrm{E}
$$

The doping concentration is $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , and, if we assume $\mu _ { n } = 1 3 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { \mathrm { - s } } ,$ , then the electric fi eld must be 

$$
\mathrm{E} = \frac {J _ {n}}{e \mu_ {n} N _ {d}} = \frac {3 . 2 9 5}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 3 5 0) (1 0 ^ {1 6})} = 1. 5 2 5 \mathrm{V/cm}
$$

#### ■ Comment

We assumed, in the derivation of the current–voltage equation, that the electric fi eld in the neutral p and n regions was zero. Although the electric fi eld is not zero, this example shows that the magnitude is very small—thus the approximation of zero electric fi eld is very good. 

#### ■ EXERCISE PROBLEM

Ex 8.4 Determine the electric fi eld in the neutral n region and neutral p region for the GaAs pn junction diode described in Ex 8.3. 

$$
(\text { Ans. } E _ {n} = 0. 0 6 9 4 \mathrm{V/cm}, E _ {p} = 3. 2 5 \mathrm{V/cm})
$$

## 8.1.7 Temperature Effects

The ideal reverse-saturation current density $J _ { s } ,$ given by Equation (8.26), is a function of the thermal-equilibrium minority carrier concentrations $n _ { p 0 }$ and $p _ { n 0 } .$ . These minority carrier concentrations are proportional to $n _ { i } ^ { 2 } .$ , which is a very strong function of temperature. For a silicon pn junction, the ideal reverse-saturation current density will increase by approximately a factor of 4 for every $1 0 ^ { \circ } \mathrm { C }$ increase in temperature. 

The forward-bias current–voltage relation is given by Equation (8.27). This relation includes Js as well as the exp (eVa /kT) factor, making the forward-bias current–voltage relation a function of temperature also. As temperature increases, less forward-bias voltage is required to obtain the same diode current. If the voltage is held constant, the diode current will increase as temperature increases. The change in forward-bias current with temperature is less sensitive than the reverse-saturation current. 

Objective: Determine the change in the forward-bias voltage on a pn junction with a change in temperature to maintain a constant diode current. 

Consider a silicon pn junction initially biased at 0.60 V at T  300 K. Assume the temperature increases to T  310 K. Calculate the change in the forward-bias voltage required to maintain a constant current through the junction. 

### EXAMPLE 8.5 

#### Solution

The forward-bias current can be written as follows: 

$$
J \propto \exp \left(\frac {- E _ {g}}{k T}\right) \exp \left(\frac {e V _ {a}}{k T}\right)
$$

If the temperature changes, we may take the ratio of the diode currents at the two temperatures. This ratio is 

$$
\frac {J _ {2}}{J _ {1}} = \frac {\exp (- E _ {g} / k T _ {2}) \exp (e V _ {a 2} / k T _ {2})}{\exp (- E _ {g} / k T _ {1}) \exp (e V _ {a 1} / k T _ {1})}
$$

If current is to be held constant, then $J _ { 1 } = J _ { 2 } ,$ , and we must have 

$$
\frac {E _ {g} - e V _ {a 2}}{k T _ {2}} = \frac {E _ {g} - e V _ {a 1}}{k T _ {1}}
$$

For $T _ { 1 } = 3 0 0 \mathrm { K } , T _ { 2 } = 3 1 0 \mathrm { K } , E _ { g } = 1 . 1 2 \mathrm { e V } ,$ and $V _ { a 1 } = 0 . 6 0 \mathrm { V }$ . We then fi nd 

$$
\frac {1 . 1 2 - V _ {a 2}}{3 1 0} = \frac {1 . 1 2 - 0 . 6 0}{3 0 0}
$$

which yields 

$$
V _ {a 2} = 0. 5 8 2 7 \mathrm{V}
$$

#### ■ Comment

The change in the forward-bias voltage is 17.3 mV for a $1 0 ^ { \circ } \mathrm { C }$ temperature change. 

#### ■ EXERCISE PROBLEM

Ex 8.5 Repeat Example 8.5 for a GaAs pn junction diode biased at $V _ { a } = 1 . 0 5 0 \mathrm { V }$ for $T =$ 300 K. 

$$
(\text { Ans. } - 1 2. 3 \text {   mV })
$$

## 8.1.8 The “Short” Diode

We assumed in the previous analysis that both p and n regions were long compared with the minority carrier diffusion lengths. In many pn junction structures, one region may, in fact, be short compared with the minority carrier diffusion length. Figure 8.11 shows one such example: the length $W _ { n }$ is assumed to be much smaller than the minority carrier hole diffusion length, $L _ { p }$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/12778c8de2b9318dda7e219e64f0bafaec86f01f91541821a1fd9dadacf86ac3.jpg)



Figure 8.11 | Geometry of a “short” diode.


The steady-state excess minority carrier hole concentration in the n region is determined from Equation (8.9), which is given as 

$$
\frac {d ^ {2} (\delta p _ {n})}{d x ^ {2}} - \frac {\delta p _ {n}}{L _ {p} ^ {2}} = 0
$$

The original boundary condition at $x = x _ { n }$ still applies, given by Equation (8.11a) as 

$$
p _ {n} (x _ {n}) = p _ {n 0} \exp \left(\frac {e V _ {a}}{k T}\right)
$$

A second boundary condition needs to be determined. In many cases we assume that an ohmic contact exists at $x = ( x _ { n } + W _ { n } )$ , implying an infi nite surface- recombination velocity and therefore an excess minority carrier concentration of zero. The second boundary condition is then written as 

$$
p _ {n} (x = x _ {n} + W _ {n}) = p _ {n 0} \tag {8.30}
$$

The general solution to Equation (8.9) is again given by Equation (8.12), which was 

$$
\delta p _ {n} (x) = p _ {n} (x) - p _ {n 0} = A e ^ {x / L _ {p}} + B e ^ {- x / L _ {p}} \quad (x \geq x _ {n})
$$

In this case, because of the fi nite length of the n region, both terms of the general solution must be retained. Applying the boundary conditions of Equations (8.11b) and (8.30), the excess minority carrier concentration is given by 

$$
\delta p _ {n} (x) = p _ {n 0} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \frac {\sinh \left[ (x _ {n} + W _ {n} - x) / L _ {p} \right]}{\sinh [ W _ {n} / L _ {p} ]} \tag {8.31}
$$

Equation (8.31) is the general solution for the excess minority carrier hole concentration in the n region of a forward-biased pn junction. If $W _ { n } \gg L _ { p } ,$ the assumption for the long diode, Equation (8.31) reduces to the previous result given by Equation (8.14). If $W _ { n } \ll L _ { p } ,$ we can approximate the hyperbolic sine terms by 

$$
\sinh \left(\frac {x _ {n} + W _ {n} - x}{L _ {p}}\right) \approx \left(\frac {x _ {n} + W _ {n} - x}{L _ {p}}\right) \tag {8.32a}
$$

and 

$$
\sinh \left(\frac {W _ {n}}{L _ {p}}\right) \approx \left(\frac {W _ {n}}{L _ {p}}\right) \tag {8.32b}
$$

Then Equation (8.31) becomes 

$$
\delta p _ {n} (x) = p _ {n 0} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \left(\frac {x _ {n} + W _ {n} - x}{W _ {n}}\right) \tag {8.33}
$$

The minority carrier concentration becomes a linear function of distance. 

The minority carrier hole diffusion current density is given by 

$$
J _ {p} = - e D _ {p} \frac {d [ \delta p _ {n} (x) ]}{d x}
$$

so that in the short n region, we have 

$$
J _ {p} (x) = \frac {e D _ {p} p _ {n 0}}{W _ {n}} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.34}
$$

The minority carrier hole diffusion current density now contains the length $W _ { n }$ in the denominator, rather than the diffusion length $L _ { p } .$ . The diffusion current density is larger for a short diode than for a long diode since $W _ { n } \ll L _ { p } .$ . In addition, since the minority carrier concentration is approximately a linear function of distance through the n re gion, the minority carrier diffusion current density is a constant. This constant current implies that there is no recombination of minority carriers in the short region. 

## TEST YOUR UNDERSTANDING

TYU 8.1 The doping concentrations in a GaAs pn junction diode at $T = 3 0 0 \mathrm { K }$ are 

$N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . The minority carrier concentration at either space charge edge is to be no larger than 10 percent of the respective majority carrier concentration. Calculate the maximum forward-bias voltage that can be applied to this junction and still meet the required specifi cations. 

$$
[ \text { Ans. } V _ {a} (\max) = 1. 0 6 7 \mathrm{V} ]
$$

TYU 8.2 A silicon pn junction at $T = 3 0 0$ K has the following parameters: $N _ { a } = 5 \times$ 

$1 0 ^ { 1 6 }$ cm $^ { \textmd { b } } , N _ { d } = 1 \times 1 0 ^ { 1 6 }$ cm3, Dn  25 cm2 /s, $D _ { p } = 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s } , \tau _ { n 0 } = 5 \times 1 0 ^ { - 7 } \mathrm { s } .$ and $\tau _ { p 0 } = 1 \times 1 0 ^ { - 7 } \mathrm { s } .$ . The cross-sectional area is $A = 1 0 ^ { - 3 } \mathrm { c m } ^ { 2 }$ and the forwardbias voltage is $V _ { a } = 0 . 6 2 5 \ : \mathrm { V }$ V. Calculate the (a) minority electron diffusion current at the space charge edge, (b) minority hole diffusion current at the space charge edge, and (c) total current in the pn junction diode. 

$$
[ \mathrm{Ans.} (a) 0. 1 5 4 \mathrm{mA}; (b) 1. 0 9 \mathrm{mA}; (c) 1. 2 4 \mathrm{mA} ]
$$

TYU 8.3 Consider the silicon pn junction diode described in TYU 8.2. The p region is long and the n region is short with $W _ { n } = 2 \ \mu \mathrm { m }$ . (a) Calculate the electron and hole currents in the depletion region. (b) Why has the hole current increased compared to that found in TYU 8.2? 

) The hole density gradient has increased.] b 5.44 mA; (  PI 0.154 mA.  nI ) a [Ans. ( 



# 8.2 | GENERATION–RECOMBINATION CURRENTS AND HIGH-INJECTION LEVELS

In the derivation of the ideal current–voltage relationship, we assumed low injection and neglected any effects occurring within the space charge region. High-level injection and other current components generated within the space charge region cause the I–V relationship to deviate from the ideal expression. The additional currents are generated from the recombination processes discussed in Chapter 6. 

## 8.2.1 Generation–Recombination Currents

The recombination rate of excess electrons and holes, given by the Shockley– Read– Hall recombination theory, was written as 

$$
R = \frac {C _ {n} C _ {p} N _ {t} (n p - n _ {i} ^ {2})}{C _ {n} (n + n ^ {\prime}) + C _ {p} (p + p ^ {\prime})} \tag {8.35}
$$

The parameters n and p are, as usual, the concentrations of electrons and holes, respectively. 

Reverse-Biased Generation Current For a pn junction under reverse bias, we have argued that the mobile electrons and holes have essentially been swept out of the space charge region. Accordingly, within the space charge region, $n \approx p \approx 0 .$ . The recombination rate from Equation (8.35) becomes 

$$
R = \frac {- C _ {n} C _ {p} N _ {i} n _ {i} ^ {2}}{C _ {n} n ^ {\prime} + C _ {p} p ^ {\prime}} \tag {8.36}
$$

The negative sign implies a negative recombination rate; hence, we are really generating electron–hole pairs within the reverse-biased space charge region. The recombination of excess electrons and holes is the process whereby we are trying to reestablish thermal equilibrium. Since the concentration of electrons and holes is essentially zero within the reverse-biased space charge region, electrons and holes are being generated via the trap level to also try to reestablish thermal equilibrium. This generation process is schematically shown in Figure 8.12. As the electrons and holes are generated, they are swept out of the space charge region by the electric fi eld. The fl ow of charge is in the direction of a reverse-biased current. This reverse-biased generation current, caused by the generation of electrons and holes in the space charge region, is in addition to the ideal reverse-biased saturation current. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/b1db259faf8f039a2398e1b2cba1fd97300a906b5752ff5dc9f9de2b1ca393f5.jpg)



Figure 8.12 | Generation process in a reverse-biased pn junction.


We may calculate the density of the reverse-biased generation current by considering Equation (8.36). If we make a simplifying assumption and let the trap level be at the intrinsic Fermi level, then from Equations (6.92) and (6.97), we have that $n ^ { \prime }$ $= n _ { i }$ and $p ^ { \prime } = n _ { i } .$ Equation (8.36) now becomes 

$$
R = \frac {- n _ {i}}{\frac {1}{N _ {t} C _ {p}} + \frac {1}{N _ {t} C _ {n}}} \tag {8.37}
$$

Using the defi nitions of lifetimes from Equations (6.103) and (6.104), we may write Equation (8.37) as 

$$
R = \frac {- n _ {i}}{\tau_ {p 0} + \tau_ {n 0}} \tag {8.38}
$$

If we defi ne a new lifetime as the average of $\tau _ { p 0 }$ and $\tau _ { n 0 } .$ , or 

$$
\tau_ {0} = \frac {\tau_ {p 0} + \tau_ {n 0}}{2} \tag {8.39}
$$

then the recombination rate can be written as 

$$
R = \frac {- n _ {i}}{2 \tau_ {0}} \equiv - G \tag {8.40}
$$

The negative recombination rate implies a generation rate, so G is the generation rate of electrons and holes in the space charge region. 

The generation current density may be determined from 

$$
J _ {\text { gen }} = \int_ {0} ^ {W} e G d x \tag {8.41}
$$

where the integral is over the space charge region. If we assume that the generation rate is constant throughout the space charge region, then we obtain 

$$
J _ {\text { gen }} = \frac {e n _ {i} W}{2 \tau_ {0}} \tag {8.42}
$$

The total reverse-biased current density is the sum of the ideal reverse saturation current density and the generation current density, or 

$$
J _ {R} = J _ {s} + J _ {\text { gen }} \tag {8.43}
$$

The ideal reverse-saturation current density $J _ { s }$ is independent of the reverse-biased voltage. However, $J _ { \mathrm { g e n } }$ is a function of the depletion width W, which in turn is a function of the reverse-biased voltage. The actual reverse-biased current density, then, is no longer independent of the reverse-biased voltage. 

### EXAMPLE 8.6

Objective: Determine the relative magnitudes of the ideal reverse-saturation current density and the generation current density in a reverse-biased pn junction. 

Consider a silicon pn junction at $T = 3 0 0 \mathrm { K }$ with parameters $D _ { n } = 2 5 \mathrm { c m } ^ { 2 } / \mathrm { s } , D _ { p } = 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s } ,$ , $N _ { a } = N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } ,$ , and $\tau _ { 0 } = \tau _ { n 0 } = \tau _ { p 0 } = 5 \times 1 0 ^ { - 7 } \mathrm { s }$ . Assume the diode is reverse biased at $V _ { R } = 5 \mathrm { V } .$ 

#### ■ Solution

The ideal reverse-saturation current density was calculated in Example 8.2 and was found to be $J _ { s } = 4 . 1 5 5 \times 1 0 ^ { - 1 1 } \mathrm { A } / \mathrm { c m } ^ { 2 }$ . 

The built-in potential is found as 

$$
V _ {b i} = V _ {t} \ln \left(\frac {N _ {a} N _ {d}}{n _ {i} ^ {2}}\right) = (0. 0 2 5 9) \ln \left[ \frac {(1 0 ^ {1 6}) (1 0 ^ {1 6})}{(1 . 5 \times 1 0 ^ {1 0}) ^ {2}} \right] = 0. 6 9 5 \mathrm{V}
$$

The depletion width is found to be 

$$
\begin{array}{l} W = \left\{\frac {2 \in_ {s} (V _ {b i} + V _ {R})}{e} \left(\frac {N _ {a} + N _ {d}}{N _ {a} N _ {d}}\right) \right\} ^ {1 / 2} \\ = \left\{\frac {2 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 6 9 5 + 5)}{1 . 6 \times 1 0 ^ {- 1 9}} \left[ \frac {1 0 ^ {1 6} + 1 0 ^ {1 6}}{(1 0 ^ {1 6}) (1 0 ^ {1 6})} \right] \right\} ^ {1 / 2} \\ = 1. 2 1 4 \times 1 0 ^ {- 4} \mathrm{cm} \\ \end{array}
$$

The generation current density is then found to be 

$$
J _ {\text { gen }} = \frac {e n _ {i} W}{2 \tau_ {0}} = \frac {(1 . 6 \times 1 0 ^ {- 1 9}) (1 . 5 \times 1 0 ^ {1 0}) (1 . 2 1 4 \times 1 0 ^ {- 4})}{2 (5 \times 1 0 ^ {- 7})}
$$

or 

$$
J _ {\mathrm{gen}} = 2. 9 1 4 \times 1 0 ^ {- 7} \mathrm {A / cm^ {2}}
$$

The ratio of the two currents is 

$$
\frac {J _ {\mathrm{gen}}}{J _ {s}} = \frac {2 . 9 1 4 \times 1 0 ^ {- 7}}{4 . 1 5 5 \times 1 0 ^ {- 1 1}} \cong 7 \times 1 0 ^ {3}
$$

#### ■ Comment

Comparing the solutions for the two current densities, it is obvious that, for the silicon pn junction diode at room temperature, the generation current density is approximately four orders of magnitude larger than the ideal saturation current density. The generation current is the dominant reverse-biased current in a silicon pn junction diode. 

#### ■ EXERCISE PROBLEM

Ex 8.6 Consider a GaAs pn junction diode at $T = 3 0 0 \mathrm { K }$ with parameters $N _ { d } = 8 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ , $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } , D _ { n } = 2 0 7 \mathrm { c m } ^ { 2 } / \mathrm { s } , D _ { p } = 9 . 8 0 \mathrm { c m } ^ { 2 } / \mathrm { s } ,$ and $\tau _ { 0 } = \tau _ { p 0 } = \tau _ { n 0 } = 5 \times$ $1 0 ^ { - 8 } \mathrm { s } . ( a )$ Calculate the ideal reverse-biased saturation current density. (b) Find the reverse-biased generation current density if the diode is reverse biased at $V _ { R } = 5 \mathrm { V }$ . (c) Determine the ratio of $J _ { \mathrm { g e n } } \tan J _ { s } .$ 

$$
[ \text { Ans. } (a) 1. 6 7 7 \times 1 0 ^ {- 1 7} \mathrm{A/cm} ^ {2}; (b) 6. 1 6 6 \times 1 0 ^ {- 1 0} \mathrm{A/cm} ^ {2}; (c) 3. 6 8 \times 1 0 ^ {7} ]
$$

Forward-Bias Recombination Current For the reverse-biased pn junction, electrons and holes are essentially completely swept out of the space charge region so that $n \approx p \approx 0 .$ . Under forward bias, however, electrons and holes are injected across the space charge region, so we do, in fact, have some excess carriers in the space charge region. The possibility exists that some of these electrons and holes will recombine within the space charge region and not become part of the minority carrier distribution. 

The recombination rate of electrons and holes is again given from Equation (8.35) as 

$$
R = \frac {C _ {n} C _ {p} N _ {t} \left(n p - n _ {i} ^ {2}\right)}{C _ {n} \left(n + n ^ {\prime}\right) + C _ {p} \left(p + p ^ {\prime}\right)}
$$

Dividing both numerator and denominator by $C _ { n } C _ { p } N _ { t }$ and using the defi nitions of $\tau _ { n 0 }$ and $\tau _ { p 0 } ,$ we may write the recombination rate as 

$$
R = \frac {n p - n _ {i} ^ {2}}{\tau_ {p 0} (n + n ^ {\prime}) + \tau_ {n 0} (p + p ^ {\prime})} \tag {8.44}
$$

Figure 8.13 shows the energy-band diagram of the forward-biased pn junction. Shown in the fi gure are the intrinsic Fermi level and the quasi-Fermi levels for electrons and holes. From the results of Chapter 6, we may write the electron concentration as 

$$
n = n _ {i} \exp \left[ \frac {E _ {F n} - E _ {F i}}{k T} \right] \tag {8.45}
$$

and the hole concentration as 

$$
p = n _ {i} \exp \left[ \frac {E _ {F i} - E _ {F p}}{k T} \right] \tag {8.46}
$$

where $E _ { F n }$ and $E _ { F p }$ are the quasi-Fermi levels for electrons and holes, respectively. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/c20f6db51318cfab718f47892537c38ae7e829ed61d11063ea8088cb58f2b14f.jpg)



Figure 8.13 | Energy-band diagram of a forward-biased pn junction including quasi-Fermi levels.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/41c5dff9c808f70d4ef83284ca2d723666977fe8ff407c05749823ed7f03afa4.jpg)



Figure 8.14 | Relative magnitude of the recombination rate through the space charge region of a forward-biased pn junction.


From Figure 8.13, we may note that 

$$
\left(E _ {F n} - E _ {F i}\right) + \left(E _ {F i} - E _ {F p}\right) = e V _ {a} \tag {8.47}
$$

where $V _ { a }$ is the applied forward-bias voltage. Again, if we assume that the trap level is at the intrinsic Fermi level, then $n ^ { \prime } = p ^ { \prime } = n _ { i } .$ Figure 8.14 shows a plot of the relative magnitude of the recombination rate as a function of distance through the space charge region. This plot was generated using Equations (8.44), (8.45), (8.46), and (8.47). A very sharp peak occurs at the metallurgical junction (x  0). 

At the center of the space charge region, we have 

$$
E _ {F n} - E _ {F i} = E _ {F i} - E _ {F p} = \frac {e V _ {a}}{2} \tag {8.48}
$$

Equations (8.45) and (8.46) then become 

$$
n = n _ {i} \exp \left(\frac {e V _ {a}}{2 k T}\right) \tag {8.49}
$$

and 

$$
p = n _ {i} \exp \left(\frac {e V _ {a}}{2 k T}\right) \tag {8.50}
$$

If we assume that $n ^ { \prime } = p ^ { \prime } = n _ { i }$ and that $\tau _ { n 0 } = \tau _ { p 0 } = \tau _ { 0 } ,$ then Equation (8.44) becomes 

$$
R _ {\max} = \frac {n _ {i}}{2 \tau_ {0}} \frac {[ \exp (e V _ {a} / k T) - 1 ]}{[ \exp (e V _ {a} / 2 k T) + 1 ]} \tag {8.51}
$$

which is the maximum recombination rate for electrons and holes that occurs at the center of the forward-biased pn junction. If we assume that $V _ { a } \gg k T / e$ , we may neglect the (1) term in the numerator and the (1) term in the denominator. Equation (8.51) then becomes 

$$
R _ {\max} = \frac {n _ {i}}{2 \tau_ {0}} \exp \left(\frac {e V _ {a}}{2 k T}\right) \tag {8.52}
$$

The recombination current density may be calculated from 

$$
J _ {\mathrm{rec}} = \int_ {0} ^ {W} e R d x \tag {8.53}
$$

where again the integral is over the entire space charge region. In this case, however, the recombination rate is not a constant through the space charge region. We have calculated the maximum recombination rate at the center of the space charge region, so we may write 

$$
J _ {\mathrm{rec}} = e x ^ {\prime} \frac {n _ {i}}{2 \tau_ {0}} \exp \left(\frac {e V _ {a}}{2 k T}\right) \tag {8.54}
$$

where x	 is a length over which the maximum recombination rate is effective. How ever, since $\tau _ { 0 }$ may not be a well-defi ned or known parameter, it is customary to write 

$$
J _ {\mathrm{rec}} = \frac {e W n _ {i}}{2 \tau_ {0}} \exp \left(\frac {e V _ {a}}{2 k T}\right) = J _ {r 0} \exp \left(\frac {e V _ {a}}{2 k T}\right) \tag {8.55}
$$

where W is the space charge width. 

Total Forward-Bias Current The total forward-bias current density in the pn junction is the sum of the recombination and the ideal diffusion current densities. Figure 8.15 shows a plot of the minority carrier hole concentration in the neutral n region. This distribution yields the ideal hole diffusion current density and is a function of the minority carrier hole diffusion length and the applied junction voltage. The distribution is established as a result of holes being injected across the space charge region. If, now, some of the injected holes in the space charge region are lost due to recombination, then additional holes must be injected from the p region to make up for this loss. The fl ow of these additional injected carriers, per unit time, results in the recombination current. This added component is schematically shown in the fi gure. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/1ffd9882879c2e98df5adf3f318240b577484b948e856b4cf9fb205108688099.jpg)



Figure 8.15 | Because of recombination, additional holes from the p region must be injected into the space charge region to establish the minority carrier hole concentration in the n region.


The total forward-bias current density is the sum of the recombination and the ideal diffusion current densities, so we can write 

$$
J = J _ {\mathrm{rec}} + J _ {D} \tag {8.56}
$$

where $J _ { \mathrm { r e c } }$ is given by Equation (8.55) and $J _ { D }$ is given by 

$$
J _ {D} = J _ {s} \exp \left(\frac {e V _ {a}}{k T}\right) \tag {8.57}
$$

The (1) term in Equation (8.27) has been neglected. The parameter $J _ { s }$ is the ideal reverse-saturation current density, and from previous discussion, the value of $J _ { r 0 }$ from the recombination current is larger than the value of $J _ { s }$ . 

If we take the natural log of Equations (8.55) and (8.57), we obtain 

$$
\ln J _ {\mathrm{rec}} = \ln J _ {r 0} + \frac {e V _ {a}}{2 k T} = \ln J _ {r 0} + \frac {V _ {a}}{2 V _ {t}} \tag {8.58a}
$$

and 

$$
\ln J _ {D} = \ln J _ {s} + \frac {e V _ {a}}{k T} = \ln J _ {s} + \frac {V _ {a}}{V _ {t}} \tag {8.58b}
$$

Figure 8.16 shows the recombination and diffusion current components plotted on a log current scale as a function of $V _ { a } / V _ { t } .$ . The slopes of the two curves are not the same. Also shown in the fi gure is the total current density—the sum of the two current components. We may notice that, at a low current density, the recombination current dominates, and at a higher current density, the ideal diffusion current dominates. 

In general, the diode current–voltage relationship may be written as 

$$
I = I _ {s} \left[ \exp \left(\frac {e V _ {a}}{n k T}\right) - 1 \right] \tag {8.59}
$$

where the parameter n is called the ideality factor. For a large forward-bias voltage, $n \approx 1$ when diffusion dominates, and for low forward-bias voltage, $n \approx 2$ when recombination dominates. There is a transition region where $1 < n < 2$ . 

## 8.2.2 High-Level Injection

In the derivation of the ideal diode I–V relationship, we assumed that low injection was valid. Low injection implies that the excess minority carrier concentrations are always much less than the majority carrier concentration. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/e679b85f6906f03dd0612ea91c7c304fa5f4f4bbf045778b01467c749eb78c60.jpg)



Figure 8.16 | Ideal diffusion, recombination, and total current in a forward-biased pn junction.


However, as the forward-bias voltage increases, the excess carrier concentrations increase and may become comparable or even greater than the majority carrier concentration. From Equation (8.18), we can write 

$$
n p = n _ {i} ^ {2} \exp \left(\frac {V _ {a}}{V _ {t}}\right)
$$

We have that $n = n _ { o } + \delta n$ and $p = p _ { o } + \delta p$ , so that 

$$
(n _ {o} + \delta n) (p _ {o} + \delta p) = n _ {i} ^ {2} \exp \left(\frac {V _ {a}}{V _ {t}}\right) \tag {8.60}
$$

Under high-level injection, we may have $\delta n > n _ { o }$ and $\delta p > p _ { o }$ so that Equation (8.60) becomes approximately 

$$
(\delta n) (\delta p) \cong n _ {i} ^ {2} \exp \left(\frac {V _ {a}}{V _ {t}}\right) \tag {861}
$$

Since $\delta n = \delta p$ , then 

$$
\delta n = \delta p \cong n _ {i} \exp \left(\frac {V _ {a}}{2 V _ {t}}\right) \tag {8.62}
$$

The diode current is proportional to the excess carrier concentration so that, under high-level injection, we have 

$$
I \propto \exp \left(\frac {V _ {a}}{2 V _ {t}}\right) \tag {8.63}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/69c6c7e400f23330e67fda98e63dd27e4915b49027b16fce285c7f7aae992ff2.jpg)



Figure 8.17 | Forward-bias current versus voltage from low forward bias to high forward bias.


In the high-level injection region, it takes a larger increase in diode voltage to produce a given increase in diode current. 

The diode forward-bias current, from low-bias levels to high-bias levels, is plotted in Figure 8.17. This plot shows the effect of recombination at low-bias voltages and high-level injection at high-bias voltages. 

## TEST YOUR UNDERSTANDING

TYU 8.4 Consider a silicon pn junction diode at T  300 K with parameters $N _ { a } = 2 \times$ $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } , N _ { d } = 8 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } , D _ { p } = 1 0 \mathrm { c m } ^ { 2 } / \mathrm { s } , D _ { n } = 2 5 \mathrm { c m } ^ { 2 } / \mathrm { s } ,$ and $\tau _ { 0 } = \tau _ { p 0 } =$ $\tau _ { n 0 } = 1 0 ^ { - 7 }$ s. The diode is forward biased at $V _ { a } = 0 . 3 5 \ : \mathrm { V } .$ . (a) Calculate the ideal diode current density. (b) Find the forward-biased recombination current density. (c) Determine the ratio of recombination current to the ideal diffusion current. ) 2.35] c( $\dot { \varsigma } _ { \zeta } \mathrm { U } \mathsf { 2 } / \mathsf { V } _ { \mathsf { \Delta } \nu - } \mathrm { 0 } \mathrm { I } \times \mathsf { 0 } \mathsf { Z } \mathsf { 0 } ^ { \circ } \mathsf { S } \left( q \right) \dot { \varsigma } _ { \zeta } \mathrm { U } \mathsf { 3 } / \mathsf { V } _ { \mathsf { \Delta } \nu - } \mathrm { 0 } \mathrm { I } \times \mathsf {  { \angle } \mathrm { \xi } } \mathrm { I } ^ { \circ } \left( \mathsf { \Delta } p \right)$ [Ans. 

# 8.3 | SMALL-SIGNAL MODEL OF THE pn JUNCTION

We have been considering the dc characteristics of the pn junction diode. When semiconductor devices with pn junctions are used in linear amplifi er circuits, for example, sinusoidal signals are superimposed on the dc currents and voltages, so that the small-signal characteristics of the pn junction become important. 

## 8.3.1 Diffusion Resistance

The ideal current–voltage relationship of the pn junction diode was given by Equation (8.27), where J and $J _ { s }$ are current densities. If we multiply both sides of the equation by the junction cross-sectional area, we have 

$$
I _ {D} = I _ {s} \left[ \exp \left(\frac {e V _ {a}}{k T}\right) - 1 \right] \tag {8.64}
$$

where $I _ { D }$ is the diode current and $I _ { s }$ is the diode reverse-saturation current. 

Assume that the diode is forward-biased with a dc voltage $V _ { 0 }$ producing a dc diode current $I _ { D Q } .$ . If we now superimpose a small, low-frequency sinusoidal voltage as shown in Figure 8.18, then a small sinusoidal current will be produced, superimposed on the dc current. The ratio of sinusoidal current to sinusoidal voltage is called the incremental conductance. In the limit of a very small sinusoidal current and voltage, the small-signal incremental conductance is just the slope of the dc current–voltage curve, or 

$$
g _ {d} = \left. \frac {d I _ {D}}{d V _ {a}} \right| _ {V _ {a} = V _ {0}} \tag {8.65}
$$

The reciprocal of the incremental conductance is the incremental resistance, defi ned as 

$$
r _ {d} = \left. \frac {d V _ {a}}{d I _ {D}} \right| _ {I _ {D} = I _ {D Q}} \tag {8.66}
$$

where $I _ { D Q }$ is the dc quiescent diode current. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/e1fe8eb49401227640de2369b4ea51faaebd7d14a32bed2311460421193afb67.jpg)



Figure 8.18 | Curve showing the concept of the small-signal diffusion resistance.


If we assume that the diode is biased suffi ciently far in the forward-bias region, then the (1) term can be neglected and the incremental conductance becomes 

$$
g _ {d} = \left. \frac {d I _ {D}}{d V _ {a}} \right| _ {V _ {a} = V _ {0}} = \left(\frac {e}{k T}\right) I _ {s} \exp \left(\frac {e V _ {0}}{k T}\right) \approx \frac {I _ {D Q}}{V _ {t}} \tag {8.67}
$$

The small-signal incremental resistance is then the reciprocal function, or 

$$
\boxed {r _ {d} = \frac {V _ {t}}{I _ {D Q}}} \tag {8.68}
$$

The incremental resistance decreases as the bias current increases, and is inversely proportional to the slope of the I–V characteristic as shown in Figure 8.18. The incremental resistance is also known as the diffusion resistance. 

## 8.3.2 Small-Signal Admittance

In the last chapter, we considered the pn junction capacitance as a function of the reverse-biased voltage. When the pn junction diode is forward-biased, another capacitance becomes a factor in the diode admittance. The small-signal admittance, or impedance, of the pn junction under forward bias is derived using the minority carrier diffusion current relations we have already considered. 

Qualitative Analysis Before we delve into the mathematical analysis, we can qualitatively understand the physical processes that lead to a diffusion capacitance, which is one component of the junction admittance. Figure 8.19a schematically shows a pn junction forward biased with a dc voltage. A small ac voltage is also superimposed on the dc voltage so that the total forward-biased voltage can be written as $V _ { a } = V _ { \mathrm { d c } } + \hat { \nu }$ sin t. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/f20e276792bc6978438c07f18bf515151f096e38c26e57ba3c8ea65c32434c12.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/fc05d1c0949de90f6c636c02d04da20168e1c7eab409ecbdd32bd8a9b7341758.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/f3f7d5147112f62be55fea418a65a3fa55758dfca43145c1ee0f4f75e4199e5d.jpg)



Figure 8.19 | (a) A pn junction with an ac voltage superimposed on a forward-biased dc value; (b) the hole concentration versus time at the space charge edge; (c) the hole concentration versus distance in the n region at three different times.


As the voltage across the junction changes, the number of holes injected across the space charge region into the n region also changes. Figure 8.19b shows the hole concentration at the space charge edge as a function of time. At $t = t _ { 0 } ,$ the ac voltage is zero so that the concentration of holes at $x = 0$ is just given by $p _ { n } ( 0 ) =$ $p _ { n 0 } \exp { ( V _ { \mathrm { d c } } / V _ { t } ) }$ , which is what we have seen previously. 

Now, as the ac voltage increases during its positive half cycle, the concentration of holes at $x = 0$ will increase and reach a peak value at $t = t _ { 1 } .$ , which corresponds to the peak value of the ac voltage. When the ac voltage is on its negative half cycle, the total voltage across the junction decreases so that the concentration of holes at $x = 0$ decreases. The concentration reaches a minimum value at $t = t _ { 2 } ,$ which corresponds to the time that the ac voltage reaches its maximum negative value. The minority carrier hole concentration at $x = 0 .$ , then, has an ac component superimposed on the dc value as indicated in Figure 8.19b. 

As previously discussed, the holes at the space charge edge $( x = 0 )$ diffuse into the n region where they recombine with the majority carrier electrons. We assume that the period of the ac voltage is large compared to the time it takes carriers to diffuse into the n region. The hole concentration as a function of distance into the n region can then be treated as a steady-state distribution. Figure 8.19c shows the steady-state hole concentrations at three different times. $\mathrm { A t } ~ t = t _ { 0 } ,$ the ac voltage is zero, so the $t = t _ { 0 }$ curve corresponds to the hole distribution established by the dc voltage. The $t = t _ { 1 }$ curve corresponds to the distribution established when the ac voltage has reached its peak positive value, and the $t = t _ { 2 }$ curve corresponds to the distribution established when the ac voltage has reached its maximum negative value. The shaded areas represents the charge $\Delta Q$ that is alternately charged and discharged during the ac voltage cycle. 

Exactly the same process is occurring in the p region with the electron concentration. The mechanism of charging and discharging of holes in the n region and electrons in the p region leads to a capacitance. This capacitance is called diffusion capacitance. The physical mechanism of this diffusion capacitance is different from that of the junction capacitance discussed in the last chapter. We show that the magnitude of the diffusion capacitance in a forward-biased pn junction is usually substantially larger than the junction capacitance. 

Mathematical Analysis The minority carrier distribution in the pn junction will be derived for the case when a small sinusoidal voltage is superimposed on the dc junction voltage. We can then determine small signal, or ac, diffusion currents from these minority carrier functions. Figure 8.20 shows the minority carrier distribution in a pn junction when a forward-biased dc voltage is applied. The origin, $x = 0$ , is set at the edge of the space charge region on the n side for convenience. The minority carrier hole concentration at $x = 0$ is given by Equation (8.7) as $p _ { n } ( 0 ) =$ pn0 exp $( e V _ { a } / k T )$ , where $V _ { a }$ is the applied voltage across the junction. 

Now let 

$$
V _ {a} = V _ {0} + v _ {1} (t) \tag {8.69}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/3c6363d37cb9d079388167dafcb0a543aa69471609f3c511f3d7aadd19bdc1a7.jpg)



Figure 8.20 | The dc characteristics of a forward-biased pn junction used in the small-signal admittance calculations.


where $V _ { 0 }$ is the dc quiescent bias voltage and $v _ { 1 } ( t )$ is the ac signal voltage that is superimposed on this dc level. We may now write 

$$
p _ {n} (x = 0) = p _ {n 0} \exp \left\{\frac {e [ V _ {0} + v _ {1} (t) ]}{k T} \right\} = p _ {n} (0, t) \tag {8.70}
$$

Equation (8.70) may be written as 

$$
p _ {n} (0, t) = p _ {\mathrm{dc}} \exp \left[ \frac {e v _ {1} (t)}{k T} \right] \tag {8.71}
$$

where 

$$
p _ {\mathrm{dc}} = p _ {n 0} \exp \left(\frac {e V _ {0}}{k T}\right) \tag {8.72}
$$

If we assume that $| v _ { 1 } ( t ) | \ll ( k T / e ) = V _ { t } ,$ , then the exponential term in Equation (8.71) may be expanded into a Taylor series retaining only the linear terms, and the minority carrier hole concentration at $x = 0$ can be written as 

$$
p _ {n} (0, t) \approx p _ {\mathrm{dc}} \left[ 1 + \frac {v _ {1} (t)}{V _ {t}} \right] \tag {8.73}
$$

If we assume that the time-varying voltage $v _ { 1 } ( t )$ is a sinusoidal signal, we can write Equation (8.73) as 

$$
p _ {n} (0, t) = p _ {\mathrm{dc}} \left(1 + \frac {\hat {V} _ {1}}{V _ {t}} e ^ {j \omega t}\right) \tag {8.74}
$$

where $\hat { V } _ { 1 }$ is the phasor of the applied sinusoidal voltage. Equation (8.74) will be used as the boundary condition in the solution of the time-dependent diffusion equation for the minority carrier holes in the n region. 

In the neutral n region $( x > 0 )$ , the electric fi eld is assumed to be zero; thus, the behavior of the excess minority carrier holes is determined from the equation 

$$
D _ {p} \frac {\partial^ {2} (\delta p _ {n})}{\partial x ^ {2}} - \frac {\delta p _ {n}}{\tau_ {p 0}} = \frac {\partial (\delta p _ {n})}{\partial t} \tag {8.75}
$$

where $\delta p _ { n }$ is the excess hole concentration in the n region. We are assuming that the ac signal voltage $v _ { 1 } \left( t \right)$ is sinusoidal. We then expect the steady-state solution for $\delta p _ { r }$ to be of the form of a sinusoidal solution superimposed on the dc solution, or 

$$
\delta p _ {n} (x, t) = \delta p _ {0} (x) + p _ {1} (x) e ^ {j \omega t} \tag {8.76}
$$

where $\delta p _ { 0 } ( x )$ is the dc excess carrier concentration and $p _ { 1 } ( x )$ is the magnitude of the ac component of the excess carrier concentration. The expression for $\delta p _ { 0 } ( x )$ is the same as that given in Equation (8.14). 

Substituting Equation (8.76) into the differential Equation (8.75), we obtain 

$$
D _ {p} \left\{\frac {\partial^ {2} [ \delta p _ {0} (x) ]}{\partial x ^ {2}} + \frac {\partial^ {2} p _ {1} (x)}{\partial x ^ {2}} e ^ {j \omega t} \right\} - \frac {\delta p _ {0} (x) + p _ {1} (x) e ^ {j \omega t}}{\tau_ {p 0}} = j \omega p _ {1} (x) e ^ {j \omega t} \tag {8.77}
$$

We may rewrite this equation, combining the time-dependent and time-independent terms, as 

$$
\left\{\frac {D _ {p} \partial^ {2} [ \delta p _ {0} (x) ]}{\partial x ^ {2}} - \frac {\delta p _ {0} (x)}{\tau_ {p 0}} \right\} + \left[ D _ {p} \frac {\partial^ {2} p _ {1} (x)}{\partial x ^ {2}} - \frac {p _ {1} (x)}{\tau_ {p 0}} - j \omega p _ {1} (x) \right] e ^ {j \omega t} = 0 \tag {8.78}
$$

If the ac component, $p _ { 1 } ( x )$ , is zero, then the fi rst bracketed term is just the differential Equation (8.10), which is identically zero. Then we have, from the second bracketed term, 

$$
D _ {p} \frac {d ^ {2} p _ {1} (x)}{d x ^ {2}} - \frac {p _ {1} (x)}{\tau_ {p 0}} - j \omega p _ {1} (x) = 0 \tag {8.79}
$$

Noting that $L _ { p } ^ { 2 } = D _ { p } \tau _ { p 0 } .$ Equation (8.79) may be rewritten in the form 

$$
\frac {d ^ {2} p _ {1} (x)}{d x ^ {2}} - \frac {(1 + j \omega \tau_ {p 0})}{L _ {p} ^ {2}} p _ {1} (x) = 0 \tag {8.80}
$$

or 

$$
\frac {d ^ {2} p _ {1} (x)}{d x ^ {2}} - C _ {p} ^ {2} p _ {1} (x) = 0 \tag {8.81}
$$

where 

$$
C _ {p} ^ {2} = \frac {(1 + j \omega \tau_ {p 0})}{L _ {p} ^ {2}} \tag {8.82}
$$

The general solution to Equation (8.81) is 

$$
p _ {1} (x) = K _ {1} e ^ {- C _ {p} x} + K _ {2} e ^ {+ C _ {p} x} \tag {8.83}
$$

One boundary condition is that $p _ { 1 } ( x  + \infty ) = 0$ , which implies that the coeffi cient $K _ { 2 } = 0$ . Then 

$$
p _ {1} (x) = K _ {1} e ^ {- C _ {p} x} \tag {8.84}
$$

Applying the boundary condition at $x = 0$ from Equation (8.74), we obtain 

$$
p _ {1} (0) = K _ {1} = p _ {\mathrm{dc}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \tag {8.85}
$$

The hole diffusion current density can be calculated at x  0. This is given by 

$$
J _ {p} = - e D _ {p} \left. \frac {\partial p _ {n}}{\partial x} \right| _ {x = 0} \tag {8.86}
$$

If we consider a homogeneous semiconductor, the derivative of the hole concentration will be just the derivative of the excess hole concentration. Then 

$$
J _ {p} = - e D _ {p} \left. \frac {\partial (\delta p _ {n})}{\partial x} \right| _ {x = 0} = - e D _ {p} \left. \frac {\partial [ \delta p _ {0} (x) ]}{\partial x} \right| _ {x = 0} - e D _ {p} \left. \frac {\partial p _ {1} (x)}{\partial x} \right| _ {x = 0} e ^ {j \omega t} \tag {8.87}
$$

We can write this equation in the form 

$$
J _ {p} = J _ {p 0} + j _ {p} (t) \tag {8.88}
$$

where 

$$
J _ {p 0} = - e D _ {p} \frac {\partial [ \delta p _ {0} (x) ]}{\partial x} \bigg | _ {x = 0} = \frac {e D _ {p} p _ {n 0}}{L _ {p}} \left[ \exp \left(\frac {e V _ {0}}{k T}\right) - 1 \right] \tag {8.89}
$$

Equation (8.89) is the dc component of the hole diffusion current density and is exactly the same as in the ideal I–V relation derived previously. 

The sinusoidal component of the diffusion current density is then found from 

$$
j _ {p} (t) = \hat {J} _ {p} e ^ {j \omega t} = - e D _ {p} \frac {\partial p _ {1} (x)}{\partial x} e ^ {j \omega t} \bigg | _ {x = 0} \tag {8.90}
$$

where $\hat { J } _ { p }$ is the current density phasor. Combining Equations (8.90), (8.84), and (8.85), we have 

$$
\hat {J} _ {p} = - e D _ {p} (- C _ {p}) \left[ p _ {\mathrm{dc}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \right] e ^ {- c _ {p} x} \Bigg | _ {x = 0} \tag {8.91}
$$

We can write the total ac hole current phasor as 

$$
\hat {I} _ {p} = A \hat {J} _ {p} = e A D _ {p} C _ {p} p _ {\mathrm{dc}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \tag {8.92}
$$

where A is the cross-sectional area of the pn junction. Substituting the expression for $C _ { p } ,$ we obtain 

$$
\hat {I} _ {p} = \frac {e A D _ {p} p _ {\mathrm{dc}}}{L _ {p}} \sqrt {1 + j \omega \tau_ {p 0}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \tag {8.93}
$$

If we defi ne 

$$
I _ {p 0} = \frac {e A D _ {p} p _ {d c}}{L _ {p}} = \frac {e A D _ {p} p _ {n 0}}{L _ {p}} \exp \left(\frac {e V _ {0}}{k T}\right) \tag {8.94}
$$

then Equation (8.93) becomes 

$$
\hat {I} _ {p} = I _ {p 0} \sqrt {1 + j \omega \tau_ {p 0}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \tag {8.95}
$$

Going through the same type of analysis for the minority carrier electrons in the p region, we obtain 

$$
\hat {I} _ {n} = I _ {n 0} \sqrt {1 + j \omega \tau_ {n 0}} \left(\frac {\hat {V} _ {1}}{V _ {t}}\right) \tag {8.96}
$$

where 

$$
I _ {n 0} = \frac {e A D _ {n} n _ {p 0}}{L _ {n}} \exp \left(\frac {e V _ {0}}{k T}\right) \tag {8.97}
$$

The total ac current phasor is the sum of $\hat { I } _ { p }$ and ${ \hat { I } } _ { n } .$ The pn junction admittance is the total ac current phasor divided by the ac voltage phasor, or 

$$
Y = \frac {\hat {I}}{\hat {V} _ {1}} = \frac {\hat {I} _ {p} + \hat {I} _ {n}}{\hat {V} _ {1}} = \left(\frac {1}{V _ {t}}\right) \left[ I _ {p 0} \sqrt {1 + j \omega \tau_ {p 0}} + I _ {n 0} \sqrt {1 + j \omega \tau_ {n 0}} \right] \tag {8.98}
$$

There is not a linear, lumped, fi nite, passive, bilateral network that can be synthesized to give this admittance function. However, we may make the following approximations. Assume that 

$$
\omega \tau_ {p 0} \ll 1 \tag {8.99a}
$$

and 

$$
\omega \tau_ {n 0} \ll 1 \tag {8.99b}
$$

These two assumptions imply that the frequency of the ac signal is not too large. Then we may write 

$$
\sqrt {1 + j \omega \tau_ {p 0}} \approx 1 + \frac {j \omega \tau_ {p 0}}{2} \tag {8.100a}
$$

and 

$$
\sqrt {1 + j \omega \tau_ {n 0}} \approx 1 + \frac {j \omega \tau_ {n 0}}{2} \tag {8.100b}
$$

Substituting Equations (8.100a) and (8.100b) into the admittance Equation (8.98), we obtain 

$$
Y = \left(\frac {1}{V _ {t}}\right) \left[ I _ {p 0} \left(1 + \frac {j \omega \tau_ {p 0}}{2}\right) + I _ {n 0} \left(1 + \frac {j \omega \tau_ {n 0}}{2}\right) \right] \tag {8.101}
$$

If we combine the real and imaginary portions, we get 

$$
Y = \left(\frac {1}{V _ {t}}\right) (I _ {p 0} + I _ {n 0}) + j \omega \left[ \left(\frac {1}{2 V _ {t}}\right) (I _ {p 0} \tau_ {p 0} + I _ {n 0} \tau_ {n 0}) \right] \tag {8.102}
$$

Equation (8.102) may be written in the form 

$$
Y = g _ {d} + j \omega C _ {d} \tag {8.103}
$$

The parameter $g _ { d }$ is called the diffusion conductance and is given by 

$$
g _ {d} = \left(\frac {1}{V _ {t}}\right) (I _ {p 0} + I _ {n 0}) = \frac {I _ {D Q}}{V _ {t}} \tag {8.104}
$$

where $I _ { D Q }$ is the dc bias current. Equation (8.104) is exactly the same conductance as we obtained previously in Equation (8.67). The parameter $C _ { d }$ is called the diffusion capacitance and is given by 

$$
C _ {d} = \left(\frac {1}{2 V _ {t}}\right) (I _ {p 0} \tau_ {p 0} + I _ {n 0} \tau_ {n 0}) \tag {8.105}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/9d9a40bb3a339f41c509425fc516d5dfb902863ca690525dda0e5fe0f624b45f.jpg)



Figure 8.21 | Minority carrier concentration changes with changing forward-bias voltage.


The physics of the diffusion capacitance may be seen in Figure 8.21. The dc values of the minority carrier concentrations are shown along with the changes due to the ac component of voltage. The $\Delta Q$ charge is alternately being charged and discharged through the junction as the voltage across the junction changes. The change in the stored minority carrier charge as a function of the change in voltage is the diffusion capacitance. One consequence of the approximations $\omega \tau _ { p 0 } \ll 1$ and $\omega \tau _ { n 0 } \ll 1$ is that there are no “wiggles” in the minority carrier curves. The sinusoidal frequency is low enough so that the exponential curves are maintained at all times. 

### EXAMPLE 8.7

Objective: Calculate the small-signal admittance parameters of a pn junction diode. 

This example is intended to give an indication of the magnitude of the diffusion capacitance as compared with the junction capacitance considered in the last chapter. The diffusion resistance will also be calculated. Assume that $N _ { a } \gg N _ { d }$ so that $p _ { n 0 } \gg n _ { p 0 } .$ . This assumption implies that $I _ { p 0 } \gg I _ { n 0 } .$ Let T  300 K, $\tau _ { p 0 } = 1 0 ^ { - 7 } \mathrm { s }$ , and $I _ { p 0 } = I _ { D Q } = 1 \mathrm { m A }$ . 

#### ■ Solution

The diffusion capacitance, with these assumptions, is given by 

$$
C _ {d} \approx \left(\frac {1}{2 V _ {t}}\right) (I _ {p 0} \tau_ {p 0}) = \frac {1}{(2) (0 . 0 2 5 9)} (1 0 ^ {- 3}) (1 0 ^ {- 7}) = 1. 9 3 \times 1 0 ^ {- 9} \mathrm{F}
$$

The diffusion resistance is 

$$
r _ {d} = \frac {V _ {t}}{I _ {D Q}} = \frac {0 . 0 2 5 9 \mathrm{V}}{1 \mathrm{mA}} = 2 5. 9 \Omega
$$

#### ■ Comment

The value of 1.93 nF for the diffusion capacitance of a forward-biased pn junction is three to four orders of magnitude larger than the junction capacitance of the reverse-biased pn junction, which we calculated in Example 7.5. 

#### ■ EXERCISE PROBLEM

Ex 8.7 A silicon pn junction diode at $T = 3 0 0 \mathrm { K }$ has the following parameters: $N _ { d } = 8 \times$ $1 0 ^ { 1 6 }$ cm $^ { - 3 } , N _ { a } = 2 \times 1 0 ^ { 1 5 }$ cm3, Dn  25 cm2 /s, $D _ { p } = 1 0$ cm2/s, $\tau _ { n 0 } = 5 \times 1 0 ^ { - 7 } \mathrm { s } .$ and $\tau _ { p 0 } = 1 0 ^ { - 7 } \mathrm { s }$ . The cross-sectional area is $A = 1 0 ^ { - 3 } \mathrm { c m } ^ { 2 } .$ . Determine the diffusion resistance and diffusion capacitance if the diode is forward biased at (a) $V _ { a } =$ 0.550 V and (b) $V _ { a } = 0 . 6 1 0 \mathrm { V } .$ 

$$
[ \text { Ans. } (a) r _ {d} = 1 1 8 \Omega , C _ {d} = 2. 0 7 \mathrm{nf}; (b) r _ {d} = 1 1. 6 \Omega , C _ {d} = 2 0. 9 \mathrm{nF} ]
$$

The diffusion capacitance tends to dominate the capacitance terms in a forwardbiased pn junction. The small-signal diffusion resistance can be fairly small if the diode current is a fairly large value. As the diode current decreases, the diffusion resistance increases. We will consider the impedance of forward-biased pn junctions again when we discuss bipolar transistors. 

## 8.3.3 Equivalent Circuit

The small-signal equivalent circuit of the forward-biased pn junction is derived from Equation (8.103). This circuit is shown in Figure 8.22a. We need to add the junction capacitance, which will be in parallel with the diffusion resistance and diffusion capacitance. The last element we add, to complete the equivalent circuit, is a series resistance. The neutral n and p regions have fi nite resistances so the actual pn junction will include a series resistance. The complete equivalent circuit is given in Figure 8.22b. 

The voltage across the actual junction is $V _ { a }$ and the total voltage applied to the pn diode is given by $V _ { \mathrm { a p p } } .$ . The junction voltage $V _ { a }$ is the voltage in the ideal current–voltage expression. We can write the expression 

$$
V _ {\mathrm{app}} = V _ {a} + I r _ {s} \tag {8.106}
$$

Figure 8.23 is a plot of the current–voltage characteristic from Equation (8.106) showing the effect of the series resistance. A larger applied voltage is required to achieve the same current value when a series resistance is included. In most diodes, the series resistance will be negligible. In some semiconductor devices with pn junctions, however, the series resistance will be in a feedback loop; in these cases, the resistance is multiplied by a gain factor and becomes non-negligible. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/abb1c484884c29679ef939774e99c9139d5cc3555b5848ada822f7a8b8677f92.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/3bf391b9b894727649fc5380f8d1f7c6b2298ef9811f38b985aca66a21489b5c.jpg)



Figure 8.22 | (a) Small-signal equivalent circuit of ideal forwardbiased pn junction diode; (b) complete small-signal equivalent circuit of pn junction.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/16b9b85da34837dc26352bf25f901ad18429e3dc047b79f636e0ff9807fce066.jpg)



Figure 8.23 | Forward-biased I–V characteristics of a pn junction diode showing the effect of series resistance.


## TEST YOUR UNDERSTANDING

TYU 8.5 A GaAs pn junction diode at $T = 3 0 0 \mathrm { K }$ has the same parameters given in Ex 8.7 except that $D _ { n } = 2 0 7$ cm2/s and $D _ { p } = 9 . 8 0 \mathrm { c m } ^ { 2 } / \mathrm { s }$ . Determine the diffusion resistance and diffusion capacitance if the diode is forward biased at (a) $V _ { a } = 0 . 9 7 0 \ : \mathrm { V }$ and (b) $V _ { a } = 1 . 0 4 5 \mathrm { V } .$ . 

$$
[ \text { Ans. } (a) r _ {d} = 2 6 3 \Omega , C _ {d} = 0. 9 4 0 \mathrm{nF}; (b) r _ {d} = 1 4. 6 \Omega , C _ {d} = 1 7. 0 \mathrm{nF} ]
$$

TYU 8.6 A silicon pn junction diode at $T = 3 0 0 \mathrm { K }$ has the same parameters as those described in Ex 8.7. The neutral n-region and neutral p-region lengths are 0.01 cm. Estimate the series resistance of the diode (neglect ohmic contacts). 

$$
(\text { Ans. } R = 6 6 \Omega)
$$

# *8.4 | CHARGE STORAGE AND DIODE TRANSIENTS

The pn junction is typically used as an electrical switch. In forward bias, referred to as the on state, a relatively large current can be produced by a small applied voltage; in reverse bias, referred to as the $o f f$ state, only a very small current will exist. Of primary interest in circuit applications is the speed of the pn junction diode in switching states. We qualitatively discuss the transients that occur and the charge storage effects. We simply state the equations that describe the switching times without any mathematical derivations. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/83306597297c21845f07f2e0505c8981b06e47254e1197be05b0dc5069ac9469.jpg)



Figure 8.24 | Simple circuit for switching a diode from forward to reverse bias.


## 8.4.1 The Turn-off Transient

Suppose we want to switch a diode from the forward bias on state to the reversebiased off state. Figure 8.24 shows a simple circuit that will switch the applied bias at $t = 0$ . For $t < 0$ , the forward-bias current is 

$$
I = I _ {F} = \frac {V _ {F} - V _ {a}}{R _ {F}} \tag {8.107}
$$

The minority carrier concentrations in the device, for the applied forward voltage $V _ { F } ,$ are shown in Figure 8.25a. There is excess minority carrier charge stored in both the p and n regions of the diode. The excess minority carrier concentrations at the space charge edges are supported by the forward-bias junction voltage $V _ { a } .$ . When the voltage is switched from the forward- to the reverse-biased state, the excess minority carrier concentrations at the space charge edges can no longer be supported and they start to decrease, as shown in Figure 8.25b. 

The collapse of the minority carrier concentrations at the edges of the space charge region leads to large concentration gradients and diffusion currents in the reverse-biased direction. If we assume, for the moment, that the voltage across the diode junction is small compared with $V _ { R } ,$ then the reverse-biased current is limited to approximately 

$$
I = - I _ {R} \approx \frac {- V _ {R}}{R _ {R}} \tag {8.108}
$$

The junction capacitances do not allow the junction voltage to change instantaneously. If the current $I _ { R }$ were larger than this value, there would be a forward-bias voltage across the junction, which would violate our assumption of a reverse-biased current. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/1feaa98431242209838034d4dba6160fe83068ac776dc6c611b20199f27a4c78.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/38872bb29f16ed7d7445c5ca741912335b2ab79e404d61b4c24cd851452a3951.jpg)



Figure 8.25 | (a) Steady-state forward-bias minority carrier concentrations; (b) minority carrier concentrations at various times during switching.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/226236a7016071bb35d84ff55091dacc771b5e17f2b9dc0e39dd133b11214e3c.jpg)



Figure 8.26 | Current characteristic versus time during diode switching.


If the current $I _ { R }$ were smaller than this value, there would be a reverse-biased voltage across the junction, which means that the junction voltage would have changed instantaneously. Since the reverse current is limited to the value given by Equation (8.108), the reverse-biased density gradient is constant; thus, the minority carrier concentrations at the space charge edge decrease with time as shown in Figure 8.25b. 

This reverse current $I _ { R }$ will be approximately constant for $0 ^ { + } \leq t \leq t _ { s } ,$ where $t _ { s }$ is called the storage time. The storage time is the length of time required for the minority carrier concentrations at the space charge edge to reach the thermal- equilibrium values. After this time, the voltage across the junction will begin to change. The current characteristic is shown in Figure 8.26. The reverse current is the fl ow of the stored minority carrier charge, which is the difference between the minority carrier concentrations at $t = 0 ^ { - }$ and $t = \infty ,$ , as shown in Figure 8.25b. 

The storage time ts can be determined by solving the time-dependent continuity equation. If we consider a one-sided $\mathfrak { p } ^ { + } \mathfrak { n }$ junction, the storage time is determined from the equation 

$$
\operatorname{erf} \sqrt {\frac {t _ {s}}{\tau_ {p 0}}} = \frac {I _ {F}}{I _ {F} + I _ {R}} \tag {8.109}
$$

where erf $( x )$ is known as the error function. An approximate solution for the storage time can be obtained as 

$$
t _ {s} \approx \tau_ {p 0} \ln \left(1 + \frac {I _ {F}}{I _ {R}}\right) \tag {8.110}
$$

The recovery phase for $t > t _ { s }$ is the time required for the junction to reach its steady-state reverse-biased condition. The remainder of the excess charge is being removed and the space charge width is increasing to the reverse-biased value. The decay time $t _ { 2 }$ is determined from 

$$
\operatorname{erf} \sqrt {\frac {t _ {2}}{\tau_ {p 0}}} + \frac {\exp (- t _ {2} / \tau_ {p 0})}{\sqrt {\pi t _ {2} / \tau_ {p 0}}} = 1 + 0. 1 \left(\frac {I _ {R}}{I _ {F}}\right) \tag {8.111}
$$

The total turn-off time is the sum of $t _ { s }$ and $t _ { 2 } .$ 

To switch the diode quickly, we need to be able to produce a large reverse current as well as have a small minority carrier lifetime. In the design of diode circuits, then, the designer must provide a path for the transient reverse-biased current pulse in order to be able to switch the diode quickly. These same effects will be considered when we discuss the switching of bipolar transistors. 

## 8.4.2 The Turn-on Transient

The turn-on transient occurs when the diode is switched from its $\mathit { \Omega } ^ { 6 6 } \mathrm { o f f } ^ { 9 }$ state into the forward-bias “on” state. The turn-on can be accomplished by applying a forwardbias current pulse. The fi rst stage of turn-on occurs very quickly and is the length of time required to narrow the space charge width from the reverse-biased value to its thermal-equilibrium value when $V _ { a } = 0$ . During this time, ionized donors and acceptors are neutralized as the space charge width narrows. 

The second stage of the turn-on process is the time required to establish the minority carrier distributions. During this time the voltage across the junction is increasing toward its steady-state value. A small turn-on time is achieved if the minority carrier lifetime is small and if the forward-bias current is small. 

## TEST YOUR UNDERSTANDING

TYU 8.7 A one-sided pn silicon diode, which has a forward-bias current of $I _ { F } = 1 . 7 5 \mathrm { m A }$ , is switched to reverse bias with an effective reverse-biased voltage of $V _ { R } = 2 \mathrm { V }$ and an effective series resistance of $R _ { R } = 4 { \mathrm { k } } \Omega$ . The minority carrier hole lifetime is $1 0 ^ { - 7 } \mathrm { \ : s } .$ (a) Determine the storage time ts. (b) Calculate the decay time $t _ { 2 } . \ ( c )$ What is the turn-off time of the diode? 

$$
[ \mathrm{s} _ {L} 0 \mathrm{I} \times 2 \approx (c); \mathrm{s} _ {L} 0 \mathrm{I} \times 1 0 ^ {- 7} \mathrm{s}; (\mathrm{b}) 1. 2 5 \times 1 0 ^ {- 7} \mathrm{s}; (\mathrm{c}) \approx 2 \times 1 0 ^ {- 7} \mathrm{s} ]
$$

# *8.5 | THE TUNNEL DIODE

The tunnel diode is a pn junction in which both the n and p regions are degenerately doped. As we discuss the operation of this device, we will fi nd a region that exhibits a negative differential resistance. The tunnel diode was used in oscillator circuits in the past, but other types of solid-state devices are now used as high-frequency oscillators; thus, the tunnel diode is really only of academic interest. Nevertheless, this device does demonstrate the phenomenon of tunneling we discussed in Chapter 2. 

Recall the degenerately doped semiconductors we discussed in Chapter 4: the Fermi level is in the conduction band of a degenerately doped n-type material and in the valence band of a degenerately doped p-type material. Then, even at T  0 K, electrons will exist in the conduction band of the n-type material, and holes (empty states) will exist in the p-type material. 

Figure 8.27 shows the energy-band diagram of a pn junction in thermal equilibrium for the case when both the n and p regions are degenerately doped. The depletion region width decreases as the doping increases and may be on the order of approximately 100 Å for the case shown in Figure 8.27. The potential barrier at the junction can be approximated by a triangular potential barrier, as shown in Fig ure 8.28. This potential barrier is similar to the potential barrier used in Chapter 2 to illustrate the tunneling phenomenon. The barrier width is small and the electric fi eld in the space charge region is quite large; thus, a fi nite probability exists that an electron may tunnel through the forbidden band from one side of the junction to the other. 

We may qualitatively determine the current–voltage characteristics of the tunnel diode by considering the simplifi ed energy-band diagrams in Figure 8.29. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/ed0cc70f38294c447e7c1ba5f2bb93e55760e6e19771d2e85569c94ae7fd266e.jpg)



Figure 8.27 | Energy-band diagram of a pn junction in thermal equilibrium in which both the n and p regions are degenerately doped.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/a8cbcc800bcd3abdb8bd106b31ef9cff3809ce9aa1aa88bb63260d8af30a9f69.jpg)



Figure 8.28 | Triangular potential barrier approximation of the potential barrier in the tunnel diode.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/27d411b2d4e55e1ae3b0ba0ea1e1f7661a13e4413cae9fa0bd9ac1476e7c618d.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/158ada4d36e7390d86c36c1dc39ff773b19e8fdc1e75aab9f0a0baeaf7a1dd4e.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/3a0dfe13f3f1c7fe45490d2d9d70fdc7b5b4b56bd8c0b57897f2b95815977c8a.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/117a6dd9dd5f0446b286b71ca63edb908f51dcef35a97ce4327cb9c08567502a.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/7a0b1e55c9d904d932bce81eeaca0158156ad6d2a1b739abaab61208bb483103.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/ffc3efea208ccfe9d926e1391afdd5a6879a6b42fe5e1d8ca54a9f117e8a5d14.jpg)



(c)



Figure 8.29 | Simplifi ed energy-band diagrams and I–V characteristics of the tunnel diode at (a) zero bias; (b) a slight forward bias; (c) a forward bias producing maximum tunneling current. (continued)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/964ae1d7f216c9b0e94c4db22023219334b09d19271047981666453f7a6bf601.jpg)



Figure 8.29 | (concluded) (d) A higher forward bias showing less tunneling current; (e) a forward bias for which the diffusion current dominates.


Figure 8.29a shows the energy-band diagram at zero bias, which produces zero current on the I–V diagram. If we assume, for simplicity, that we are near 0 K, then all energy states are fi lled below $E _ { F }$ on both sides of the junction. 

Figure 8.29b shows the situation when a small forward-bias voltage is applied to the junction. Electrons in the conduction band of the n region are directly opposite to empty states in the valence band of the p region. There is a fi nite probability that some of these electrons will tunnel directly into the empty states, producing a forward-bias tunneling current as shown. With a slightly larger forward-bias voltage, as in Figure 8.29c, the maximum number of electrons in the n region will be opposite the maximum number of empty states in the p region; this will produce a maximum tunneling current. 

As the forward-bias voltage continues to increase, the number of electrons on the n side directly opposite empty states on the p side decreases, as in Figure 8.29d, and the tunneling current will decrease. In Figure 8.29e, there are no electrons on the n side directly opposite to available empty states on the p side. For this forward-bias voltage, the tunneling current will be zero and the normal ideal diffusion current will exist in the device as shown in the I–V characteristics. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/a7152828db5c4ef2c4b9c22226e6f4302613109a5f09108605bc86563978db7a.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-29/db9d541f-6b69-4e19-b518-0ad021f4c68e/5edc33d15019e01aa3bf1a58b157b9a5848a0fc30abc6b3dac19348348413f55.jpg)



(b)



Figure 8.30 | (a) Simplifi ed energy-band diagram of a tunnel diode with a reversebiased voltage; (b) I–V characteristic of a tunnel diode with a reverse-biased voltage.


The portion of the curve showing a decrease in current with an increase in voltage is the region of differential negative resistance. The range of voltage and current for this region is quite small; thus, any power generated from an oscillator using this negative resistance property would also be fairly small. 

A simplifi ed energy-band diagram of the tunnel diode with an applied reversebiased voltage is shown in Figure 8.30a. Electrons in the valence band on the p side are directly opposite empty states in the conduction band on the n side, so electrons can now tunnel directly from the p region into the n region, resulting in a large reverse-biased tunneling current. This tunneling current will exist for any reversebiased voltage. The reverse-biased current will increase monotonically and rapidly with reverse-biased voltage as shown in Figure 8.30b. 

# 8.6 | SUMMARY

■ When a forward-bias voltage is applied across a pn junction (p region positive with respect to the n region), the potential barrier is lowered so that holes from the p region and electrons from the n region can fl ow across the junction. 

■ The boundary conditions relating the minority carrier hole concentration in the n region at the space charge edge and the minority carrier electron concentration in the p region at the space charge edge were derived. 

■ The holes that are injected into the n region and the electrons that are injected into the p region now become excess minority carriers. The behavior of the excess minority carrier is described by the ambipolar transport equation developed and described in Chapter 6. Solving the ambipolar transport equation and using the boundary conditions, the steady-state minority carrier hole and electron concentrations in the n region and p region, respectively, were derived. 

■ Gradients exist in the minority carrier hole and electron concentrations so that minority carrier diffusion currents exist in the pn junction. These diffusion currents yield the ideal current–voltage relationship of the pn junction diode. 

■ Excess carriers are generated in the space charge region of a reverse-biased pn junction. These carriers are swept out by the electric fi eld and create the reverse-biased generation current that is another component of the reverse-biased diode current. Excess carriers recombine in the space charge region of a forward-biased pn junction. This recombination process creates the forward-bias recombination current that is another component of the forward-bias diode current. 

■ The small-signal equivalent circuit of the pn junction diode was developed. The two parameters of interest are the diffusion resistance and the diffusion capacitance. 

■ When a pn junction is switched from forward bias to reverse bias, the stored excess minority carrier charge must be removed from the junction. The time required to remove this charge is called the storage time and is a limiting factor in the switching speed of a diode. 

■ The I–V characteristics of a tunnel diode were developed showing a region of negative differential resistance. 

# GLOSSARY OF IMPORTANT TERMS

carrier injection The fl ow of carriers across the space charge region of a pn junction when a voltage is applied. 

diffusion capacitance The capacitance of a forward-biased pn junction due to minority carrier storage effects. 

diffusion conductance The ratio of a low-frequency, small-signal sinusoidal current to voltage in a forward-biased pn junction. 

diffusion resistance The inverse of diffusion conductance. 

forward bias The condition in which a positive voltage is applied to the p region with respect to the n region of a pn junction so that the potential barrier between the two regions is lowered below the thermal-equilibrium value. 

generation current The reverse-biased pn junction current produced by the thermal generation of electron–hole pairs within the space charge region. 

high-level injection The condition in which the excess carrier concentration becomes comparable to or greater than the majority carrier concentration. 

“long” diode A pn junction diode in which both the neutral p and n regions are long compared with the respective minority carrier diffusion lengths. 

recombination current The forward-bias pn junction current produced as a result of the fl ow of electrons and holes that recombine within the space charge region. 

reverse saturation current The ideal reverse-biased current in a pn junction. 

“short” diode A pn junction diode in which at least one of the neutral p or n regions is short compared to the respective minority carrier diffusion length. 

storage time The time required for the excess minority carrier concentrations at the space charge edge to go from their steady-state values to zero when the diode is switched from forward to reverse bias. 

# CHECKPOINT

After studying this chapter, the reader should have the ability to: 

■ Describe the mechanism of charge fl ow across the space charge region of a pn junction when a forward-bias voltage is applied. 

■ State the boundary conditions for the minority carrier concentrations at the edge of the space charge region. 

■ Derive the expressions for the steady-state minority carrier concentrations in the pn junction. 

■ Derive the ideal current–voltage relationship for a pn junction diode. 

■ Describe the characteristics of a “short” diode. 

■ Describe generation and recombination currents in a pn junction. 

■ Defi ne high-level injection and describe its effect on the diode I–V characteristics. 

■ Describe what is meant by diffusion resistance and diffusion capacitance. 

■ Describe the turn-off transient response in a pn junction. 

# REVIEW QUESTIONS

1. Sketch the energy bands in a zero-biased, reverse-biased, and forward-biased pn junction. 

2. Write the boundary conditions for the excess minority carriers in a pn junction (a) under forward bias and (b) under reverse bias. 

3. Sketch the steady-state minority carrier concentrations in a forward-biased pn junction. 

4. Explain the procedure that is used in deriving the ideal current–voltage relationship in a pn junction diode. 

5. Sketch the electron and hole currents through a forward-biased pn junction diode. Are currents near the junction primarily due to drift or diffusion? What about currents far from the junction? 

6. What is the temperature dependence of the ideal reverse-saturation current? 

7. What is meant by a “short” diode? 

8. Explain the physical mechanism of the (a) generation current and (b) recombination current. 

9. Sketch the forward-bias I–V characteristics of a pn junction diode showing the effects of recombination and high-level injection. 

10. (a) Explain the physical mechanism of diffusion capacitance. (b) What is diffusion resistance? 

11. If a forward-biased pn junction is switched off, explain what happens to the stored minority carriers. In which direction is the current immediately after the diode is switched off? 

