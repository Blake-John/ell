# Fundamentals of the Metal–Oxide–Semiconductor Field-Effect Transistor

T he single-junction semiconductor devices that we have considered, including the pn homojunction diode, can be used to produce rectifying current– voltage characteristics and to form electronic switching circuits. The transistor is a the pn homojunction diode, can be used to produce rectifying current-voltage characteristics and to form electronic switching circuits. The transistor is a multijunction semiconductor device that, in conjunction with other circuit elements, is capable of current gain, voltage gain, and signal power gain. The basic transistor action is the control of current at one terminal by the voltage applied across the other two terminals of the device. 

The Metal–Oxide–Semiconductor Field-Effect Transistor (MOSFET) is one of two major types of transistors. The fundamental physics of the MOSFET is developed in this chapter. The MOSFET is used extensively in digital circuit applications where, because of its small size, millions of devices can be fabricated in a single integrated circuit. 

Two complementary confi gurations of MOS transistors, the n-channel MOSFET and the p-channel MOSFET, can be fabricated. Electronic circuit design becomes very versatile when the two types of devices are used in the same circuit. These circuits are referred to as complementary MOS (CMOS) circuits. ■ 

## 10.0 | PREVIEW

In this chapter, we will: 

■ Study the characteristics of energy bands as a function of applied voltage in the metal–oxide–semiconductor structure known as the MOS capacitor. The MOS capacitor is the heart of the MOSFET. 

■ Discuss the concept of surface inversion in the semiconductor of the MOS capacitor. 

Defi ne and derive the expression for the threshold voltage, which is a basic parameter of the MOSFET. 

■ Discuss various physical structures of MOSFETs, including enhancement and depletion mode devices. 

■ Derive the ideal current–voltage relationship of the MOSFET. 

■ Develop the small-signal equivalent circuit of the MOSFET. This circuit is used to relate small-signal currents and voltages in analog circuits. 

■ Derive the frequency limiting factors of the MOSFET. 

## 10.1 | THE TWO-TERMINAL MOS STRUCTURE

The heart of the MOSFET is the MOS capacitor shown in Figure 10.1. The metal may be aluminum or some other type of metal, although in many cases, it is actually a high-conductivity polycrystalline silicon that has been deposited on the oxide; however, the term metal is usually still used. The parameter $t _ { \mathrm { o x } }$ in the fi gure is the thickness of the oxide and $\epsilon _ { \mathrm { o x } }$ is the permittivity of the oxide. 

## 10.1.1 Energy-Band Diagrams

The physics of the MOS structure can be more easily explained with the aid of the simple parallel-plate capacitor. Figure 10.2a shows a parallel-plate capacitor with the top plate at a negative voltage with respect to the bottom plate. An insulator material separates the two plates. With this bias, a negative charge exists on the top plate, a positive charge exists on the bottom plate, and an electric fi eld is induced between the two plates as shown. The capacitance per unit area for this geometry is 

$$
C ^ {\prime} = \frac {\epsilon}{d} \tag {10.1}
$$

where - is the permittivity of the insulator and d is the distance between the two plates. The magnitude of the charge per unit area on either plate is 

$$
Q ^ {\prime} = C ^ {\prime} V \tag {10.2}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/dfe1c391f510d3b8824f4e1188403d6094c7d4eb743cad1c506c94e0a668d70a.jpg)



Figure 10.1 | The basic MOS capacitor structure.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/0e23274bc55614020b612ee68968bd131e29e7ce7c43ef117b40e9bcc1ece577.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/1e70528ae99f74ede7da63af63327e487ec1f6092b993c7f42dfded44afebaa5.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/fbf1d7a97d53448c5f54285d664aef3fe3c6f1a937912b4e1dd08d6a34c2a2df.jpg)



Figure 10.2 | (a) A parallel-plate capacitor showing the electric fi eld and conductor charges. (b) A corresponding MOS capacitor with a negative gate bias showing the electric fi eld and charge fl ow. (c) The MOS capacitor with an accumulation layer of holes.


where the prime indicates charge or capacitance per unit area. The magnitude of the electric fi eld is 

$$
\mathrm{E} = \frac {V}{d} \tag {10.3}
$$

Figure 10.2b shows a MOS capacitor with a p-type semiconductor substrate. The top metal gate is at a negative voltage with respect to the semiconductor substrate. From the example of the parallel-plate capacitor, we can see that a negative charge will exist on the top metal plate and an electric fi eld will be induced with the direction shown in the fi gure. If the electric fi eld were to penetrate into the semiconductor, the majority carrier holes would experience a force toward the oxide– semiconductor interface. Figure 10.2c shows the equilibrium distribution of charge in the MOS capacitor with this particular applied voltage. An accumulation layer of holes at the oxide–semiconductor junction corresponds to the positive charge on the bottom “plate” of the MOS capacitor. 

Figure 10.3a shows the same MOS capacitor in which the polarity of the applied voltage is reversed. A positive charge now exists on the top metal plate and the induced electric fi eld is in the opposite direction as shown. If the electric fi eld penetrates the semiconductor in this case, majority carrier holes will experience a force away from the oxide–semiconductor interface. As the holes are pushed away from the interface, a negative space charge region is created because of the fi xed ionized acceptor atoms. The negative charge in the induced depletion region corresponds to the negative charge on the bottom “plate” of the MOS capacitor. Figure 10.3b shows the equilibrium distribution of charge in the MOS capacitor with this applied voltage. 

The energy-band diagrams of the MOS capacitor with a p-type substrate for various gate biases are shown in Figure 10.4. Figure 10.4a shows the ideal case when zero bias is applied across the MOS device. The energy bands in the semiconductor are fl at indicating no net charge exists in the semiconductor. This condition is known as fl at band and is discussed in more detail later in the chapter. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/85c07e874283fdf467d544082e8a0e0495f6904f2acc760a7b39bef95d14a28c.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/30b71e3f3c6b673bb65553af0f6641eeb09990cac65ceef9bfd18c064a656c06.jpg)



(b)



Figure 10.3 | The MOS capacitor with a moderate positive gate bias, showing (a) the electric fi eld and charge fl ow and (b) the induced space charge region.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/14b590c78fa0cd942b25ad1eddc4b4fb374a3da5aa93f5bb4b676eeb6c13ccf0.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/fe6ccd2c12c5dc2d3f481d0c7f6ce0fa49adc7b8e00d267040c2e833d78d752e.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/9353f184504b5746d7e1e0a8bec46609d671f5f7c2c87b3bb73548b5ca791e57.jpg)



(c)



Figure 10.4 | The energy-band diagram of a MOS capacitor with a p-type substrate for (a) a zero applied gate bias showing the ideal case, (b) a negative gate bias, and (c) a moderate positive gate bias.


Figure 10.4b shows the energy-band diagram for the case when a negative bias is applied to the gate. (Remember that positive electron energy is plotted “upward” and positive voltage is plotted “downward.”) The valence-band edge is closer to the Fermi level at the oxide–semiconductor interface than in the bulk material, which implies that there is an accumulation of holes. The semiconductor surface appears to be more p-type than the bulk material. The Fermi level is a constant in the semiconductor since the MOS system is in thermal equilibrium and there is no current through the oxide. 

Figure 10.4c shows the energy-band diagram of the MOS system when a positive voltage is applied to the gate. The conduction- and valence-band edges bend as shown in the fi gure, indicating a space charge region similar to that in a pn junction. The conduction band and intrinsic Fermi levels move closer to the Fermi level. The induced space charge width is $x _ { d } .$ 

Now consider the case when a still larger positive voltage is applied to the top metal gate of the MOS capacitor. We expect the induced electric fi eld to increase in magnitude and the corresponding positive and negative charges on the MOS capacitor to increase. A larger negative charge in the MOS capacitor implies a larger induced space charge region and more band bending. Figure 10.5 shows such a condition. The intrinsic Fermi level at the surface is now below the Fermi level. The conduction band at the surface is now close to the Fermi level, whereas the valence band is close to the Fermi level in the bulk semiconductor. This result implies that the surface in the semiconductor adjacent to the oxide–semiconductor interface is n type. By applying a suffi ciently large positive gate voltage, we have inverted the surface of the semiconductor from a p-type to an n-type semiconductor. We have created an inversion layer of electrons at the oxide–semiconductor interface. 

In the MOS capacitor structure that we have just considered, we assumed a p-type semiconductor substrate. The same type of energy-band diagrams can be constructed for a MOS capacitor with an n-type semiconductor substrate. Figure 10.6a shows the MOS capacitor structure with a positive voltage applied to the top gate terminal. A positive charge exists on the top gate and an electric fi eld is induced with the direction shown in the fi gure. An accumulation layer of electrons will be induced in the n-type substrate. The case when a negative voltage is applied to the top gate is shown in Figure 10.6b. A positive space charge region is induced in the n-type semiconductor in this situation. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b79885487b33d37bd1c8b08f065910739d8bd1d49b9669e171c60d7b5dd9a898.jpg)



Figure 10.5 | The energy-band diagram of the MOS capacitor with a p-type substrate for a “large” positive gate bias.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e2625d1e4dcf371ea0978c1aa3e650d4b3fcdf27eebb97c24d4036908de35b40.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/5a600394dd1418768fccf06cf1b592175f9e3974f358e6f0d29de932649e75e6.jpg)



(b)



Figure 10.6 | The MOS capacitor with an n-type substrate for (a) a positive gate bias and (b) a moderate negative gate bias.


The energy-band diagrams for this MOS capacitor with the n-type substrate are shown in Figure 10.7. Figure 10.7a shows the case when a positive voltage is applied to the gate and an accumulation layer of electrons is formed. Figure 10.7b shows the energy bands when a negative voltage is applied to the gate. The conduction and valence bands now bend upward indicating that a space charge region has been induced in the n-type substrate. Figure 10.7c shows the energy bands when a larger negative voltage is applied to the gate. The conduction and valence bands are bent even more and the intrinsic Fermi level has moved above the Fermi level. The valence band at the surface is now close to the Fermi level, whereas the conduction band is close to the Fermi level in the bulk semiconductor. This result implies that the semiconductor surface adjacent to the oxide–semiconductor interface is p type. By applying a suffi ciently large negative voltage to the gate of the MOS capacitor, the semiconductor surface has been inverted from n type to p type. An inversion layer of holes has been induced at the oxide–semiconductor interface. 

## 10.1.2 Depletion Layer Thickness

We may calculate the width of the induced space charge region adjacent to the oxide– semiconductor interface. Figure 10.8 shows the space charge region in a ptype semi conductor substrate. The potential $\phi _ { f p }$ is the difference (in V) between $E _ { F i }$ and $E _ { F }$ and is given by 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {i}}\right) \tag {10.4}
$$

where $N _ { a }$ is the acceptor doping concentration and $n _ { i }$ is the intrinsic carrier concentration. 

The potential $\phi _ { s }$ is called the surface potential; it is the difference (in V) between $E _ { F i }$ measured in the bulk semiconductor and $E _ { F i }$ i measured at the surface. The surface potential is the potential difference across the space charge layer. The space charge width can now be written in a form similar to that of a one-sided pn junction. We can write that 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d926039138500d2e8ffb1a11e2534a6885d8934f9692307b9bcac0fed8cf8f17.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/fa2fbe37726180b031f09b78a4b9368534023dd5ac24e35624ce4a1162a8deb6.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/4c27fcfb791a6d051f145d223aa6a084f6e7a4a9d35a9f06d7dae38a87a46377.jpg)



Figure 10.7 | The energy-band diagram of the MOS capacitor with an n-type substrate for (a) a positive gate bias, (b) a moderate negative bias, and (c) a “large” negative gate bias.


$$
x _ {d} = \left(\frac {2 \epsilon_ {s} \phi_ {s}}{e N _ {a}}\right) ^ {1 / 2} \tag {10.5}
$$

where $\epsilon _ { s }$ is the permittivity of the semiconductor. Equation (10.5) assumes that the abrupt depletion approximation is valid. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/f33dee875af462617955f27713287b3aa3245bacd5af7bee4085d73332a1ce9f.jpg)



Figure 10.8 | The energy-band diagram in the p-type semiconductor, indicating surface potential.


Figure 10.9 shows the energy bands for the case in which $\phi _ { s } = 2 \phi _ { f p }$ . The Fermi level at the surface is as far above the intrinsic level as the Fermi level is below the intrinsic level in the bulk semiconductor. The electron concentration at the surface is the same as the hole concentration in the bulk material. This condition is known as the threshold inversion point. The applied gate voltage creating this condition is known as the threshold voltage. If the gate voltage increases above this threshold value, the conduction band will bend slightly closer to the Fermi level, but the change in the conduction band at the surface is now only a slight function of gate voltage. The electron concentration at the surface, however, is an exponential function of the surface potential. The surface potential may increase by a few $( k T / e )$ volts, which will change the electron concentration by orders of magnitude, but the space charge width changes only slightly. In this case, then, the space charge region has essentially reached a maximum width. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e8f6f086e77bf7d401808a2c9158fe51f9958436959e5670361e7fb59dd5142e.jpg)



Figure 10.9 | The energy-band diagram in the p-type semiconductor at the threshold inversion point.


The maximum space charge width, $x _ { d T } ,$ at this inversion transition point can be calculated from Equation (10.5) by setting $\phi _ { s } = 2 \phi _ { f p }$ . Then 

$$
x _ {d T} = \left(\frac {4 \epsilon_ {s} \phi_ {f p}}{e N _ {a}}\right) ^ {1 / 2} \tag {10.6}
$$

Objective: Calculate the maximum space charge width for a given semiconductor doping concentration. 

Consider silicon at $T = 3 0 0 \mathrm { K }$ doped to $N _ { a } = 1 0 ^ { 1 6 } \thinspace \mathrm { c m } ^ { - 3 }$ . The intrinsic carrier concentration is $n _ { i } = 1 . 5 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 3 }$ . 

## Solution

From Equation (10.4), we have 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {i}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0 ^ {1 6}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 3 4 7 3 \mathrm{V}
$$

Then the maximum space charge width is 

$$
x _ {d T} = \left[ \frac {4 \epsilon_ {s} \phi_ {f p}}{e N _ {a}} \right] ^ {1 / 2} = \left[ \frac {4 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 3 4 7 3)}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 6})} \right] ^ {1 / 2}
$$

or 

$$
x _ {d T} \cong 0. 3 0 \times 1 0 ^ {- 4} \mathrm{cm} = 0. 3 0 \mu \mathrm{m}
$$

## ■ Comment

The maximum induced space charge width is on the same order of magnitude as pn junction space charge widths. 

## ■ EXERCISE PROBLEM

Ex 10.1 Consider an oxide-to-p-type silicon junction at $T = 3 0 0 \mathrm { K }$ . The impurity doping concentration in the silicon is $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Calculate the maximum space charge width. Does the space charge width increase or decrease as the p-type doping concentration decreases? 

$$
(A n s. x _ {d t} = 0. 6 2 9 \mu m, i n c r e a s e)
$$

We have been considering a p-type semiconductor substrate. The same maximum induced space charge region width occurs in an n-type substrate. Figure 10.10 is the energy-band diagram at the threshold voltage with an n-type substrate. We can write 

$$
\phi_ {f n} = V _ {t} \ln \left(\frac {N _ {d}}{n _ {i}}\right) \tag {10.7}
$$

and 

$$
x _ {d T} = \left(\frac {4 \epsilon_ {s} \phi_ {f n}}{e N _ {d}}\right) ^ {1 / 2} \tag {10.8}
$$

Note that we are always assuming the parameters $\phi _ { f p }$ and $\phi _ { f n }$ to be positive quantities. 

Figure 10.11 is a plot of $x _ { d T }$ at $T = 3 0 0 \mathrm { K }$ as a function of doping concentration in silicon. The semiconductor doping can be either n type or p type. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/691a37e72e0bd00d87da7b3b9b62a4a0e3eb4ae101f87526cb13b0251892519f.jpg)



Figure 10.10 | The energy-band diagram in the n-type semiconductor at the threshold inversion point.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/0e9a3dcb1ff519c113872183f2a76c8ca0058b58766c8d03d4c384c0efdcd379.jpg)



Figure 10.11 | Maximum induced space charge region width versus semiconductor doping.


## 10.1.3 Surface Charge Density

From the results of Chapter 4, the electron concentration in the conduction band can be written in the form 

$$
n = n _ {i} \exp \left[ \frac {E _ {F} - E _ {F i}}{k T} \right] \tag {10.9}
$$

For a p-type semiconductor substrate, the electron inversion charge density can then be written as (see Figure 10.9) 

$$
n _ {s} = n _ {i} \exp \left[ \frac {e (\phi_ {f p} + \Delta \phi_ {s})}{k T} \right] = n _ {i} \exp \left[ \frac {\phi_ {f p} + \Delta \phi_ {s}}{V _ {t}} \right] \tag {10.10a}
$$

or 

$$
n _ {s} = n _ {i} \exp \left(\frac {\phi_ {f p}}{V _ {t}}\right) \cdot \exp \left(\frac {\Delta \phi_ {s}}{V _ {t}}\right) \tag {10.10b}
$$

where $\Delta \phi _ { s } ,$ , is the surface potential greater than $2 \phi _ { f p }$ 

We may note that 

$$
n _ {s t} = n _ {i} \exp \left(\frac {\phi_ {f p}}{V _ {t}}\right) \tag {10.11}
$$

where $n _ { s t }$ is the surface charge density at the threshold inversion point. The electron inversion charge density can then be written as 

$$
n _ {s} = n _ {s t} \exp \left(\frac {\Delta \phi_ {s}}{V _ {t}}\right) \tag {10.12}
$$

Figure 10.12 shows the electron inversion charge density as a function of surface potential for the case when the threshold inversion charge density is $n _ { s t } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . We may note that the inversion charge density increases by a factor of 10 with a 60-mV increase in surface potential. As discussed previously, the electron inversion charge density increases rapidly with small increases in surface potential, which means that the space charge width essentially reaches a maximum value. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/c3d2b1afab69d3c38a3c6071c0b7b4b3a19efdf987d267f4b32786e19def5673.jpg)



Figure 10.12 | Electron inversion charge density as a function of surface potential.


## 10.1.4 Work Function Differences

We have been concerned, so far, with the energy-band diagrams of the semiconductor material. Figure 10.13a shows the energy levels in the metal, silicon dioxide $\left( \mathrm { S i O } _ { 2 } \right)$ , and silicon relative to the vacuum level. The metal work function is $\phi _ { m }$ and the electron affi nity is $\chi .$ . The parameter $\chi _ { i }$ is the oxide electron affi nity and, for $\mathrm { S i O } _ { 2 } ,$ $\chi _ { i } = 0 . 9 \ : \mathrm { V }$ . 

Figure 10.13b shows the energy-band diagram of the entire MOS structure with zero gate voltage applied. The Fermi level is a constant through the entire system at thermal equilibrium. We may defi ne $\phi _ { m } ^ { \prime }$ as a modifi ed metal work function—the potential required to inject an electron from the metal into the conduction band of the oxide. Similarly, $\chi ^ { \prime }$ is defi ned as a modifi ed electron affi nity. The voltage $V _ { \mathrm { o x 0 } }$ is the potential drop across the oxide for zero applied gate voltage and is not necessarily zero because of the difference between $\phi _ { m }$ and $\chi .$ The potential $\phi _ { s 0 }$ is the surface potential for this case. 

If we sum the energies from the Fermi level on the metal side to the Fermi level on the semiconductor side, we have 

$$
e \phi_ {m} ^ {\prime} + e V _ {\mathrm{ox0}} = e \chi^ {\prime} + \frac {E _ {g}}{2} - e \phi_ {s 0} + e \phi_ {J f p} \tag {10.13}
$$

Equation (10.13) can be rewritten as 

$$
V _ {\mathrm{ox0}} + \phi_ {s 0} = - \left[ \phi_ {m} ^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} + \phi_ {f p}\right) \right] \tag {10.14}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e0e0bd4cee1560d7896d3f071797fb103db4818036848c84b9eb5cb31b4216ed.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ad0cfda0f6f819cde1ae020b21dda458396328c8ecf16c099baad201cbe98e08.jpg)



(b)



Figure 10.13 | (a) Energy levels in a MOS system prior to contact and (b) energy-band diagram through the MOS structure in thermal equilibrium after contact.


We can defi ne a potential $\phi _ { m s }$ as 

$$
\phi_ {m s} \equiv \left[ \phi_ {m} ^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} + \phi_ {f p}\right) \right] \tag {10.15}
$$

which is known as the metal–semiconductor work function difference. 

Objective: Determine the metal–semiconductor work function difference, $\phi _ { m s } ,$ for a given MOS system and semiconductor doping. 

For an aluminum–silicon dioxide junction, $\phi _ { m } ^ { \prime } = 3 . 2 0 \mathrm { V }$ and, for a silicon–silicon dioxide junction, $\chi ^ { \prime } = 3 . 2 5 \ : \mathrm { V } .$ . We may assume that $E _ { g } = 1 . 1 2 \ : \mathrm { V }$ . Let the p-type doping be $N _ { a } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

EXAMPLE 10.2 

## Solution

For silicon at $T = 3 0 0 \mathrm { K } ,$ we may calculate $\phi _ { f p }$ as 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {j}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0 ^ {1 5}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 2 8 8 \mathrm{V}
$$

Then the metal–semiconductor work function difference is 

$$
\phi_ {m s} = \phi_ {m} ^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} + \phi_ {f p}\right) = 3. 2 0 - (3. 2 5 + 0. 5 6 0 + 0. 2 8 8)
$$

or 

$$
\phi_ {m s} = - 0. 8 9 8 \mathrm{V}
$$

## ■ Comment

The value of $\phi _ { m s }$ s will become more negative as the doping of the p-type substrate increases. 

## ■ EXERCISE PROBLEM

Ex 10.2 Repeat Example 10.2 for a semiconductor doping of $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . 

$$
(\text { Ans. } \phi_ {m s} = - 0. 9 5 7 \text { V })
$$

Degenerately doped polysilicon deposited on the oxide is also often used as the metal gate. Figure 10.14a shows the energy-band diagram of a MOS capacitor with an $\mathrm { n ^ { + } }$ polysilicon gate and a p-type substrate. Figure 10.14b shows the energy-band diagram for the case of a $\mathfrak { p } ^ { + }$ polysilicon gate and the p-type silicon substrate. In the degenerately doped polysilicon, we will initially assume that $E _ { F } = E _ { c }$ for the $\mathrm { n ^ { + } }$ case and $E _ { F } = E _ { v }$ for the $\mathfrak { p } ^ { + }$ case. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b6b33686f1401269a9aa81ca0feaeb541476f8bc6fe798d8d6f8d1f078866f85.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/7c676214fa9a0bf8486218a912c793a35633a12dda4dcbc622fdf3c40f6bdc88.jpg)



(b)



Figure 10.14 | Energy-band diagram through the MOS structure with a p-type substrate at zero gate bias for (a) an $\mathrm { n ^ { + } }$ polysilicon gate and (b) $\mathtt { a p } ^ { + }$ polysilicon gate.


For the $\mathrm { n ^ { + } }$ polysilicon gate, the metal–semiconductor work function difference can be written as 

$$
\phi_ {m s} = \left[ \chi^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} + \phi_ {f p}\right) \right] = - \left(\frac {E _ {g}}{2 e} + \phi_ {f p}\right) \tag {10.16}
$$

and for the $\mathfrak { p } ^ { + }$ polysilicon gate, we have 

$$
\phi_ {m s} = \left[ \left(\chi^ {\prime} + \frac {E _ {g}}{e}\right) - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} + \phi_ {f p}\right) \right] = \left(\frac {E _ {g}}{2 e} - \phi_ {f p}\right) \tag {10.17}
$$

However, for degenerately doped $\mathrm { n ^ { + } }$ polysilicon and $\mathrm { p } ^ { + }$ polysilicon, the Fermi level can be above $E _ { c }$ and below $E _ { v } ,$ respectively, by 0.1 to 0.2 V. The experimental $\phi _ { m s }$ values will then be slightly different from the values calculated by using Equations (10.16) and (10.17). 

We have been considering a p-type semiconductor substrate. We may also have an n-type semiconductor substrate in a MOS capacitor. Figure 10.15 shows the energy-band diagram of the MOS capacitor with a metal gate and the n-type semiconductor substrate, for the case when a negative voltage is applied to the gate. The metal–semiconductor work function difference for this case is defi ned as 

$$
\phi_ {m s} = \phi_ {m} ^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} - \phi_ {f n}\right) \tag {10.18}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/f251273dc4f85b36bab3c58d3b51ebb0123f2675ac65cd25c843de1589f81210.jpg)



Figure 10.15 | Energy-band diagram through the MOS structure with an n-type substrate for a negative applied gate bias.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e3c75c77b66d5bbd8dd9bf5fbfe516ab8d127839354b0ac7d72c9ec6ca16b14b.jpg)



Figure 10.16 | Metal–semiconductor work function difference versus doping for aluminum, gold, and n and p polysilicon gates.



(From Sze [17] and Werner [20].)


where $\phi _ { f n }$ is assumed to be a positive value. We will have similar expressions for $\mathrm { n ^ { + } }$ and $\mathfrak { p } ^ { + }$ polysilicon gates. 

Figure 10.16 shows the work function differences as a function of semiconductor doping for the various types of gates. We may note that the magnitudes of $\phi _ { m s }$ for the polysilicon gates are somewhat larger than Equations (10.16) and (10.17) predict. This difference again is because the Fermi level is not equal to the conduction-band energy for the $\mathrm { n ^ { + } }$ gate and is not equal to the valence-band energy for the $\mathfrak { p } ^ { + }$ gate. The metal–semiconductor work function difference becomes important in the fl atband and threshold voltage parameters discussed next. 

## 10.1.5 Flat-Band Voltage

The fl at-band voltage is defi ned as the applied gate voltage such that there is no band bending in the semiconductor and, as a result, zero net space charge in this region. Figure 10.17 shows this fl at-band condition. Because of the work function difference and possible trapped charge in the oxide, the voltage across the oxide for this case is not necessarily zero. 

We have implicitly been assuming that there is zero net charge density in the oxide material. This assumption may not be valid—a net fi xed charge density, usually positive, may exist in the insulator. The positive charge has been identifi ed with broken or dangling covalent bonds near the oxide–semiconductor interface. During the thermal formation of $\mathrm { S i O } _ { 2 } ,$ oxygen diffuses through the oxide and reacts near the $\mathrm { S i } { - } \mathrm { S i O } _ { 2 }$ interface to form the $\mathrm { S i O } _ { 2 } .$ . Silicon atoms may also break away from the silicon material just prior to reacting to form $\mathrm { S i O } _ { 2 } .$ When the oxidation process is terminated, excess silicon may exist in the oxide near the interface, resulting in the dangling bonds. The magnitude of this oxide charge seems, in general, to be a strong function of the oxidizing conditions such as oxidizing ambient and temperature. The charge density can be altered to some degree by annealing the oxide in an argon or nitrogen atmosphere. However, the charge is rarely zero. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/3ea71e09e90f82754d915917a8f4e37f7d8b5ff65cb206fd8ddb04a3afe01b19.jpg)



Figure 10.17 | Energy-band diagram of a MOS capacitor at fl at band.


The net fi xed charge in the oxide appears to be located fairly close to the oxide– semiconductor interface. We will assume in the analysis of the MOS structure that an equivalent trapped charge per unit area, $\boldsymbol { Q } _ { s s } ^ { \prime } ,$ is located in the oxide directly adjacent to the oxide–semiconductor interface. For the moment, we will ignore any other oxide-type charges that may exist in the device. The parameter $Q _ { s s } ^ { \prime }$ is usually given in terms of number of electronic charges per unit area. 

Equation (10.14), for zero applied gate voltage, can be written as 

$$
V _ {\mathrm{ox} 0} + \phi_ {s 0} = - \phi_ {m s} \tag {10.19}
$$

If a gate voltage is applied, the potential drop across the oxide and the surface potential will change. We can then write 

$$
V _ {G} = \Delta V _ {\mathrm{ox}} + \Delta \phi_ {s} = (V _ {\mathrm{ox}} - V _ {\mathrm{ox0}}) + (\phi_ {s} - \phi_ {s 0}) \tag {10.20}
$$

Using Equation (10.19), we have 

$$
V _ {G} = V _ {\mathrm{ox}} + \phi_ {s} + \phi_ {m s} \tag {10.21}
$$

Figure 10.18 shows the charge distribution in the MOS structure for the fl atband condition. There is zero net charge in the semiconductor, and we can assume that an equivalent fi xed surface charge density exists in the oxide. The charge density on the metal is $Q _ { m } ^ { \prime } ,$ , and from charge neutrality we have 

$$
Q _ {m} ^ {\prime} + Q _ {s s} ^ {\prime} = 0 \tag {10.22}
$$

We can relate $\boldsymbol { Q } _ { m } ^ { \prime }$ to the voltage across the oxide by 

$$
V _ {\mathrm{ox}} = \frac {Q _ {m} ^ {\prime}}{C _ {\mathrm{ox}}} \tag {10.23}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/cc9f02db58c1136bef962839c80a545729cc2c4d50a37e14980880789006760c.jpg)



Figure 10.18 | Charge distribution in a MOS capacitor at fl at band.


where $C _ { \mathrm { o x } }$ is the oxide capacitance per unit area.1 Substituting Equation (10.22) into Equation (10.23), we have 

$$
V _ {\mathrm{ox}} = \frac {- Q _ {s s} ^ {\prime}}{C _ {\mathrm{ox}}} \tag {10.24}
$$

In the fl at-band condition, the surface potential is zero, or $\phi _ { s } = 0$ . Then from Equation (10.21), we have 

$$
V _ {G} = \boxed {V _ {F B} = \phi_ {m s} - \frac {Q _ {s s} ^ {\prime}}{C _ {\mathrm{ox}}}} \tag {10.25}
$$

Equation (10.25) is the fl at-band voltage for this MOS device. 

Objective: Calculate the fl at-band voltage for a MOS capacitor with a p-type semiconductor substrate. 

Consider a MOS capacitor with a p-type silicon substrate doped to $N _ { a } = 1 0 ^ { 1 6 } \mathrm { ~ c m } ^ { - 3 } .$ , a silicon dioxide insulator with a thickness of $t _ { o x } = 2 0 \mathrm { n m } = 2 0 0 \mathring \mathrm { \mathrm { A } } .$ , and an $\mathrm { n ^ { + } }$ polysilicon gate. Assume that $Q _ { s s } ^ { \prime } = 5 \times 1 0 ^ { 1 0 }$ electronic charges per cm2. 

## Solution

The work function difference, from Figure 10.16, is $\phi _ { m s } \cong - 1 . 1 \mathrm { V } .$ The oxide capacitance is found to be 

$$
C _ {o x} = \frac {\epsilon_ {o x}}{t _ {o x}} = \frac {(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})}{2 0 0 \times 1 0 ^ {- 8}} = 1. 7 2 6 \times 1 0 ^ {- 7} \mathrm {F / cm^ {2}}
$$

The equivalent oxide charge density is 

$$
Q _ {s s} ^ {\prime} = (5 \times 1 0 ^ {1 0}) (1. 6 \times 1 0 ^ {- 1 9}) = 8 \times 1 0 ^ {- 9} \mathrm{C/cm} ^ {2}
$$

The fl at-band voltage is then determined to be 

$$
V _ {F B} = \phi_ {m s} - \frac {Q _ {s s} ^ {\prime}}{C _ {o x}} = - 1. 1 \frac {- 8 \times 1 0 ^ {- 9}}{1 . 7 2 6 \times 1 0 ^ {- 7}} = - 1. 1 5 \mathrm{V}
$$

EXAMPLE 10.3 

## ■ Comment

The applied gate voltage required to achieve the fl at-band condition for this p-type substrate is negative. If the amount of fi xed oxide charge increases, the fl at-band voltage becomes even more negative. 

## ■ EXERCISE PROBLEM

Ex 10.3 Repeat Example 10.3 for a doping concentration of $N _ { a } = 2 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , an oxide thickness of $t _ { o x } = 4 \ : \mathrm { n m } = 4 0 \ : \mathring { \mathrm { A } }$ , and $Q _ { s s } ^ { \prime } = 2 \times 1 0 ^ { 1 0 }$ electronic charges per cm2. What is the value of the metal–semiconductor work function difference? 

$$
(A n s. \phi_ {m s} \approx - 1. 0 3 V, V _ {F B} = - 1. 0 3 4 V)
$$

## 10.1.6 Threshold Voltage

The threshold voltage is defi ned as the applied gate voltage required to achieve the threshold inversion point. The threshold inversion point, in turn, is defi ned as the con dition when the surface potential is $\phi _ { s } = 2 \phi _ { f p }$ for the p-type semiconductor and $\phi _ { s } = 2 \phi _ { \mathrm { \it f n } }$ for the n-type semiconductor. These conditions are shown in Figures 10.9 and 10.10. The threshold voltage will be derived in terms of the electrical and geometrical properties of the MOS capacitor. 

Figure 10.19 shows the charge distribution through the MOS device at the threshold inversion point for a p-type semiconductor substrate. The space charge width has reached its maximum value. We will assume that there is an equiva lent oxide charge $Q _ { s s } ^ { \prime }$ and the positive charge on the metal gate at threshold is $\boldsymbol { Q } _ { m T } ^ { \prime } .$ The prime on the charge terms indicates charge per unit area. Even though we are assuming that the surface has been inverted, we will neglect the inversion layer charge at this threshold inversion point. From conservation of charge, we can write 

$$
Q _ {m T} ^ {\prime} + Q _ {s s} ^ {\prime} = \left| Q _ {S D} ^ {\prime} (\max) \right| \tag {10.26}
$$

where 

$$
\left| Q _ {S D} ^ {\prime} (\max) \right| = e N _ {a} x _ {d T} \tag {10.27}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/611573abefbe06ec82cb046b37123749645f31cc2045e932154b031ef3541890.jpg)



Figure 10.19 | Charge distribution in a MOS capacitor with a p-type substrate at the threshold inversion point.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/9f52734e07742f837e1fce8e262d3663963040c01451b254efce1f47de47f492.jpg)



Figure 10.20 | Energy-band diagram through the MOS structure with a positive applied gate bias.


and is the magnitude of the maximum space charge density per unit area of the depletion region. 

The energy-band diagram of the MOS system with an applied positive gate voltage is shown in Figure 10.20. As we mentioned, an applied gate voltage will change the voltage across the oxide and will change the surface potential. We had from Equ ation (10.20) that 

$$
V _ {G} = \Delta V _ {\mathrm{ox}} + \Delta \phi_ {s} = V _ {\mathrm{ox}} + \phi_ {s} + \phi_ {m s}
$$

At threshold, we can defi ne $V _ { G } = V _ { T N } ,$ where $V _ { T N }$ is the threshold voltage that creates the electron inversion layer charge. The surface potential is $\phi _ { s } = 2 \phi _ { f p }$ at threshold, so Equation (10.20) can be written as 

$$
V _ {T N} = V _ {\mathrm{ox} T} + 2 \phi_ {f p} + \phi_ {m s} \tag {10.28}
$$

where $V _ { \mathrm o x T }$ is the voltage across the oxide at this threshold inversion point. 

The voltage $V _ { \mathrm o x T }$ can be related to the charge on the metal and to the oxide capa citance by 

$$
V _ {\mathrm{ox} T} = \frac {Q _ {m T} ^ {\prime}}{C _ {\mathrm{ox}}} \tag {10.29}
$$

where again $C _ { \mathrm { o x } }$ is the oxide capacitance per unit area. Using Equation (10.26), we can write 

$$
V _ {\mathrm{ox} T} = \frac {Q _ {m T} ^ {\prime}}{C _ {\mathrm{ox}}} = \frac {1}{C _ {\mathrm{ox}}} \left(\left| Q _ {S D} ^ {\prime} (\max) \right| - Q _ {s s} ^ {\prime}\right) \tag {10.30}
$$

Finally, the threshold voltage can be written as 

$$
V _ {T N} = \frac {\left| Q _ {S D} ^ {\prime} (\max) \right|}{C _ {\mathrm{ox}}} - \frac {Q _ {s s} ^ {\prime}}{C _ {\mathrm{ox}}} + \phi_ {m s} + 2 \phi_ {f p} \tag {10.31a}
$$

or 

$$
V _ {T N} = \left(\left| Q _ {S D} ^ {\prime} (\max) \right| - Q _ {s s} ^ {\prime}\right) \left(\frac {t _ {\mathrm{ox}}}{\epsilon_ {\mathrm{ox}}}\right) + \phi_ {m s} + 2 \phi_ {f p} \tag {10.31b}
$$

Using the defi nition of fl at-band voltage from Equation (10.25), we can also express the threshold voltage as 

$$
V _ {T N} = \frac {\left| Q _ {S D} ^ {\prime} (\max) \right|}{C _ {\mathrm{ox}}} + V _ {F B} + 2 \phi_ {f p} \tag {10.31c}
$$

For a given semiconductor material, oxide material, and gate metal, the threshold volt age is a function of semiconductor doping, oxide charge $\boldsymbol { Q } _ { s s } ^ { \prime } ,$ and oxide thickness. 

## EXAMPLE 10.4

Objective: Calculate the threshold voltage of a MOS system using an aluminum gate. 

Consider a p-type silicon substrate at T  300 K doped to $N _ { a } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } .$ . Let $Q _ { s s } ^ { \prime } =$ $1 0 ^ { 1 0 }$ cm2, $, t _ { o x } = 1 2 \mathrm { n m } = 1 2 0 \mathring { \mathrm { A } } .$ , and assume the oxide is silicon dioxide. 

## Solution

From Figure 10.16, we fi nd $\phi _ { m s } \cong - 0 . 8 8 \ : \mathrm { V } .$ . The other parameters are 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {i}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0 ^ {1 5}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 2 8 7 7 \mathrm{V}
$$

and 

$$
x _ {d T} = \left\{\frac {4 \epsilon_ {s} \phi_ {f p}}{e N _ {a}} \right\} ^ {1 / 2} = \left\{\frac {4 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 2 8 7 7)}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 5})} \right\} ^ {1 / 2} = 8. 6 3 \times 1 0 ^ {- 5} \mathrm{cm}
$$

Then 

$$
\left| Q _ {S D} ^ {\prime} (\max) \right| = e N _ {a} x _ {d T} = (1. 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 5}) (8. 6 3 \times 1 0 ^ {- 5}) = 1. 3 8 1 \times 1 0 ^ {- 8} \mathrm{C} / \mathrm{cm} ^ {2}
$$

The threshold voltage is now found to be 

$$
\begin{array}{l} V _ {T N} = \left(\left| Q _ {S D} ^ {\prime} (\max) \right| - Q _ {s s} ^ {\prime}\right) \left(\frac {t _ {o x}}{\epsilon_ {o x}}\right) + \phi_ {m s} + 2 \phi_ {f p} \\ = \left[ (1. 3 8 1 \times 1 0 ^ {- 8}) - (1 0 ^ {1 0}) (1. 6 \times 1 0 ^ {- 1 9}) \right] \cdot \left[ \frac {1 2 0 \times 1 0 ^ {- 8}}{(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})} \right] \\ + (- 0. 8 8) + 2 (0. 2 8 7 7) \\ \end{array}
$$

or 

$$
V _ {T N} = - 0. 2 6 2 \mathrm{V}
$$

## ■ Comment

In this example, the semiconductor is fairly lightly doped, which, in conjunction with the positive charge in the oxide and the work function difference, is suffi cient to induce an electron inversion layer charge even with zero applied gate voltage. This condition makes the threshold voltage negative. 

## ■ EXERCISE PROBLEM

Ex 10.4 Determine the metal–semiconductor work function difference and the threshold v oltage for a silicon MOS device at T  300 K for the following parameters: 

$$
\mathrm{p} ^ {+} \text {   polysilicon   gate,   } N _ {a} = 2 \times 1 0 ^ {1 6} \mathrm{cm} ^ {- 3}, t _ {o x} = 8 \mathrm{nm} = 8 0 \mathrm {\AA}, \text {   and   } Q _ {s s} ^ {\prime} = 2 \times 1 0 ^ {1 0} \mathrm{cm} ^ {- 2}.
$$

$$
(\text { Ans. } \phi_ {m n} \approx + 0. 2 8 \mathrm{V}, \mathrm{V} _ {T N} = + 1. 1 6 \mathrm{V})
$$

A negative threshold voltage for a p-type substrate implies a depletion mode device. A negative voltage must be applied to the gate in order to make the inversion layer charge equal to zero, whereas a positive gate voltage will induce a larger inversion layer charge. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/7e2ddf7e51fc6ea9d4f5012f674e2c9edf3bd616780da1ea86b07872515510c7.jpg)



Figure 10.21 | Threshold voltage of an n-channel MOSFET versus the p-type substrate doping concentration for various values of oxide trapped charge $( t _ { \mathrm { o x } } = 5 0 0 \mathrm { \AA }$ , aluminum gate).


Figure 10.21 is a plot of the threshold voltage $V _ { T N }$ as a function of the acceptor doping concentration for various positive oxide charge values. We may note that the p-type semiconductor must be somewhat heavily doped in order to obtain an enhancement mode device. 

The previous derivation of the threshold voltage assumed a p-type semiconductor substrate. The same type of derivation can be done with an n-type semiconductor substrate, where a negative gate voltage can induce an inversion layer of holes at the oxide–semiconductor interface. 

Figure 10.15 shows the energy-band diagram of the MOS structure with an ntype substrate and with an applied negative gate voltage. The threshold voltage for this case can be derived and is given by 

$$
V _ {T P} = \left(- \left| Q _ {S D} ^ {\prime} (\max) \right| - Q _ {s s} ^ {\prime}\right) \left(\frac {t _ {\mathrm{ox}}}{\epsilon_ {\mathrm{ox}}}\right) + \phi_ {m s} - 2 \phi_ {f n} \tag {10.32}
$$

where 

$$
\phi_ {m s} = \phi_ {m} ^ {\prime} - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} - \phi_ {f n}\right) \tag {10.33a}
$$

$$
\left| Q _ {S D} ^ {\prime} (\max) \right| = e N _ {d} x _ {d T} \tag {10.33b}
$$

$$
x _ {d T} = \left\{\frac {4 \epsilon_ {s} \phi_ {f n}}{e N _ {d}} \right\} ^ {1 / 2} \tag {10.33c}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/be13e8246aae90dc4a0e2d00bc986381ed7471fd103a21b4b02da8ede8f24811.jpg)



Figure 10.22 | Threshold voltage of a p-channel MOSFET versus the n-type substrate doping concentration for various values of oxide trapped charge $( t _ { \mathrm { o x } } = 5 0 0 \mathring { \mathrm { A } } .$ , aluminum gate).


and 

$$
\phi_ {f n} = V _ {t} \ln \left(\frac {N _ {d}}{n _ {i}}\right) \tag {10.33d}
$$

We may note that $x _ { d T }$ and $\phi _ { f n }$ are defi ned as positive quantities. We may also note that the notation of $V _ { T P }$ is the threshold voltage that will induce an inversion layer of holes. We will later drop the N and P subscript notation on the threshold voltage, but, for the moment, the notation may be useful for clarity. 

Figure 10.22 is a plot of $V _ { T P }$ versus doping concentration for several values of $Q _ { s s } ^ { \prime }$ . We may note that, for all values of positive oxide charge, this MOS capacitor is always an enhancement mode device. As the $Q _ { s s } ^ { \prime }$ charge increases, the threshold voltage becomes more negative, which means that it takes a larger applied gate voltage to create the inversion layer of holes at the oxide–semiconductor interface. 

DESIGN EXAMPLE 10.5 

Objective: Determine the gate material and design the semiconductor doping concentration to yield a specifi ed threshold voltage. 

Consider a MOS device with silicon dioxide and an n-type silicon substrate. The oxide thickness is $t _ { o x } = 1 2 \mathrm { n m } = 1 2 0 \mathring \mathrm { A }$ and the oxide charge is $Q _ { s s } ^ { \prime } = 2 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . The threshold voltage is to be approximately $V _ { T P } = - 0 . 3 \ : \mathrm { V } .$ 

## ■ Solution

The solution to this design problem is not straight forward, since the doping concentration parameter appears in the terms $\phi _ { f n } , x _ { d T } , Q _ { s D } ^ { \prime } \left( \mathrm { m a x } \right)$ , and $\phi _ { m s } .$ . The threshold voltage, then, is a nonlinear function of $N _ { d } .$ We resort to trial and error to obtain a solution. 

Figure 10.22 shows the threshold voltage for an aluminum gate system. Since the required threshold voltage in this problem is less negative than the values shown in Figure 10.22, we require a metal–semiconductor work function difference value that is more positive than for the aluminum gate. We therefore choose $\mathfrak { l } \mathfrak { p } ^ { + }$ polysilicon gate. 

Consider a doping concentration of $N _ { d } = 1 0 ^ { 1 7 } ~ \mathrm { c m } ^ { - 3 } .$ . From Figure 10.16, the metal– semiconductor work function difference is $\phi _ { m s } \cong + 1 . 1 \mathrm { ~ V ~ }$ . The remaining parameters are found to be 

$$
\phi_ {f n} = V _ {t} \ln \left(\frac {N _ {d}}{n _ {i}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0 ^ {1 7}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 4 0 7 \mathrm{V}
$$

$$
x _ {d T} = \left(\frac {4 \epsilon_ {s} \phi_ {f n}}{e N _ {d}}\right) ^ {1 / 2} = \left\{\frac {4 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 4 0 7)}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 7})} \right\} ^ {1 / 2}
$$

$$
= 1. 0 2 6 \times 1 0 ^ {- 5} \mathrm{cm}
$$

$$
\begin{array}{l} \left| Q _ {S D} ^ {\prime} (\max) \right| = e N _ {d} x _ {d T} = (1. 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 7}) (1. 0 2 6 \times 1 0 ^ {- 5}) \\ = 1. 6 4 2 \times 1 0 ^ {- 7} \mathrm{C} / \mathrm{cm} ^ {2} \\ \end{array}
$$

The threshold voltage is determined to be 

$$
V _ {T P} = \left[ - \left| Q _ {S D} ^ {\prime} (\max) \right| - Q _ {s s} ^ {\prime} \right] \cdot \left(\frac {t _ {o x}}{\epsilon_ {o x}}\right) + \phi_ {m s} - 2 \phi_ {f n}
$$

or 

$$
\begin{array}{l} V _ {T P} = \frac {\left[ - (1 . 6 4 2 \times 1 0 ^ {- 7}) - (2 \times 1 0 ^ {1 0}) (1 . 6 \times 1 0 ^ {- 1 9}) \right] \cdot (1 2 0 \times 1 0 ^ {- 8})}{(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})} \\ + 1. 1 - 2 (0. 4 0 7) \\ \end{array}
$$

which yields 

$$
V _ {T P} = - 0. 2 9 6 \mathrm{V} \cong - 0. 3 \mathrm{V}
$$

## ■ Comment

The negative threshold voltage, with the n-type substrate, implies that this MOS capacitor is an enhancement mode device. The inversion layer charge is zero with zero applied gate voltage, and a negative gate voltage must be applied to induce the hole inversion charge. 

## ■ EXERCISE PROBLEM

Ex 10.5 Consider a MOS capacitor with silicon dioxide and an n-type silicon substrate at T  300 K with the following parameters: $\mathfrak { p } ^ { + }$ polysilicon gate, $N _ { d } = 2 \times$ $1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } , t _ { o x } = 2 0 \mathrm { n m } = 2 0 0 \mathring { \mathrm { A } } ,$ , and $Q _ { s s } ^ { \prime } = 5 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . Determine the threshold voltage. Is the capacitor an enhancement mode or depletion mode device? enhancement mode) ${ } ^ { \circ } \Lambda \mathsf { Z I } ^ { \cdot } 0 - = { } ^ { d L } \Lambda \mathsf { \Omega } ^ { \cdot } \mathsf { S U } \mathsf { Y } )$ 

## TEST YOUR UNDERSTANDING

TYU 10.1 (a) Consider an oxide-to-n-type silicon junction at $T = 3 0 0 \mathrm { K } .$ . The impurity doping concentration in the silicon is $N _ { d } = 8 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Calculate the maximum space charge width in the silicon. (b) Repeat part (a) for a doping concentration of $N _ { d } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . 

$$
[ \mathrm{Ans.} (a) 0. 3 3 2 \mu \mathrm{m}; (b) 0. 1 5 8 \mu \mathrm{m} ]
$$

TYU 10.2 Consider an $\mathrm { n ^ { + } }$ polysilicon gate in a MOS structure with a p-type silicon substrate. The doping concentration of the silicon is $N _ { a } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Using Equation (10.16), fi nd the value of $\phi _ { m s }$ . 

$$
(\text { Ans. } \phi_ {m s} = - 0. 9 3 6 \text { V })
$$

TYU 10.3 Repeat TYU 10.2 for a $\mathfrak { p } ^ { + }$ polysilicon gate using Equation (10.17). 

$$
(\text { Ans. } \phi_ {m s} = + 0. 1 8 4 \mathrm{V})
$$

TYU 10.4 Consider the MOS capacitor described in Exercise TYU 10.3. The oxide thickness is $t _ { o x } = 1 6 \mathrm { n m } = 1 6 0 \mathring { \mathrm { A } }$ and the oxide charge density is $Q _ { s s } ^ { \prime } = 8 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ Determine the fl at-band voltage. 

$$
(\text { Ans. } + 0. 1 2 5 \mathrm{V})
$$

TYU 10.5 Consider an $\mathrm { n ^ { + } }$ polysilicon gate on silicon dioxide with a p-type silicon substrate doped to $N _ { a } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ . Assume $Q _ { s s } ^ { \prime } = 5 \times 1 0 ^ { 1 0 }$ cm2. Determine the required oxide thickness such that the threshold voltage is $V _ { T N } = + 0 . 6 5 \ : \mathrm { V } .$ 

$$
(\text { Ans. } t _ {o x} = 4 5. 2 \mathrm{nm} = 4 5 2 \mathrm{A})
$$

## 10.2 | CAPACITANCE–VOLTAGE CHARACTERISTICS

As mentioned previously, the MOS capacitor structure is the heart of the MOSFET. A great deal of information about the MOS device and the oxide–semiconductor interface can be obtained from the capacitance versus voltage or C–V characteristics of the device. The capacitance of a device is defi ned as 

$$
C = \frac {d Q}{d V} \tag {10.34}
$$

where dQ is the magnitude of the differential change in charge on one plate as a function of the differential change in voltage $d V$ across the capacitor. The capacitance is a small-signal or ac parameter and is measured by superimposing a small ac voltage on an applied dc gate voltage. The capacitance, then, is measured as a function of the applied dc gate voltage. 

## 10.2.1 Ideal C–V Characteristics

First we will consider the ideal C–V characteristics of the MOS capacitor and then discuss some of the deviations that occur from these idealized results. We will initially assume that there is zero charge trapped in the oxide and also that there is no charge trapped at the oxide–semiconductor interface. 

There are three operating conditions of interest in the MOS capacitor: accumulation, depletion, and inversion. Figure 10.23a shows the energy-band diagram of a MOS capacitor with a p-type substrate for the case when a negative voltage is applied to the gate, inducing an accumulation layer of holes in the semiconductor at the oxide–semiconductor interface. A small differential change in voltage across the MOS structure will cause a differential change in charge on the metal gate and also in the hole accumulation charge, as shown in Figure 10.23b. The differential changes in charge density occur at the edges of the oxide, as in a parallel-plate capacitor. The capacitance $C ^ { \prime }$ per unit area of the MOS capacitor for this accumulation mode is just the oxide capacitance, or 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/99fd03005a1ecb8be58baa762897e8d2fafb3edfb4e1134164715e7e5d1d667c.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/6d1e357432324c45c1b326031c8e5228507bd50fb2d4eebc71d1490ad6ae6e55.jpg)



(b)



Figure 10.23 | (a) Energy-band diagram through a MOS capacitor for the accumulation mode. (b) Differential charge distribution at accumulation for a differential change in gate voltage.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/c5c07aeb2175e1ab0896f36b0475c08ec6a893bc05a559680275124c20d209fa.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/4428289f819a239c3a72a0fac0f07c9f93347fd15761eb8122457f6b49ac9471.jpg)



(b)



Figure 10.24 | (a) Energy-band diagram through a MOS capacitor for the depletion mode. (b) Differential charge distribution at depletion for a differential change in gate voltage.


$$
C ^ {\prime} (\mathrm{acc}) = C _ {\mathrm{ox}} = \frac {\epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}}} \tag {10.35}
$$

Figure 10.24a shows the energy-band diagram of the MOS device when a small positive voltage is applied to the gate, inducing a space charge region in the semiconductor; Figure 10.24b shows the charge distribution through the device for this condition. The oxide capacitance and the capacitance of the depletion region are in series. A small differential change in voltage across the capacitor will cause a differential change in the space charge width. The corresponding differential changes in charge densities are shown in the fi gure. The total capacitance of the series combination is 

$$
\frac {1}{C ^ {\prime} (\mathrm{depl})} = \frac {1}{C _ {\mathrm{ox}}} + \frac {1}{C _ {S D} ^ {\prime}} \tag {10.36a}
$$

or 

$$
C ^ {\prime} (\mathrm{depl}) = \frac {C _ {\mathrm{ox}} C _ {S D} ^ {\prime}}{C _ {\mathrm{ox}} + C _ {S D} ^ {\prime}} \tag {10.36b}
$$

Since $C _ { \mathrm { o x } } = \epsilon _ { \mathrm { o x } } / t _ { \mathrm { o x } }$ and $C _ { S D } ^ { \prime } = \epsilon _ { s } / x _ { d } ,$ Equation (10.36b) can be written as 

$$
C ^ {\prime} (\text { depl }) = \frac {C _ {\mathrm{ox}}}{1 + \frac {C _ {\mathrm{ox}}}{C _ {S D} ^ {\prime}}} = \frac {\epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}} + \left(\frac {\epsilon_ {\mathrm{ox}}}{\epsilon_ {s}}\right) x _ {d}} \tag {10.37}
$$

As the space charge width increases, the total capacitance $C ^ { \prime } ( \mathrm { d e p l } )$ decreases. 

We had defi ned the threshold inversion point to be the condition when the maximum depletion width is reached, but there is essentially zero inversion charge density. This condition will yield a minimum capacitance $C _ { \mathrm { m i n } } ^ { \prime } ,$ which is given by 

$$
C _ {\min} ^ {\prime} = \frac {\epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}} + \left(\frac {\epsilon_ {\mathrm{ox}}}{\epsilon_ {s}}\right) x _ {d T}} \tag {10.38}
$$

Figure 10.25a shows the energy-band diagram of this MOS device for the inversion condition. In the ideal case, a small incremental change in the voltage across the MOS capacitor will cause a differential change in the inversion layer charge density. The space charge width does not change. If the inversion charge can respond to the change in capacitor voltage as indicated in Figure 10.25b, then the capacitance is again just the oxide capacitance, or 

$$
C ^ {\prime} (\mathrm{inv}) = C _ {\mathrm{ox}} = \frac {\epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}}} \tag {10.39}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/bc0b259caf00644b3df5fbe6e5e0b5e94966fc7263b2a0250ac7444cf8341eae.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/3cc7b9776f6d843522a50477113e770657fb9d30bb185b0ab192fd6aa40a1aa9.jpg)



(b)



Figure 10.25 | (a) Energy-band diagram through a MOS capacitor for the inversion mode. (b) Differential charge distribution at inversion for a low-frequency differential change in gate voltage.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/003264fc9d76aeee5365f999c2c7c74969f9c6f7e8038f463b82dcd06d6d3181.jpg)



Figure 10.26 | Ideal low-frequency capacitance versus gate voltage of a MOS capacitor with a p-type substrate. Individual capacitance components are also shown.


Figure 10.26 shows the ideal capacitance versus gate voltage, or C–V, characteristics of the MOS capacitor with a p-type substrate. The three dashed segments correspond to the three components $C _ { \mathrm { o x } } , C _ { S D } ^ { \prime } ,$ and $C _ { \mathrm { m i n } } ^ { \prime } .$ The solid curve is the ideal net capacitance of the MOS capacitor. Moderate inversion, which is indicated in the fi gure, is the transition region between the point when only the space charge density changes with gate voltage and when only the inversion charge density changes with gate voltage. 

The point on the curve that corresponds to the fl at-band condition is of interest. The fl at-band condition occurs between the accumulation and depletion conditions. The capacitance at fl at band is given by 

$$
C _ {F B} ^ {\prime} = \frac {\epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}} + \left(\frac {\epsilon_ {\mathrm{ox}}}{\epsilon_ {s}}\right) \sqrt {\left(\frac {k T}{e}\right) \left(\frac {\epsilon_ {s}}{e N _ {a}}\right)}} \tag {10.40}
$$

We may note that the fl at-band capacitance is a function of oxide thickness as well as semiconductor doping. The general location of this point on the C–V plot is shown in Figure 10.26. 

Objective: Calculate $C _ { o x } , C _ { \mathrm { m i n } } ^ { \prime } ,$ and $C _ { F B } ^ { \prime }$ for a MOS capacitor. 

Consider a p-type silicon substrate at T  300 K doped to $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } .$ . 

The oxide is silicon dioxide with a thickness of $t _ { o x } = 1 8 \ \mathrm { n m } = 1 8 0 \ \mathring { \mathrm { A } }$ , and the gate is aluminum. 

## Solution

The oxide capacitance is 

$$
C _ {o x} = \frac {\epsilon_ {o x}}{t _ {o x}} = \frac {(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})}{1 8 0 \times 1 0 ^ {- 8}} = 1. 9 1 7 5 \times 1 0 ^ {- 7} \mathrm {F / cm^ {2}}
$$

To fi nd the minimum capacitance, we need to calculate 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {i}}\right) = (0. 0 2 5 9) \ln \left(\frac {1 0 ^ {1 6}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 3 4 7 3 \mathrm{V}
$$

EXAMPLE 10.6 

and 

$$
\begin{array}{l} x _ {d T} = \left\{\frac {4 \epsilon_ {s} \phi_ {f p}}{e N _ {a}} \right\} ^ {1 / 2} = \left\{\frac {4 (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (0 . 3 4 7 3)}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 6})} \right\} ^ {1 / 2} \\ \cong 0. 3 0 \times 1 0 ^ {- 4} \mathrm{cm} \\ \end{array}
$$

Then 

$$
\begin{array}{l} C _ {\min} ^ {\prime} = \frac {\epsilon_ {o x}}{t _ {o x} + \left(\frac {\epsilon_ {o x}}{\epsilon_ {s}}\right) x _ {d T}} = \frac {(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})}{1 8 0 \times 1 0 ^ {- 8} + \left(\frac {3 . 9}{1 1 . 7}\right) (0 . 3 0 \times 1 0 ^ {- 4})} \\ = 2. 9 2 5 \times 1 0 ^ {- 8} \mathrm{F} / \mathrm{cm} ^ {2} \\ \end{array}
$$

We may note that 

$$
\frac {C _ {\min} ^ {\prime}}{C _ {o x}} = \frac {2 . 9 2 5 \times 1 0 ^ {- 8}}{1 . 9 1 7 5 \times 1 0 ^ {- 7}} = 0. 1 5 2 5
$$

The fl at-band capacitance is 

$$
\begin{array}{l} C _ {F B} ^ {\prime} = \frac {\epsilon_ {o x}}{t _ {o x} + \left(\frac {\epsilon_ {o x}}{\epsilon_ {s}}\right) \sqrt {\frac {V _ {t} \epsilon_ {s}}{e N _ {a}}}} \\ = \frac {(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})}{1 8 0 \times 1 0 ^ {- 8} + \left(\frac {3 . 9}{1 1 . 7}\right) \sqrt {\frac {(0 . 0 2 5 9) (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4})}{(1 . 6 \times 1 0 ^ {- 1 9}) (1 0 ^ {1 6})}}} \\ = 1. 0 9 1 \times 1 0 ^ {- 7} \mathrm{F} / \mathrm{cm} ^ {2} \\ \end{array}
$$

We also note that 

$$
\frac {C _ {F B} ^ {\prime}}{C _ {o x}} = \frac {1 . 0 9 1 \times 1 0 ^ {- 7}}{1 . 9 1 7 5 \times 1 0 ^ {- 7}} = 0. 5 6 9
$$

## ■ Comment

The ratios of $C _ { \mathrm { m i n } } ^ { \prime } / C _ { o x }$ and $C _ { F B } ^ { \prime } / C _ { o x }$ are typical values obtained in C–V plots. 

## ■ EXERCISE PROBLEM

Ex 10.6 Consider a MOS capacitor with the following parameters: n polysilicon gate, $N _ { a } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } , t _ { o x } = 8 \mathrm { n m } = 8 0 \mathring { \mathrm { A } } ,$ and $Q _ { s s } ^ { \prime } = 2 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . Determine the ratios $C _ { \mathrm { m i n } } ^ { \prime } / C _ { o x }$ and $C _ { F B } ^ { \prime } / C _ { o x } .$ 

$$
(A n s. C _ {i n} ^ {\prime} / C _ {o x} = 0. 1 1 8, C _ {F B} ^ {\prime} / C _ {o x} = 0. 5 0 4)
$$

If we assume the oxide capacitance per unit area is $C _ { o x } = 1 . 9 1 7 5 \times 1 0 ^ { - 7 } { \mathrm { F / c m } } ^ { 2 }$ and the channel length and width are $L = 2 \mu \mathrm { m }$ and $W = 2 0 \ \mu \mathrm { m }$ , respectively, then the total gate oxide capacitance is 

$$
\begin{array}{l} C _ {o x T} = C _ {o x} L W = (1. 9 1 7 5 \times 1 0 ^ {- 7}) (2 \times 1 0 ^ {- 4}) (2 0 \times 1 0 ^ {- 4}) \\ = 7. 6 7 \times 1 0 ^ {- 1 4} \mathrm{F} = 0. 0 7 6 7 \mathrm{pF} = 7 6. 7 \mathrm{fF} \\ \end{array}
$$

The total oxide capacitance in a typical MOS device is quite small. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/403aee80bda4ff88c52764d7f72d1d0b4bef828eecab6ebf9e735280ffdee92b.jpg)



Figure 10.27 | Ideal low-frequency capacitance versus gate voltage of a MOS capacitor with an n-type substrate.


The same type of ideal C–V characteristics is obtained for a MOS capacitor with an n-type substrate by changing the sign of the voltage axis. The accumulation condition is obtained for a positive gate bias and the inversion condition is obtained for a negative gate bias. This ideal curve is shown in Figure 10.27. 

## 10.2.2 Frequency Effects

Figure 10.25a shows the MOS capacitor with a p-type substrate and biased in the inversion condition. We have argued that a differential change in the capacitor voltage in the ideal case causes a differential change in the inversion layer charge density. However, we must consider the source of electrons that produces a change in the inversion charge density. 

There are two sources of electrons that can change the charge density of the inversion layer. The fi rst source is by diffusion of minority carrier electrons from the p-type substrate across the space charge region. This diffusion process is the same as that in a reverse-biased pn junction that generates the ideal reverse saturation current. The second source of electrons is by thermal generation of electron–hole pairs within the space charge region. This process is again the same as that in a reverse- biased pn junction generating the reverse-biased generation current. Both of these processes generate electrons at a particular rate. The electron concentration in the inversion layer, then, cannot change instantaneously. If the ac voltage across the MOS capacitor changes rapidly, the change in the inversion layer charge will not be able to respond. The C–V characteristics will then be a function of the frequency of the ac signal used to measure the capacitance. 

In the limit of a very high frequency, the inversion layer charge will not respond to a differential change in capacitor voltage. Figure 10.28 shows the charge distribution in the MOS capacitor with a p-type substrate. At a high-signal frequency, the differential change in charge occurs at the metal and in the space charge width in the semiconductor. The capacitance of the MOS capacitor is then $C _ { \mathrm { m i n } } ^ { \prime } .$ which we discussed earlier. 

The high-frequency and low-frequency limits of the C–V characteristics are shown in Figure 10.29. In general, high frequency corresponds to a value on the order of 1 MHz and low frequency corresponds to values in the range of 5 to 100 Hz. Typically, the high-frequency characteristics of the MOS capacitor are measured. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d5520587796be9445d5a5a7a81a6b52e90f068181b692b7751f01eebc83dac9d.jpg)



Figure 10.28 | Differential charge distribution at inversion for a high-frequency differential change in gate voltage.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/00482b0341ac1837c82b7f3433b84f0da135d0d8b1379812529af850fd0ce491.jpg)



Figure 10.29 | Low-frequency and high-frequency capacitance versus gate voltage of a MOS capacitor with a p-type substrate.


## 10.2.3 Fixed Oxide and Interface Charge Effects

In all of the discussion concerning C–V characteristics so far, we have assumed an ideal oxide in which there are no fi xed oxide or oxide–semiconductor interface charges. These two types of charges will change the C–V characteristics. 

We previously discussed how the fi xed oxide charge affects the threshold voltage. This charge will also affect the fl at-band voltage. The fl at-band voltage from Equation (10.25) is given by 

$$
V _ {F B} = \phi_ {m s} - \frac {Q _ {s s} ^ {\prime}}{C _ {\mathrm{ox}}}
$$

where $Q _ { s s } ^ { \prime }$ is the equivalent fi xed oxide charge and $\phi _ { m s }$ is the metal–semiconductor work function difference. The fl at-band voltage shifts to more negative voltages for a positive fi xed oxide charge. Since the oxide charge is not a function of gate voltage, the curves show a parallel shift with oxide charge, and the shape of the C–V curves remains the same as the ideal characteristics. Figure 10.30 shows the high-frequency characteristics of a MOS capacitor with a p-type substrate for several values of fi xed positive oxide charge. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b3caad4c46a492fd3c7ae616a72bda646dcf37b3e745699db1461d6f209cf2c9.jpg)



Figure 10.30 | High-frequency capacitance versus gate voltage of a MOS capacitor with a p-type substrate for several values of effective trapped oxide charge.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/50ed0b9df287b9c62a92e6cf8db789d325485f019246c0a52417a770567f3f19.jpg)



Figure 10.31 | Schematic diagram showing interface states at the oxide– semiconductor interface.


The C–V characteristics can be used to determine the equivalent fi xed oxide charge. For a given MOS structure, $\phi _ { m s }$ and $C _ { \mathrm { o x } }$ are known, so the ideal fl at-band voltage and fl at-band capacitance can be calculated. The experimental value of fl at-band voltage can be measured from the C–V curve, and the value of fi xed oxide charge can then be determined. The C–V measurements are a valuable diagnostic tool to characterize a MOS device. This characterization is especially useful in the study of radiation effects on MOS devices, for example. 

We fi rst encountered oxide–semiconductor interface states in Chapter 9 in the discussion of Schottky barrier diodes. Figure 10.31 shows the energy-band diagram of a semiconductor at the oxide–semiconductor interface. The periodic nature of the semiconductor is abruptly terminated at the interface so that allowed electronic energy levels will exist within the forbidden bandgap. These allowed energy states are referred to as interface states. Charge can fl ow between the semiconductor and interface states, in contrast to the fi xed oxide charge. The net charge in these interface states is a function of the position of the Fermi level in the bandgap. 

In general, acceptor states exist in the upper half of the bandgap and donor states exist in the lower half of the bandgap. An acceptor state is neutral if the Fermi level is below the state and becomes negatively charged if the Fermi level is above the state. A donor state is neutral if the Fermi level is above the state and becomes positively charged if the Fermi level is below the state. The charge of the interface states is then a function of the gate voltage applied across the MOS capacitor. 

Figure 10.32a shows the energy-band diagram in a p-type semiconductor of a MOS capacitor biased in the accumulation condition. In this case, there is a net positive charge trapped in the donor states. Now let the gate voltage change to produce the energy-band diagram shown in Figure 10.32b. The Fermi level corresponds to the intrinsic Fermi level at the surface; thus, all interface states are neutral. This particular bias condition is known as midgap. Figure 10.32c shows the condition at inversion in which there is now a net negative charge in the acceptor states. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/1888566cd82c801461085f72cd97d9b7ea036385123454d9b8d4c47f988fdcc9.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/215913b3c069d4bb8798e64e849f16f370f310d686b49ad1d86e4fea6397d13f.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/6203dcebb7ce6bafcadf8132d93522527420f9e61b83796ad989a7789bdcc8a8.jpg)



Figure 10.32 | Energy-band diagram in a p-type semiconductor showing the charge trapped in the interface states when the MOS capacitor is biased (a) in accumulation, (b) at midgap, and (c) at inversion.


The net charge in the interface states changes from positive to negative as the gate voltage sweeps from the accumulation, depletion, to the inversion condition. We noted that the C–V curves shifted in the negative gate voltage direction due to positive fi xed oxide charge. When interface states are present, the amount and direction of the shift change as we sweep through the gate voltage, since the amount and sign of the interface trapped charge change. The C–V curves now become “smeared out” as shown in Figure 10.33. 

Again, the C–V measurements can be used as a diagnostic tool in semiconductor device process control. For a given MOS device, the ideal C–V curve can be determined. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/2124ce60a05feb6f67628bd212527027e19b992989dd7993343eb60f8590f62e.jpg)



Figure 10.33 | High-frequency C–V characteristics of a MOS capacitor showing effects of interface states.


Any “smearing out” in the experimental curve indicates the presence of interface states and any parallel shift indicates the presence of fi xed oxide charge. The amount of smearing out can be used to determine the density of interface states. These types of measurement are extremely useful in the study of radiation effects on MOS devices. 

## 10.3 | THE BASIC MOSFET OPERATION

The current in a MOSFET is due to the fl ow of charge in the inversion layer or channel region adjacent to the oxide–semiconductor interface. We have discussed the creation of the inversion layer charge in enhancement-type MOS capacitors. We may also have depletion-type devices in which a channel already exists at zero gate voltage. 

## 10.3.1 MOSFET Structures

There are four basic MOSFET device types. Figure 10.34 shows an n-channel enhancement mode MOSFET. Implicit in the enhancement mode notation is the idea that the semiconductor substrate is not inverted directly under the oxide with zero gate voltage. A positive gate voltage induces the electron inversion layer, which then “connects” the n-type source and the n-type drain regions. The source terminal is the source of carriers that fl ow through the channel to the drain terminal. For this n-channel device, electrons fl ow from the source to the drain so the conventional current will enter the drain and leave the source. The conventional circuit symbol for this n-channel enhancement mode device is also shown in the fi gure. 

Figure 10.35 shows an n-channel depletion mode MOSFET. An n-channel region exists under the oxide with 0 V applied to the gate. However, we have shown that the threshold voltage of a MOS device with a p-type substrate may be negative; this means that an electron inversion layer already exists with zero gate voltage applied. Such a device is also considered to be a depletion mode device. The n-channel shown in the fi gure can be an electron inversion layer or an intentionally doped n region. The conventional circuit symbol for the n-channel depletion mode MOSFET is also shown in the fi gure. 

Figures 10.36a, b show a p-channel enhancement mode MOSFET and a p-channel depletion mode MOSFET. In the p-channel enhancement mode device, a negative gate voltage must be applied to create an inversion layer of holes that will “connect” the p-type source and drain regions. Holes fl ow from the source to the drain, so the conventional current will enter the source and leave the drain. A p-channel region exists in the depletion mode device even with zero gate voltage. The conventional circuit symbols are shown in the fi gure. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/125e4ba1fbd2a93dae7af4dda09e52b13204379799ac21231f978f914e946bc5.jpg)



Figure 10.34 | Cross section and circuit symbol for an n-channel enhancement mode MOSFET.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/9d39ccc853600c72d91586b63c669de0023303ee0cb27cd3b344fa74b0040cf1.jpg)



Figure 10.35 | Cross section and circuit symbol for an n-channel depletion mode MOSFET.


## 10.3.2 Current–Voltage Relationship—Concepts

Figure 10.37a shows an n-channel enhancement mode MOSFET with a gate-tosource voltage that is less than the threshold voltage and with only a very small drain-to-source voltage. The source and substrate, or body, terminals are held at ground potential. With this bias confi guration, there is no electron inversion layer, the drain-to-substrate pn junction is reverse biased, and the drain current is zero (disregarding pn junction leakage currents). 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/998ce20becf4f0d1fe75c29b006e1362183fbec4561abb56f6c285b43fe12b85.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/0736e0f5dfc67a16efffcf2e79c9244f2d5666273cc2720c4a4a7c033970de79.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ab9dcab42d8665330d742aecee57a716df17854d4b01670c53c1bc75fa42251e.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ce05eb21d8f5a3c3adeb6f11364801ecf93b81f64da2ab3d53db2560cbcb3d71.jpg)



Figure 10.36 | Cross section and circuit symbol for (a) a p-channel enhance ment mode MOSFET and (b) a p-channel depletion mode MOSFET.


Figure 10.37b shows the same MOSFET with an applied gate voltage such that $V _ { G S } > V _ { T } .$ An electron inversion layer has been created so that when a small drain voltage is applied, the electrons in the inversion layer will fl ow from the source to the positive drain terminal. The conventional current enters the drain terminal and leaves the source terminal. In this ideal case, there is no current through the oxide to the gate terminal. 

For small $V _ { D S }$ values, the channel region has the characteristics of a resistor, so we can write 

$$
I _ {D} = g _ {d} V _ {D S} \tag {10.41}
$$

where $g _ { d }$ is defi ned as the channel conductance in the limit as $V _ { D S }  0$ . The channel conductance is given by 

$$
g _ {d} = \frac {W}{L} \cdot \mu_ {n} \left| Q _ {n} ^ {\prime} \right| \tag {10.42}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/252f56f356ee586a6bd86b5b0c39d74884b553563257acf361efa6ee6c7b84b5.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d90355ebb599618056adc8366bbc1dd3dd460bdc598ce01f89f2506daa84f04f.jpg)



(b)



Figure 10.37 | The n-channel enhancement mode MOSFET (a) with an applied gate voltage $V _ { G S } < V _ { T }$ and (b) with an applied gate voltage $V _ { G S } > V _ { T }$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/8d6945c95b335cb81f96ebf486db10395520fd6220cf50c413d5557e99c2261c.jpg)



Figure 10.38 $I _ { D }$ versus $V _ { D S }$ charac teristics for small values of $V _ { D S }$ at three VGS voltages.


where $\mu _ { n }$ is the mobility of the electrons in the inversion layer and $\left| Q _ { n } ^ { \prime } \right|$ is the magnitude of the inversion layer charge per unit area. The inversion layer charge is a function of the gate voltage; thus, the basic MOS transistor action is the modulation of the channel conductance by the gate voltage. The channel conductance, in turn, determines the drain current. We will initially assume that the mobility is a constant; we will discuss mobility effects and variations in the next chapter. 

The $I _ { D }$ versus $V _ { D S }$ characteristics, for small values of $V _ { D S } ,$ are shown in Figure 10.38. When $V _ { G S } < V _ { T } ,$ the drain current is zero. As $V _ { G S }$ becomes larger than $V _ { T } ,$ channel inversion charge density increases, which increases the channel conductance. A larger value of $g _ { d }$ produces a larger initial slope of the $I _ { D }$ versus $V _ { D S }$ characteristic as shown in the fi gure. 

Figure 10.39a shows the basic MOS structure for the case when $V _ { G S } > V _ { T }$ and the applied $V _ { D S }$ voltage is small. The thickness of the inversion channel layer in the fi gure qualitatively indicates the relative charge density, which is essentially constant along the entire channel length for this case. The corresponding $I _ { D }$ versus $V _ { D S }$ curve is shown in the fi gure. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/23a0599b09642fc4379ad0adfa462edd9c160fd2bd8faad58a7bcba3973c25f0.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/cc77b5102e876ab510fa6429adbd845427888b1b4c406e3518081e17cb6f31b6.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/be876a22b2569292fd90301afd54cf92330334d72afb93e2c9a41ac1242824e2.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/3475befcb4bcf805eadb7e6525065d513007411abcf3383fb801d0aed016579c.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/1ca6d6813299abdf5e78e4c59bf5e3b4f15a3e216b739ec34d05c6a6b9e2adf9.jpg)



(c)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b4e3ab52cee05c7811878b5d5800f80905bbfd50904981cff2dc3dbfd46e7be1.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ebadd341f78d01004d73b76d9d36c5e653d115f2f11bb30a5b4c718123158dc9.jpg)



(d)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/8f72c86424a62451bc223d1daaab090472fbcb48bb4a5ad9693bff0b76fb693b.jpg)



Figure 10.39 | Cross section and $I _ { D }$ versus $V _ { D S }$ curve when $\mathrm { V } _ { G S } < V _ { T }$ for (a) a small $V _ { D S }$ value, (b) a larger $V _ { D S }$ value, (c) a value of $V _ { D S } = V _ { D S } ( \mathrm { s a t ) }$ , and (d) a value of $V _ { D S } > V _ { D S } ( \mathrm { s a t ) }$ .


Figure 10.39b shows the situation when the $V _ { D S }$ value increases. As the drain voltage increases, the voltage drop across the oxide near the drain terminal decreases, which means that the induced inversion charge density near the drain also decreases. The incremental conductance of the channel at the drain decreases, which then means that the slope of the $I _ { D }$ versus $V _ { D S }$ curve will decrease. This effect is shown in the $I _ { D }$ versus $V _ { D S }$ curve in the fi gure. 

When $V _ { D S }$ increases to the point where the potential drop across the oxide at the drain terminal is equal to $V _ { T } ,$ the induced inversion charge density is zero at the drain terminal. This effect is schematically shown in Figure 10.39c. At this point, the incremental conductance at the drain is zero, which means that the slope of the $I _ { D }$ versus $V _ { D S }$ curve is zero. We can write 

$$
V _ {G S} - V _ {D S} (\mathrm{sat}) = V _ {T} \tag {10.43a}
$$

or 

$$
V _ {D S} (\text { sat }) = V _ {G S} - V _ {T} \tag {10.43b}
$$

where $V _ { D S } ( \mathrm { s a t } )$ is the drain-to-source voltage producing zero inversion charge density at the drain terminal. 

When $V _ { D S }$ becomes larger than the $V _ { D S } ( \mathrm { s a t } )$ value, the point in the channel at which the inversion charge is just zero moves toward the source terminal. In this case, electrons enter the channel at the source, travel through the channel toward the drain, and then, at the point where the charge goes to zero, the electrons are injected into the space charge region where they are swept by the E-fi eld to the drain contact. If we assume that the change in channel length $\Delta L$ is small compared to the original length $L ,$ then the drain current will be a constant for $V _ { D S } > V _ { D S } ( \mathrm { s a t ) }$ . The region of the $I _ { D }$ versus $V _ { D S }$ characteristic is referred to as the saturation region. Figure 10.39d shows this region of operation. 

When $V _ { G S }$ changes, the $I _ { D }$ versus $V _ { D S }$ curve will change. We saw that, if $V _ { G S }$ increases, the initial slope of $I _ { D }$ versus $V _ { D S }$ increases. We can also note from Equation (10.43b) that the value of $V _ { D S } ( \mathrm { s a t } )$ is a function of $V _ { G S }$ . We can generate the family of curves for this n-channel enhancement mode MOSFET as shown in Figure 10.40. 

Figure 10.41 shows an n-channel depletion mode MOSFET. If the n-channel region is actually an induced electron inversion layer created by the metal– semiconductor work function difference and fi xed charge in the oxide, the current–voltage characteristics are exactly the same as we have discussed, except that $V _ { T }$ is a negative quantity. We may also consider the case when the n-channel region is actually an n-type semiconductor region. In this type of device, a negative gate voltage will induce a space charge region under the oxide, reducing the thickness of the n-channel region. The reduced thickness decreases the channel conductance, which reduces the drain current. A positive gate voltage will create an electron accumulation layer, which increases the drain current. One basic requirement for this device is that the channel thickness $t _ { c }$ must be less than the maximum induced space charge width in order to be able to turn the device off. The general $I _ { D }$ versus $V _ { D S }$ family of curves for an n-channel depletion mode MOSFET is shown in Figure 10.42. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/43288489884a7dd0bff268c3d67aecb8b785a8eadc9a6c68d301d2c9677e34a0.jpg)



Figure 10.40 | Family of $I _ { D }$ versus $V _ { D S }$ curves for an n-channel enhancement mode MOSFET.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/929406e6463dc30cc7628acd7b214a0c3b0e940d882797cf01d6badb99a0c745.jpg)



Figure 10.41 | Cross section of an n-channel depletion mode MOSFET.


In the next section, we derive the ideal current–voltage relation for the n-channel MOSFET. In the nonsaturation region, we obtain 

$$
I _ {D} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] \tag {10.44a}
$$

which can be written as 

$$
I _ {D} = \frac {k _ {n} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] \tag {10.44b}
$$

or 

$$
I _ {D} = K _ {n} \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] \tag {10.44c}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/1ee1e8a8bbc055068bf23532ebb302d8fabda6cd165e74ce83148cd019402a56.jpg)



Figure 10.42 | Family of $I _ { D }$ versus $V _ { D S }$ curves for an n-channel depletion mode MOSFET.


The parameter $k _ { n } ^ { \prime } ~ = ~ \mu _ { n } C _ { o x }$ is called the process conduction parameter for the n-channel MOSFET and has units of $\mathbf { A } / \mathbf { V } ^ { 2 }$ . The parameter $K _ { n } = ( W \mu _ { n } C _ { o x } ) / 2 L =$ $( k _ { n } ^ { \prime } / 2 ) \cdot ( W / L )$ is called the conduction parameter for the n-channel MOSFET and also has units of $\mathrm { A } / \mathrm { V } ^ { 2 }$ . 

When the transistor is biased in the saturation region, the ideal currernt–voltage relation is given by 

$$
I _ {D} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} (V _ {G S} - V _ {T}) ^ {2} \tag {10.45a}
$$

which can be written as 

$$
I _ {D} = \frac {k _ {n} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot (V _ {G S} - V _ {T}) ^ {2} \tag {10.45b}
$$

or 

$$
I _ {D} = K _ {n} (V _ {G S} - V _ {T}) ^ {2} \tag {10.45c}
$$

In general, for a given technology, the process conduction parameter, $k _ { n } ^ { \prime } ,$ is a constant. From Equations (10.44b) and (10.45b), then, we see that the design of a MOSFET, in terms of current capability, is determined by the width-to-length parameter. 

The operation of a p-channel device is the same as that of the n-channel device, except the charge carrier is the hole and the conventional current direction and voltage polarities are reversed. 

## *10.3.3 Current–Voltage Relationship—Mathematical Derivation

In the previous section, we qualitatively discussed the current–voltage characteristics. In this section, we derive the mathematical relation between the drain current, the gate-to-source voltage, and the drain-to-source voltage. Figure 10.43 shows the geometry of the device that we use in this derivation. 

In this analysis, we make the following assumptions: 

1. The current in the channel is due to drift rather than diffusion. 

2. There is no current through the gate oxide. 

3. A gradual channel approximation is used in which $\partial \mathrm { E } _ { y } / \partial y \gg \partial \mathrm { E } _ { x } / \partial x$ . This approximation means that $\mathrm { E } _ { x }$ is essentially a constant. 

4. Any fi xed oxide charge is an equivalent charge density at the oxide– semiconductor interface. 

5. The carrier mobility in the channel is constant. 

We start the analysis with Ohm’s law, which can be written as 

$$
J _ {x} = \sigma \mathrm{E} _ {x} \tag {10.46}
$$

where  is the channel conductivity and $\mathrm { E } _ { x }$ is the electric fi eld along the channel created by the drain-to-source voltage. The channel conductivity is given by $\sigma = e \mu _ { n } n ( y )$ , where $\mu _ { n }$ is the electron mobility and n(y) is the electron concentration in the inversion layer. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/47c0917a2200d15d312d0bb23a9c7bfabd8bb49222135949eac4b89e773502c8.jpg)



Figure 10.43 | Geometry of a MOSFET for $I _ { D }$ versus $V _ { D S }$ derivation.


The total channel current is found by integrating $J _ { x }$ over the cross-sectional area in the y and z directions. Then 

$$
I _ {x} = \int_ {y} \int_ {z} J _ {x} d y d z \tag {10.47}
$$

We may write that 

$$
Q _ {n} ^ {\prime} = - \int \mathrm{en} (y) d y \tag {10.48}
$$

where $Q _ { n } ^ { \prime }$ is the inversion layer charge per unit area and is a negative quantity for this case. 

Equation (10.47) then becomes 

$$
I _ {x} = - W \mu_ {n} Q _ {n} ^ {\prime} \mathrm{E} _ {x} \tag {10.49}
$$

where W is the channel width, the result of integrating over z. 

Two concepts we use in the currernt–voltage derivation are charge neutrality and Gauss’s law. Figure 10.44 shows the charge densities through the device for $V _ { G S } > V _ { T } .$ The charges are all given in terms of charge per unit area. Using the concept of charge neutrality, we can write 

$$
Q _ {m} ^ {\prime} + Q _ {s s} ^ {\prime} + Q _ {n} ^ {\prime} + Q _ {S D} ^ {\prime} (\max) = 0 \tag {10.50}
$$

The inversion layer charge and induced space charge are negative for this n- channel device. 

Gauss’s law can be written as 

$$
\oint_ {s} \epsilon \mathrm{E} _ {n} d S = Q _ {T} \tag {10.51}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/747a3ecff0c7802d500d8d837d5a156828fd8b2bcb157d39df5f870ae9bd8615.jpg)



Figure 10.44 | Charge distribution in the n-channel enhancement mode MOSFET for $V _ { G S } > V _ { T }$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/7e751c7698fc518d34a5843f36d08e93e42341ce67988ee2408171503be810e7.jpg)



Figure 10.45 | Geometry for applying Gauss’s law.


where the integral is over a closed surface. $Q _ { T }$ is the total charge enclosed by the surface, and $\textstyle \mathrm { E } _ { n }$ is the outward directed normal component of the electric fi eld crossing the surface S. Gauss’s law is applied to the surface defi ned in Figure 10.45. Since the surface must be enclosed, we must take into account the two end surfaces in the x-y plane. However, there is no z-component of the electric fi eld so these two end surfaces do not contribute to the integral of Equation (10.51). 

Now consider the surfaces labeled 1 and 2 in Figure 10.45. From the gradual channel approximation, we assume that $\mathrm { E } _ { x }$ is essentially a constant along the channel length. This assumption means that $\mathrm { E } _ { x }$ into surface 2 is the same as $\mathrm { E } _ { x }$ out of surface 1. Since the integral in Equation (10.51) involves the outward component of the E-fi eld, the contributions of surfaces 1 and 2 cancel each other. Surface 3 is in the neutral p region, so the electric fi eld is zero at this surface. 

Surface 4 is the only surface that contributes to Equation (10.51). Taking into account the direction of the electric fi eld in the oxide, Equation (10.51) becomes 

$$
\oint_ {s} \epsilon \mathrm{E} _ {n} d S = - \epsilon_ {\mathrm{ox}} \mathrm{E} _ {\mathrm{ox}} W d x = Q _ {T} \tag {10.52}
$$

where $\epsilon _ { \mathrm { o x } }$ is the permittivity of the oxide. The total charge enclosed is 

$$
Q _ {T} = [ Q _ {s s} ^ {\prime} + Q _ {n} ^ {\prime} + Q _ {S D} ^ {\prime} (\max) ] W d x \tag {10.53}
$$

Combining Equations (10.52) and (10.53), we have 

$$
- \epsilon_ {\mathrm{ox}} \mathrm{E} _ {\mathrm{ox}} = Q _ {s s} ^ {\prime} + Q _ {n} ^ {\prime} + Q _ {S D} ^ {\prime} (\max) \tag {10.54}
$$

We now need an expression for $\operatorname { E } _ { \mathrm { o x } } .$ . Figure 10.46a shows the oxide and channel. We assume that the source is at ground potential. The voltage $V _ { x }$ is the potential in the channel at a point x along the channel length. The potential difference across the oxide at x is a function of $V _ { G S } , V _ { x } ,$ and the metal–semiconductor work function difference. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d37a34b9a5a1bf9eab446f1deefe464f281e4fa63d3c6182d781401ae1f1e066.jpg)



Figure 10.46 | (a) Potentials at a point x along the channel. (b) Energy-band diagram through the MOS structure at the point x.


The energy-band diagram through the MOS structure at point x is shown in Figure 10.46b. The Fermi level in the p-type semiconductor is $E _ { F p }$ and the Fermi level in the metal is $E _ { F m } .$ . We have 

$$
E _ {F p} - E _ {F m} = e (V _ {G S} - V _ {x}) \tag {10.55}
$$

Considering the potential barriers, we can write 

$$
V _ {G S} - V _ {x} = (\phi_ {m} ^ {\prime} + V _ {\mathrm{ox}}) - \left(\chi^ {\prime} + \frac {E _ {g}}{2 e} - \phi_ {s} + \phi_ {f p}\right) \tag {10.56}
$$

which can also be written as 

$$
V _ {G S} - V _ {x} = V _ {\mathrm{ox}} + 2 \phi_ {f p} + \phi_ {m s} \tag {10.57}
$$

where $\phi _ { m s }$ is the metal–semiconductor work function difference, and $\phi _ { s } = 2 \phi _ { f p }$ for the inversion condition. 

The electric fi eld in the oxide is 

$$
\mathrm{E} _ {\mathrm{ox}} = \frac {V _ {\mathrm{ox}}}{t _ {\mathrm{ox}}} \tag {10.58}
$$

Combining Equations (10.54), (10.57), and (10.58), we fi nd that 

$$
\begin{array}{l} - \epsilon_ {\mathrm{ox}} \mathrm{E} _ {\mathrm{ox}} = \frac {- \epsilon_ {\mathrm{ox}}}{t _ {\mathrm{ox}}} [ (V _ {G S} - V _ {x}) - (\phi_ {m s} + 2 \phi_ {f p}) ] \\ = Q _ {s s} ^ {\prime} + Q _ {n} ^ {\prime} + Q _ {S D} ^ {\prime} (\max) \tag {10.59} \\ \end{array}
$$

The inversion charge density, $Q _ { n } ^ { \prime } ,$ , from Equation (10.59) can be substituted into Equation (10.49) and we obtain 

$$
I _ {x} = - W \mu_ {n} C _ {\mathrm{ox}} \frac {d V _ {x}}{d x} \left[ (V _ {G S} - V _ {x}) - V _ {T} \right] \tag {10.60}
$$

where $\mathrm { E } _ { x } = - d V _ { x } / d x$ and $V _ { T }$ is the threshold voltage defi ned by Equation (10.31b). 

We can now integrate Equation (10.60 ) over the length of the channel. We have 

$$
\int_ {0} ^ {L} I _ {x} d x = - W \mu_ {n} C _ {\mathrm{ox}} \int_ {V _ {x} (0)} ^ {V _ {x} (L)}: [ (V _ {G S} - V _ {T}) - V _ {x} ] d V _ {x} \tag {10.61}
$$

We are assuming a constant mobility $\mu _ { n } .$ . For the n-channel device, the drain current enters the drain terminal and is a constant along the entire channel length. Letting $I _ { D } = - I _ { x } ,$ Equation (10.61) becomes 

$$
I _ {D} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] \tag {10.62}
$$

Equation (10.62) is valid for $V _ { G S } \geq V _ { T }$ and for $0 \le V _ { D S } \le V _ { D S } ( \mathrm { s a t } )$ . 

Equation (10.62) can also be written as 

$$
I _ {D} = \frac {k _ {n} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] = K _ {n} \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} - V _ {D S} ^ {2} \right] \tag {10.63}
$$

where $k _ { n } ^ { \prime }$ is the process conduction parameter and $K _ { n }$ is the conduction parameter. These parameters are described and defi ned in Equations (10.44b) and (10.44c). 

Figure 10.47 shows plots of Equation (10.62) as a function of $V _ { D S }$ for several values of $V _ { G S } .$ . We can fi nd the value of $V _ { D S }$ at the peak current value from $\partial I _ { D } / \partial V _ { D S } = 0$ . Then, using Equation (10.62), the peak current occurs when 

$$
V _ {D S} = V _ {G S} - V _ {T} \tag {10.64}
$$

This value of $V _ { D S }$ is just $V _ { D S } ( \mathrm { s a t } )$ , the point at which saturation occurs. For $V _ { D S } > V _ { D S } ( \mathrm { s a t ) }$ , the ideal drain current is a constant and is equal to 

$$
I _ {D} (\mathrm{sat}) = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} \left[ 2 (V _ {G S} - V _ {T}) V _ {D S} (\mathrm{sat}) - V _ {D S} ^ {2} (\mathrm{sat}) \right] \tag {10.65}
$$

Using Equation (10.64) for $V _ { D S } ( \mathrm { s a t } )$ , Equation (10.65) becomes 

$$
I _ {D} (\text { sat }) = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} (V _ {G S} - V _ {T}) ^ {2} \tag {10.66}
$$

Equation (10.66) can also be written as 

$$
I _ {D} = \frac {k _ {n} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot (V _ {G S} - V _ {T}) ^ {2} = K _ {n} (V _ {G S} - V _ {T}) ^ {2} \tag {10.67}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/25dabcb9c9f97ba6081f730e0ab97ac26c20a26738b93c2ce2fabe148f340a23.jpg)



Figure 10.47 | Plots of $I _ { D }$ versus $V _ { D S }$ from Equation (10.62).


Equation (10.62) is the ideal current–voltage relationship of the n-channel MOSFET in the nonsaturation region for $0 \le V _ { D S } \le V _ { D S } ( \mathrm { s a t } )$ , and Equation (10.66) is the ideal current–voltage relationship of the n-channel MOSFET in the saturation region for $V _ { D S } \geq V _ { D S } ( \mathrm { s a t } )$ . These I–V expressions were explicitly derived for an n-channel enhancement mode device. However, these same equations apply to an n-channel depletion mode MOSFET in which the threshold voltage $V _ { T }$ is a negative quantity. 

Objective: Design the width of a MOSFET such that a specifi ed current is induced for a given applied bias. 

Consider an ideal n-channel MOSFET with parameters $L = 1 . 2 5 \mu \mathrm { m } , \mu _ { n } = 6 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } ,$ $C _ { \mathrm { o x } } = 6 . 9 \times 1 0 ^ { - 8 } \mathrm { F } / \mathrm { c m } ^ { 2 } .$ , and $V _ { T } = 0 . 6 5 \mathrm { ~ V ~ }$ . Design the channel width W such that $I _ { D } ( \mathrm { s a t } ) =$ 4 mA for $V _ { G S } = 5 \mathrm { V } .$ . 

## Solution

For the transition biased in the saturation region, we have, from Equation (10.66), 

$$
I _ {D} (\text { sat }) = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L} (V _ {G S} - V _ {T}) ^ {2}
$$

or 

$$
4 \times 1 0 ^ {- 3} = \frac {W (6 5 0) (6 . 9 \times 1 0 ^ {- 8})}{2 (1 . 2 5 \times 1 0 ^ {- 4})} \cdot (5 - 0. 6 5) ^ {2} = 3. 3 9 W
$$

Then 

$$
W = 1 1. 8 \mu \mathrm{m}
$$

## ■ Comment

The current capability of a MOSFET is directly proportional to the channel width W. The current handling capability can be increased by increasing W. 

## ■ EXERCISE PROBLEM

Ex 10.7 The parameters of an n-channel silicon MOSFET are $\mu _ { n } = 6 5 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } , t _ { o x } = 8$ nm  80 Å, WL  12, and $V _ { T } = 0 . 4 0 \mathrm { V }$ . If the transistor is biased in the saturation region, fi nd the drain current for (a) $V _ { G S } = 0 . 8 \mathrm { V } , ( b ) V _ { G S } = 1 . 2 \mathrm { V } ,$ , and $( c ) \ V _ { G S }$  1.6 V. ) 2.423 mA] c ) 1.077 mA; ( b ) 0.269 mA; ( a [Ans. ( 

We can use the I–V relations to experimentally determine the mobility and threshold voltage parameters. From Equation (10.62), we can write, for very small values of $V _ { D S }$ , 

$$
I _ {D} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} (V _ {G S} - V _ {T}) V _ {D S} \tag {10.68}
$$

Figure 10.48a shows a plot of Equation (10.68) as a function of $V _ { G S }$ for constant $V _ { D S } .$ A straight line is fi tted through the points. The deviation from the straight line at low values of $V _ { G S }$ is due to subthreshold conduction and the deviation at higher values of $V _ { G S }$ is due to mobility being a function of gate voltage. Both of these effects will be considered in the next chapter. The extrapolation of the straight line to zero current gives the threshold voltage, and the slope is proportional to the inversion carrier mobility. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/444db0891c325e7831fcf0dad21cc28d80dd7f7197458855352d49d6f00be048.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/6b325a2d5f1e56657ee186a5571e9ac5aac4c1b552efa61a32b7318dedcb62eb.jpg)



Figure 10.48 | (a)__ $I _ { D }$ versus $V _ { G S }$ (for small $V _ { D S } )$ for enhancement mode MOSFET. (b) Ideal $\sqrt { I _ { D } }$ versus $V _ { G S }$ in saturation region for enhancement mode (curve A) and depletion mode (curve B) n-channel MOSFETs.


Now consider the case when the transistor is biased in the saturation region. If we take the square root of Equation (10.66), we obtain 

$$
\sqrt {I _ {D} (\mathrm{sat})} = \sqrt {\frac {W \mu_ {n} C _ {\mathrm{ox}}}{2 L}} (V _ {G S} - V _ {T}) \tag {10.69}
$$

Figure 10.48b is a plot of Equation (10.69). In the ideal case, we can obtain the same information from both curves. However, as we will see in the next chapter, the threshold voltage may be a function of $V _ { D S }$ in short-channel devices. Since Equation (10.69) applies to devices biased in the saturation region, the $V _ { T }$ parameter in this equation may differ from the extrapolated value determined in Figure 10.48a. In general, the nonsaturation current–voltage characteristics will produce the more reliable data. 

EXAMPLE 10.8 

Objective: Determine the inversion carrier mobility from experimental results. 

Consider an n-channel MOSFET with $W = 1 5 \mu \mathrm { m } , L = 2 \mu \mathrm { m } .$ , and $C _ { \mathrm { o x } } = 6 . 9 \times 1 0 ^ { - 8 } \mathrm { F } / \mathrm { c m } ^ { 2 }$ . Assume that the drain current in the nonsaturation region for $V _ { D S } = 0 . 1 0 \mathrm { ~ V ~ }$ is $I _ { D } = 3 5 \ \mu \mathrm { A }$ at $V _ { G S } = 1 . 5 \ : \mathrm { V }$ and $I _ { D } = 7 5 \mu \mathrm { A }$ at $V _ { G S } = 2 . 5 \ : \mathrm { V }$ . 

## Solution

From Equation (10.68), we can write 

$$
I _ {D 2} - I _ {D 1} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} (V _ {G S 2} - V _ {G S 1}) V _ {D S}
$$

so that 

$$
7 5 \times 1 0 ^ {- 6} - 3 5 \times 1 0 ^ {- 6} = \left(\frac {1 5}{2}\right) \mu_ {n} (6. 9 \times 1 0 ^ {- 8}) (2. 5 - 1. 5) (0. 1 0)
$$

which yields 

$$
\mu_ {n} = 7 7 3 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}
$$

We can then determine 

$$
V _ {T} = 0. 6 2 5 \mathrm{V}
$$

## ■ Comment

The mobility of carriers in the inversion layer is less than that in the bulk semiconductor due to the surface scattering effect. We will discuss this effect in the next chapter. 

## ■ EXERCISE PROBLEM

Ex 10.8 An n-channel silicon MOSFET has the following parameters: $W = 6 \mu \mathrm { m } , L =$ 1.5 m, and $t _ { o x } = 8 \mathrm { n m } = 8 0 \mathring \mathrm { A }$ . When the transistor is biased in the saturation region, the drain current is $I _ { D } ( s a t ) = 0 . 1 3 2 \mathrm { m A }$ at $V _ { G S } = 1 . 0 \ : \mathrm { V }$ and $I _ { D } ( s a t ) = 0 . 2 9 5 \mathrm { m A }$ at $V _ { G S } = 1 . 2 5 \ : \mathrm { V }$ . Determine the electron mobility and the threshold voltage. 

$$
(\text { Ans. } \mu_ {n} \approx 6 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s}, \mathrm{V} _ {T} = 0. 4 9 5 \mathrm{V})
$$

The current–voltage relationship of a p-channel device can be obtained by the same type of analysis. Figure 10.49 shows a p-channel enhancement mode MOSFET. The voltage polarities and current direction are the reverse of those in the n-channel device. We may note the change in the subscript notation for this device. For the current direction shown in the fi gure, the I–V relation for the p-channel MOSFET biased in the nonsaturation region is 

$$
I _ {D} = \frac {W \mu_ {p} C _ {\mathrm{ox}}}{2 L} \left[ 2 (V _ {S G} + V _ {T}) V _ {S D} - V _ {S D} ^ {2} \right] \tag {10.70}
$$

Equation (10.70) is valid for $0 \le V _ { S D } \le V _ { S D } ( s a t )$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b35d6f985fb40baa3aeb1328bb8bf202f78f2a0c757ce409f18c5b90f513fead.jpg)



Figure 10.49 | Cross section and bias confi guration for a p-channel enhancement mode MOSFET.


Equation (10.70) can also be written as 

$$
I _ {D} = \frac {k _ {p} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot \left[ 2 (V _ {S G} + V _ {T}) V _ {S D} - V _ {S D} ^ {2} \right] = K _ {p} \left[ 2 (V _ {S G} + V _ {T}) V _ {S D} - V _ {S D} ^ {2} \right] \tag {10.71}
$$

where $k _ { p } ^ { \prime } = \mu _ { p } C _ { o x }$ is the process conduction parameter for the p-channel MOSFET and $K _ { p } \stackrel { . } { = } ( W \mu _ { p } C _ { o x } ) / ( 2 L ) = ( k _ { p } ^ { \prime } / 2 ) \cdot ( W / L )$ is the conduction parameter. 

When the transistor is biased in the saturation region, the I–V relation is given by 

$$
I _ {D} (\text { sat }) = \frac {W \mu_ {p} C _ {\mathrm{ox}}}{2 L} (V _ {S G} + V _ {T}) ^ {2} \tag {10.72}
$$

Equation (10.72) is valid for $V _ { S D } \geq V _ { S D }$ (sat). 

Equation (10.72) can also be written as 

$$
I _ {D} = \frac {k _ {p} ^ {\prime}}{2} \cdot \frac {W}{L} \cdot (V _ {S G} + V _ {T}) ^ {2} = K _ {p} (V _ {S G} + V _ {T}) ^ {2} \tag {10.73}
$$

The source-to-drain saturation voltage is given by 

$$
V _ {S D} (s a t) = V _ {S G} + V _ {T} \tag {10.74}
$$

Note the change in the sign in front of $V _ { T }$ and note that the mobility is now the mobility of the holes in the hole inversion layer charge. Keep in mind that $V _ { T }$ is negative for a p-channel enhancement mode MOSFET and positive for a depletion mode p-channel device. 

One assumption we made in the derivation of the currernt–voltage relationship was that the charge neutrality condition given by Equation (10.50) was valid over the entire length of the channel. We implicitly assumed that $Q _ { S D } ^ { \prime } ( \mathrm { m a x } )$ was constant along the length of the channel. The space charge width, however, varies between source and drain due to the drain-to-source voltage; it is widest at the drain when $V _ { D S } > 0 . \mathrm { { A } }$ change in the space charge density along the channel length must be balanced by a corresponding change in the inversion layer charge. An increase in the space charge width means that the inversion layer charge is reduced, implying that the drain current and drain-to-source saturation voltage are less than the ideal values. The actual saturation drain current may be as much as 20 percent less than the predicted value due to this bulk charge effect. 

## 10.3.4 Transconductance

The MOSFET transconductance is defi ned as the change in drain current with respect to the corresponding change in gate voltage, or 

$$
g _ {m} = \frac {\partial I _ {D}}{\partial V _ {G S}} \tag {10.75}
$$

The transconductance is sometimes referred to as the transistor gain. 

If we consider an n-channel MOSFET operating in the nonsaturation region, then using Equation (10.62), we have 

$$
g _ {m L} = \frac {\partial I _ {D}}{\partial V _ {G S}} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} \cdot V _ {D S} \tag {10.76}
$$

The transconductance increases linearly with $V _ { D S }$ but is independent of $V _ { G S }$ in the nonsaturation region. 

The I–V characteristics of an n-channel MOSFET in the saturation region are given by Equation (10.66). The transconductance in this region of operation is given by 

$$
g _ {m s} = \frac {\partial I _ {D} (\mathrm{sat})}{\partial V _ {G S}} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} (V _ {G S} - V _ {T}) \tag {10.77}
$$

In the saturation region, the transconductance is a linear function of $V _ { G S }$ and is independent of $V _ { D S }$ . 

The transconductance is a function of the geometry of the device as well as of carrier mobility and threshold voltage. The transconductance increases as the width of the device increases, and it also increases as the channel length and oxide thickness decrease. In the design of MOSFET circuits, the size of the transistor, in particular the channel width $W ,$ is an important engineering design parameter. 

## 10.3.5 Substrate Bias Effects

In all of our analyses so far, the substrate, or body, has been connected to the source and held at ground potential. In MOSFET circuits, the source and body may not be at the same potential. Figure 10.50a shows an n-channel MOSFET and the associated double-subscripted voltage variables. The source-to-substrate pn junction must always be zero or reverse biased, so $V _ { S B }$ must always be greater than or equal to zero. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/23f513e3de660463b1c453feefb1c3da140d4125be137c65904092acf32618bd.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d70daa41ff5ae8104fca77f8779c10767f5cb4b5369114b76f9237f987322fd6.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/8179e79440b3256768cafe8a24a4b55fd5dc4c11cef0223245c87c3291637434.jpg)



Figure 10.50 | (a) Applied voltages on an n-channel MOSFET. (b) Energy-band diagram at inversion point when $V _ { S B } = 0 .$ (c) Energy-band diagram at inversion point when $V _ { S B } > 0$ is applied.


If $V _ { S B } = 0$ , threshold is defi ned as the condition when $\phi _ { s } = 2 \phi _ { f p }$ as we discussed previously and as shown in Figure 10.50b. When $V _ { S B } > 0$ the surface will still try to invert when $\phi _ { s } = 2 \phi _ { f p } .$ . However, these electrons are at a higher potential energy than are the electrons in the source. The newly created electrons will move laterally and fl ow out of the source terminal. When $\phi _ { s } = 2 \phi _ { f p } + V _ { S B } .$ , the surface reaches an equilibrium inversion condition. The energy-band diagram for this condition is shown in Figure 10.50c. The curve represented as $E _ { F n }$ is the Fermi level from the p substrate through the reverse-biased source–substrate junction to the source contact. 

The space charge region width under the oxide increases from the original $x _ { d T }$ value when a reverse-biased source–substrate junction voltage is applied. With an applied $V _ { S B } > 0$ , there is more charge associated with this region. Considering the charge neutrality condition through the MOS structure, the positive charge on the top metal gate must increase to compensate for the increased negative space charge in order to reach the threshold inversion point. So when $V _ { S B } > 0$ , the threshold voltage of the n-channel MOSFET increases. 

When $V _ { S B } = 0$ , we had 

$$
Q _ {S D} ^ {\prime} (\max) = - e N _ {a} x _ {d T} = - \sqrt {2 e \epsilon_ {s} N _ {a} (2 \phi_ {f p})} \tag {10.78}
$$

When $V _ { S B } > 0$ , the space charge width increases and we now have 

$$
Q _ {S D} ^ {\prime} = - e N _ {a} x _ {d} = - \sqrt {2 e \epsilon_ {s} N _ {a} (2 \phi_ {f p} + V _ {S B})} \tag {10.79}
$$

The change in the space charge density is then 

$$
\Delta Q _ {S D} ^ {\prime} = - \sqrt {2 e \epsilon_ {s} N _ {a}} \left[ \sqrt {2 \phi_ {f p} + V _ {S B}} - \sqrt {2 \phi_ {f p}} \right] \tag {10.80}
$$

To reach the threshold condition, the applied gate voltage must be increased. The change in threshold voltage can be written as 

$$
\Delta V _ {T} = - \frac {\Delta Q _ {S D} ^ {\prime}}{C _ {\mathrm{ox}}} = \frac {\sqrt {2 e \epsilon_ {s} N _ {a}}}{C _ {\mathrm{ox}}} \left[ \sqrt {2 \phi_ {f p} + V _ {S B}} - \sqrt {2 \phi_ {f p}} \right] \tag {10.81}
$$

where $\Delta V _ { T } = V _ { T } ( V _ { S B } > 0 ) - V _ { T } ( V _ { S B } = 0 )$ . We may note that $V _ { S B }$ must always be positive so that, for the n-channel device, $\Delta V _ { T }$ is always positive. The threshold voltage of the n-channel MOSFET will increase as a function of the source–substrate junction voltage. 

From Equation (10.81), we may defi ne 

$$
\gamma = \frac {\sqrt {2 e \epsilon_ {s} N _ {a}}}{C _ {o x}} \tag {10.82}
$$

where $\gamma$ is defi ned as the body-effect coeffi cient. Equation (10.81) may then be written as 

$$
\Delta V _ {T} = \gamma \left[ \sqrt {2 \phi_ {f p} + V _ {S B}} - \sqrt {2 \phi_ {f p}} \right] \tag {10.83}
$$

Objective: Calculate the body-effect coeffi cient and the change in the threshold voltage due to an applied source-to-body voltage. 

Consider an n-channel silicon MOSFET at $T ~ = ~ 3 0 0 ~ \mathrm { ~ K ~ }$ . Assume the substrate is doped to $N _ { a } = 3 \times 1 0 ^ { 1 6 } ~ \mathrm { c m } ^ { - 3 }$ and assume the oxide is silicon dioxide with a thickness of $t _ { o x } = 2 0 \ : \mathrm { n m } = 2 0 0 \mathrm { \AA } . \mathrm { L e t } \ : V _ { S B } = 1 \ : \mathrm { V } .$ . 

EXAMPLE 10.9 

## Solution

We can calculate that 

$$
\phi_ {f p} = V _ {t} \ln \left(\frac {N _ {a}}{n _ {i}}\right) = (0. 0 2 5 9) \ln \left(\frac {3 \times 1 0 ^ {1 6}}{1 . 5 \times 1 0 ^ {1 0}}\right) = 0. 3 7 5 8 \mathrm{V}
$$

and 

$$
C _ {o x} = \frac {\epsilon_ {o x}}{t _ {o x}} = \frac {(3 . 9) (8 . 8 5 \times 1 0 ^ {- 1 4})}{2 0 0 \times 1 0 ^ {- 8}} = 1. 7 2 6 \times 1 0 ^ {- 7} \mathrm {F / cm^ {2}}
$$

From Equation (10.82), we fi nd the body-effect coeffi cient to be 

$$
\gamma = \frac {\sqrt {2 e \epsilon_ {s} N _ {a}}}{C _ {o x}} = \frac {[ 2 (1 . 6 \times 1 0 ^ {- 1 9}) (1 1 . 7) (8 . 8 5 \times 1 0 ^ {- 1 4}) (3 \times 1 0 ^ {1 6}) ] ^ {1 / 2}}{1 . 7 2 6 \times 1 0 ^ {- 7}}
$$

or 

$$
\gamma = 0. 5 7 7 6 \mathrm{V} ^ {1 / 2}
$$

The change in threshold voltage for $V _ { S B } = 1 \mathrm { ~ V ~ }$ is found to be 

$$
\begin{array}{l} \Delta V _ {T} = \gamma \left[ \sqrt {2 \phi_ {f p} + V _ {S B}} - \sqrt {2 \phi_ {f p}} \right] \\ = (0. 5 7 7 6) \left[ \sqrt {2 (0 . 3 7 5 8) + 1} - \sqrt {2 (0 . 3 7 5 8)} \right] \\ = (0. 5 7 7 6) [ 1. 3 2 3 5 - 0. 8 6 6 9 ] = 0. 2 6 4 \mathrm{V} \\ \end{array}
$$

## ■ Comment

Figure 10.51 shows plots of $\sqrt { I _ { D } ( s a t ) }$ versus $V _ { G S }$ for various applied values of $V _ { S B } .$ The original threshold voltage is assumed to be $V _ { T O } = 0 . 6 4 \ : \mathrm { V } .$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ebb652913af8e811360f660fd7be24f8e5edf947a5cd5c14db2d1a1a85c3274a.jpg)



Figure 10.51 | Plots of $\sqrt { I _ { D } }$ versus $V _ { G S }$ at several values of $V _ { S B }$ for an n-channel MOSFET.


## EXERCISE PROBLEM

Ex 10.9 A silicon MOSFET has the following parameters: $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and 

$t _ { o x } = 1 2 \mathrm { n m } = 1 2 0 \mathring \mathrm { A }$ . Calculate (a) the body-effect coeffi cient and (b) the change in threshold voltage for (i) $V _ { S B } = 1$ and (ii) $V _ { S B } = 2 \mathrm { V } .$ . 

$$
[ \Lambda \mathrm{I} 2 \mathrm{I} = \nabla (\eta) \wedge \nabla (\eta) (b) ^ {\prime}; (\eta) \Delta V _ {T} = 0. 0 9 3 7 \mathrm{V}, (\eta) \Delta V _ {T} = 0. 1 6 2 \mathrm{V} ] [ \text { Ans. } (a) y = 0. 2 0 0 \mathrm{V} ^ {1 / 2}; (b) (\eta) \Delta V _ {T} = 0. 0 9 3 7 \mathrm{V}, (\eta) \Delta V _ {T} = 0. 1 6 2 \mathrm{V} ]
$$

If a body or substrate bias is applied to a p-channel device, the threshold voltage is shifted to more negative values. Because the threshold voltage of a p-channel enhancement mode MOSFET is negative, a body voltage will increase the applied negative gate voltage required to create inversion. The same general observation was made for the n-channel MOSFET. 

## TEST YOUR UNDERSTANDING

TYU 10.6 The silicon n-channel MOSFET described in Exercise Problem Ex 10.7 is to be redesigned by changing the $W / L$ ratio such that $I _ { D } = 1 0 0 \mu \mathrm { A }$ when the transistor is biased in the saturation regin with $V _ { G S } = 1 . 0 ~ \mathrm { V } .$ . 

$$
(\text { Ans. } W / L = 1. 9 8)
$$

TYU 10.7 The parameters of a p-channel MOSFET are $\mu _ { p } = 3 1 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { \cdot } \mathrm { s } , t _ { \mathrm { o x } } = 2 2 0 \mathring \mathrm { A } ,$ $W / L = 6 0 ;$ , and $V _ { T } = - 0 . 4 0 \mathrm { V } .$ . If the transistor is biased in the saturation region, fi nd the drain current for $V _ { S G } = 1 , 1 . 5$ , and 2 V. 

$$
(\text { Ans. } I _ {b} = 0. 5 2 6, 1. 7 7 \text { and } 3. 7 4 \text { mA })
$$

TYU 10.8 The p-channel MOSFET in TYU 10.7 is to be redesigned by changing the $( W / L )$ ratio such that $I _ { D } = 2 0 0 \mu \mathrm { A }$ when the transistor is biased in the saturation region with $V _ { S G } = 1 . 2 5 \ : \mathrm { V } .$ . 

$$
(\text { Ans. } W / L = 1 1. 4)
$$

TYU 10.9 Repeat Exercise Problem Ex 10.9 for a substrate impurity doping concentration of $N _ { a } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

$$
[ \Lambda \mathrm{u} _ {\mathrm{s}} (a)   y = 0. 0 6 3 3   \mathrm{V} ^ {1 / 2}; (b)   (i)   \Delta V _ {T} = 0. 0 3 1 4   \mathrm{V}, (\ddot {n})   \Delta V _ {T} = 0. 0 5 3 6   \mathrm{V} ]
$$

## 10.4 | FREQUENCY LIMITATIONS

In many applications, the MOSFET is used in a linear amplifi er circuit. A small-signal equivalent circuit for the MOSFET is needed in order to mathematically analyze the electronic circuit. The equivalent circuit contains capacitances and resistances that introduce frequency effects. We initially develop a small-signal equivalent circuit and then discuss the physical factors that limit the frequency response of the MOSFET. A transistor cutoff frequency, which is a fi gure of merit, is then defi ned and an expression derived for this factor. 

## 10.4.1 Small-Signal Equivalent Circuit

The small-signal equivalent circuit of the MOSFET is constructed from the basic MOSFET geometry. A model based on the inherent capacitances and resistances within the transistor structure, along with elements that represent the basic device equations, is shown in Figure 10.52. One simplifying assumption we will make in the equivalent circuit is that the source and substrate are both tied to ground potential. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/b2d13439cc4314b1b73c3ed280b77ca0e30862502113823feb256d90d6c176a6.jpg)



Figure 10.52 | Inherent resistances and capacitances in the n-channel MOSFET structure.


Two of the capacitances connected to the gate are inherent in the device. These capacitances are $C _ { g s }$ and $C _ { g d } ,$ which represent the interaction between the gate and the channel charge near the source and drain terminals, respectively. The remaining two gate capacitances, $C _ { g s p }$ and $C _ { g d p } ,$ are parasitic or overlap capacitances. In real devices, the gate oxide will overlap the source and drain contacts because of tolerance or fabrication factors. As we will see, the drain overlap capacitance— $C _ { g d p } ,$ in particular—will lower the frequency response of the device. The parameter $C _ { d s }$ is the drain-to-substrate pn junction capacitance, and $r _ { s }$ and $r _ { d }$ are the series resistances associated with the source and drain terminals. The small-signal channel current is controlled by the internal gate-to-source voltage through the transconductance. 

The small-signal equivalent circuit for the n-channel common-source MOSFET is shown in Figure 10.53. The voltage $V _ { g s } ^ { \prime }$ is the internal gate-to-source voltage that controls the channel current. The parameters $C _ { g s T }$ and $C _ { g d T }$ are the total gate-to-source and total gate-to-drain capacitances. One parameter, $r _ { d s } ,$ shown in Figure 10.53, is not shown in Figure 10.52. This resistance is associated with the slope $I _ { D }$ versus $V _ { D S } .$ . In the ideal MOSFET biased in the saturation region, $I _ { D }$ is independent of $V _ { D S }$ so that $r _ { d s }$ would be infi nite. In short-channel-length devices, in particular, $r _ { d s }$ is fi nite because of channel length modulation, which we will consider in the next chapter. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/16d478fccf4aa8a14e40c036c2ae91d0e5cc02bf6ea76f5429f7496b78b70a45.jpg)



Figure 10.53 | Small-signal equivalent circuit of a commonsource n-channel MOSFET.


A simplifi ed small-signal equivalent circuit valid at low frequency is shown in Figure 10.54. The series resistances, $r _ { s }$ and $r _ { d } ,$ have been neglected, so the drain current is essentially only a function of the gate-to-source voltage through the transconductance. The input gate impedance is infi nite in this simplifi ed model. 

The source resistance $r _ { s }$ can have a signifi cant effect on the transistor characteristics. Figure 10.55 shows a simplifi ed, low-frequency equivalent circuit including $r _ { s }$ but neglecting $r _ { d s }$ . The drain current is given by 

$$
I _ {d} = g _ {m} V _ {g s} ^ {\prime} \tag {10.84}
$$

and the relation between $V _ { g s }$ and $V _ { g s } ^ { \prime }$ can be found from 

$$
V _ {g s} = V _ {g s} ^ {\prime} + (g _ {m} V _ {g s} ^ {\prime}) r _ {s} = (1 + g _ {m} r _ {s}) V _ {g s} ^ {\prime} \tag {10.85}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/00db23781000fc7d5a7722a6c12dd6fe68c65829a5dd1cc31a7d9f151a70ef7f.jpg)



Figure 10.54 | Simplifi ed, low-frequency small-signal equivalent circuit of a common-source n-channel MOSFET.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/487ec33899877f407f4d8eb3011e58920734fc2ef5f00f9c38924c906305e43b.jpg)



Figure 10.55 | Simplifi ed, lowfrequency small-signal equivalent circuit of common-source n-channel MOSFET including source resistance $r _ { s } .$


The drain current from Equation (10.84) can now be written as 

$$
I _ {d} = \left(\frac {g _ {m}}{1 + g _ {m} r _ {s}}\right) V _ {g s} = g _ {m} ^ {\prime} V _ {g s} \tag {10.86}
$$

The source resistance reduces the effective transconductance or transistor gain. 

The equivalent circuit of the p-channel MOSFET is exactly the same as that of the n-channel except that all voltage polarities and current directions are reversed. The same capacitances and resistances that are in the n-channel model apply to the p-channel model. 

## 10.4.2 Frequency Limitation Factors and Cutoff Frequency

There are two basic frequency limitation factors in the MOSFET. The fi rst factor is the channel transit time. If we assume that carriers are traveling at their saturation drift velocity $v _ { \mathrm { s a t } } .$ , then the transit time is $\tau _ { t } = L / v _ { \mathrm { s a t } }$ where L is the channel length. If $ { v _ { \mathrm { s a t } } } = 1 0 ^ { 7 }$ cm /s and $L = 1 \ \mu \mathrm { m }$ , then $\tau _ { t } = 1 0 \mathrm { p s }$ , which translates into a maximum frequency of 100 GHz. This frequency is much larger than the typical maximum frequency response of a MOSFET. The transit time of carriers through the channel is usually not the limiting factor in the frequency responses of MOSFETs. 

The second limiting factor is the gate or capacitance charging time. If we neglect $r _ { s } , \ r _ { d } , \ r _ { d s } ,$ and $C _ { d s } ,$ the resulting equivalent small-signal circuit is shown in Figure 10.56 where $R _ { L }$ is a load resistance. 

The input gate impedance in this equivalent circuit is no longer infi nite. Summing currents at the input gate node, we have 

$$
I _ {i} = j \omega C _ {g s T} V _ {g s} + j \omega C _ {g d T} (V _ {g s} - V _ {d}) \tag {10.87}
$$

where $I _ { i }$ is the input current. Likewise, summing currents at the output drain node, we have 

$$
\frac {V _ {d}}{R _ {L}} + g _ {m} V _ {g s} + j \omega C _ {g d T} (V _ {d} - V _ {g s}) = 0 \tag {10.88}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ee874a425695fa1013a2321d89616e8933e3e0d242f2d72241ef6e58bc285dfa.jpg)



Figure 10.56 | High-frequency smallsignal equivalent circuit of commonsource n-channel MOSFET.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/2bcb65bfd809ef792ede419fba6c06023234cb399701911ff8a780cbb6cf10c0.jpg)



Figure 10.57 | Small-signal equivalent circuit including Miller capacitance.


Combining Equations (10.87) and (10.88) to eliminate the voltage variable $V _ { d } ,$ we can determine the input current as 

$$
I _ {i} = j \omega \left[ C _ {g s T} + C _ {g d T} \left(\frac {1 + g _ {m} R _ {L}}{1 + j \omega R _ {L} C _ {g d T}}\right) \right] V _ {g s} \tag {10.89}
$$

Normally, $\omega R _ { L } C _ { g d T }$ is much less than unity; therefore, we may neglect the $( j \omega R _ { L } C _ { g d T } )$ term in the denominator. Equation (10.89) then simplifi es to 

$$
I _ {i} = j \omega [ C _ {g s T} + C _ {g d T} (1 + g _ {m} R _ {L}) ] V _ {g s} \tag {10.90}
$$

Figure 10.57 shows the equivalent circuit with the equivalent input impedance described by Equation (10.90). The parameter $C _ { M }$ is the Miller capacitance and is given by 

$$
C _ {M} = C _ {g d T} (1 + g _ {m} R _ {L}) \tag {10.91}
$$

The serious effect of the drain overlap capacitance now becomes apparent. When the transistor is operating in the saturation region, $C _ { g d }$ essentially becomes zero, but $C _ { g d p }$ is a constant. This parasitic capacitance is multiplied by the gain of the transistor and can become a signifi cant factor in the input impedance. 

The cutoff frequency $f _ { T }$ is defi ned to be the frequency at which the magnitude of the current gain of the device is unity, or when the magnitude of the input current $I _ { i }$ is equal to the ideal load current $I _ { d } .$ From Figure 10.57, we can see that 

$$
I _ {i} = j \omega (C _ {g s T} + C _ {M}) V _ {g s} \tag {10.92}
$$

and the ideal load current is 

$$
I _ {d} = g _ {m} V _ {g s} \tag {10.93}
$$

The magnitude of the current gain is then 

$$
\left| \frac {I _ {d}}{I _ {i}} \right| = \frac {g _ {m}}{2 \pi f (C _ {g s T} + C _ {M})} \tag {10.94}
$$

Setting the magnitude of the current gain equal to unity at the cutoff frequency, we fi nd 

$$
f _ {T} = \frac {g _ {m}}{2 \pi (C _ {g s T} + C _ {M})} = \frac {g _ {m}}{2 \pi C _ {G}} \tag {10.95}
$$

where $C _ { G }$ is the equivalent input gate capacitance. 

In the ideal MOSFET, the overlap or parasitic capacitances, $C _ { g s p }$ and $C _ { g d p } .$ are zero. Also, when the transistor is biased in the saturation region, $C _ { g d }$ approaches zero and $C _ { g s }$ is approximately $C _ { \mathrm { o x } } W L$ . The transconductance of the ideal MOSFET biased in the saturation region and assuming a constant mobility is given by Equation (10.77) as 

$$
g _ {m s} = \frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} (V _ {G S} - V _ {T})
$$

Then, for this ideal case, the cutoff frequency is 

$$
f _ {T} = \frac {g _ {m}}{2 \pi C _ {G}} = \frac {\frac {W \mu_ {n} C _ {\mathrm{ox}}}{L} (V _ {G S} - V _ {T})}{2 \pi (C _ {\mathrm{ox}} W L)} = \frac {\mu_ {n} (V _ {G S} - V _ {T})}{2 \pi L ^ {2}} \tag {10.96}
$$

Objective: Calculate the cutoff frequency of an ideal MOSFET with a constant mobility. 

Assume that the electron mobility in an n-channel device is $\mu _ { n } = 4 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ and that the channel length is $L = 4 \mu \mathrm { m }$ . Also assume that $V _ { T } = 1 \mathrm { ~ V ~ }$ and $V _ { G S } = 3 \mathrm { ~ V } .$ . 

EXAMPLE 10.10 

## Solution

From Equation (10.96), the cutoff frequency is 

$$
f _ {T} = \frac {\mu_ {n} (V _ {G S} - V _ {T})}{2 \pi L ^ {2}} = \frac {4 0 0 (3 - 1)}{2 \pi (4 \times 1 0 ^ {- 4}) ^ {2}} = 7 9 6 \mathrm{MHz}
$$

## ■ Comment

In an actual MOSFET, the effect of the parasitic capacitance will substantially reduce the cutoff frequency from that calculated in this example. 

## ■ EXERCISE PROBLEM

Ex 10.10 An n-channel silicon MOSFET has the following parameters: $\mu _ { n } = 4 2 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { - } \mathrm { s } ,$ , tox  18 nm  180 Å, L  1.2 m, W  24 m, and $V _ { T } = 0 . 4 \ : \mathrm { V }$ . The transistor is biased in the saturation region at $V _ { G S } = 1 . 5 \ : \mathrm { V }$ . Determine the cutoff frequency. 5.11 GHz)  Tf (Ans. 

## TEST YOUR UNDERSTANDING

TYU 10.10 Consider the n-channel MOSFET described in Exercise Problem Ex 10.10. The transistor is connected to an effective load resistance of $R _ { L } = 1 0 0 \mathrm { k } \Omega$ . Calculate the ratio of Miller capacitance $\mathrm { C } _ { M }$ to gate-to-drain capacitance $C _ { g d T } .$ (Ans. 178) 

## *10.5 | THE CMOS TECHNOLOGY

The primary objective of this book is to present the basic physics of semiconductor mate rials and devices without considering in detail the various fabrication processes; this important subject is left to other books. However, there is one MOS technology that is used extensively, for which the basic fabrication techniques must be considered in order to understand essential characteristics of these devices and circuits. The MOS technology we consider briefl y is the complementary MOS, or CMOS, process. 

We have considered the physics of both n-channel and p-channel enhancement mode MOSFETs. Both devices are used in a CMOS inverter, which is the basis of CMOS digital logic circuits. The dc power dissipation in a digital circuit can be reduced to very low levels by using a complementary p-channel and n-channel pair. 

It is necessary to form electrically isolated p- and n-substrate regions in an integrated circuit to accommodate the n- and p-channel transistors. The p-well process has been a commonly used technique for CMOS circuits. The process starts with a fairly low doped n-type silicon substrate in which the p-channel MOSFET will be fabricated. A diffused p region, called a p well, is formed in which the n-channel MOSFET will be fabricated. In most cases, the p-type substrate doping level must be larger than the n-type substrate doping level to obtain the desired threshold voltages. The larger p doping can easily compensate the initial n doping to form the p well. A simplifi ed cross section of the p-well CMOS structure is shown in Figure 10.58a. The notation FOX stands for fi eld oxide, which is a relatively thick oxide separating the devices. The FOX prevents either the n or p substrate from becoming inverted and helps maintain isolation between the two devices. In practice, additional processing steps must be included; for example, providing connections so that the p well and n substrate can be electrically connected to the appropriate voltages. The n substrate must always be at a higher potential than the p well; therefore, this pn junction will always be reverse biased. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ee6046156e885a5aa6ed3c8dc8e74a38f7655925254abfa29b3496b5ca703926.jpg)



n substrate


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/73a7615781454a1f30af4fd817fe5d5161396485761559d41689be47815e8d86.jpg)



p substrate



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e376e166e457dab864bd2be227707fdadc62a9bc75f6049f021b6e345d165402.jpg)



p or n substrate



Figure 10.58 | CMOS structures: (a) p well, (b) n well, and (c) twin well. (From Yang [22].)


With ion implantation now being extensively used for threshold voltage control, both the n-well CMOS process and twin-well CMOS process can be used. The n-well CMOS process, shown in Figure 10.58b, starts with an optimized p-type substrate that is used to form the n-channel MOSFETs. (The n-channel MOSFETs, in general, have superior characteristics, so this starting point should yield excellent n-channel devices.) The n well is then added, in which the p-channel devices are fabricated. The n-well doping can be controlled by ion implantation. 

The twin-well CMOS process, shown in Figure 10.58c, allows both the p-well and n-well regions to be optimally doped to control the threshold voltage and transconductance of each transistor. The twin-well process allows a higher packing density because of self-aligned channel stops. 

One major problem in CMOS circuits has been latch-up. Latch-up refers to a high-current, low-voltage condition that may occur in a four-layer pnpn structure. Figure 10.59a shows the circuit of a CMOS inverter and Figure 10.59b shows a simplifi ed integrated circuit layout of the inverter circuit. In the CMOS layout, $\mathfrak { p } ^ { + }$ source to n substrate to p well to $\mathrm { n ^ { + } }$ source forms such a four-layer structure. 

The equivalent circuit of this four-layer structure is shown in Figure 10.60. The silicon-controlled rectifi er action involves the interaction of the parasitic pnp and npn bipolar transistors. Bipolar transistors are discussed in Chapter 12. The npn transistor corresponds to the vertical $\mathrm { n ^ { + } }$ -source to p-well to n-substrate structure and the pnp transistor corresponds to the lateral p-well to n-substrate to $\mathfrak { p } ^ { + }$ -source structure. Under normal CMOS operation, both parasitic bipolar transistors are cut off. However, under certain conditions, avalanche breakdown may occur in the p-well to nsubstrate junction, driving both bipolar transistors into saturation. This high- current, low-voltage condition—latch-up—can sustain itself by positive feedback. The condition can prevent the CMOS circuit from operating and can also cause permanent damage and burnout of the circuit. 

Latch-up can be prevented if the product $\beta _ { n } \beta _ { p }$ is less than unity at all times, where $\beta _ { n }$ and $\beta _ { p }$ are the common-emitter current gains of the npn and pnp parasitic bipolar transistors, respectively. One method of preventing latch-up is to “kill” the minority carrier lifetime. Minority carrier lifetime degradation can be accomplished by gold doping or neutron irradiation, either of which introduces deep traps within the semiconductor. The deep traps increase the excess minority carrier recombination rate and reduce current gain. A second method of preventing latch-up is by using proper circuit layout techniques. If the two bipolar transistors can be effectively decoupled, then latch-up can be minimized or prevented. The two parasitic bipolar transistors can also be decoupled by using a different fabrication technology. The silicon-on-insulator technology, for example, allows the n-channel and the p-channel MOSFETs to be isolated from each other by an insulator. This isolation decouples the parasitic bipolar transistors. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/863154cd49659dac6b3f8abfb9f86007d9604e2363f4b995fa987c26714ace52.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/1ad83ad959812f0d5840be44f3ed100f559699c27cd11459391c32f8f753d7b8.jpg)



Figure 10.59 | (a) CMOS inverter circuit. (b) Simplifi ed integrated circuit cross section of CMOS inverter.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/7042413cf570605a41184af107e4e7f4de6d6509c22409bed69805904b940db0.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/d6b7f108fe3356b94dcbf3af79c8ec5ea49f0febdb591f13eda843f1f7e7222f.jpg)



Figure 10.60 | (a) The splitting of the basic pnpn structure. (b) The two-transistor equivalent circuit of the four-layered pnpn device.


## 10.6 | SUMMARY

■ The fundamental physics and characteristics of the metal-oxide–semiconductor fi eldeffect transistor (MOSFET) have been considered in this chapter. 

■ The heart of the MOSFET is the MOS capacitor. The energy bands in the semiconductor adjacent to the oxide–semiconductor interface bend, depending upon the voltage applied to the gate. 

■ An inversion layer of electrons can be created at the oxide–semiconductor surface in a p-type semiconductor by applying a suffi ciently positive gate voltage, and an inversion layer of holes can be created at the oxide–semiconductor surface in an n-type semiconductor by applying a suffi ciently negative gate voltage. 

The threshold voltage is the applied gate voltage required to reach the threshold inversion point. The fl at-band voltage was defi ned and discussed. 

■ The n-channel MOSFET, both enhancement mode and depletion mode, and the p-channel MOSFET, both enhancement mode and depletion mode, were described. 

■ The basic transistor action is the modulation of the current at the drain terminal by the gate-to-source voltage. 

■ The ideal MOSFET current–voltage relations were derived. 

■ The body-effect coeffi cient was defi ned and discussed. The expression for the shift in threshold voltage due to the body effect was derived. 

■ A small-signal equivalent circuit of the MOSFET was developed. 

■ Various physical factors in the MOSFET that affect the frequency limitations were discussed. An expression for the cutoff frequency was developed. 

■ The CMOS technology was briefl y considered. 

## GLOSSARY OF IMPORTANT TERMS

accumulation layer charge The induced charge directly under an oxide that is in excess of the thermal-equilibrium majority carrier concentration. 

channel conductance The ratio of drain current to drain-to-source voltage in the limit as $V _ { D S }  0 .$ 

channel conductance modulation The process whereby the channel conductance varies with gate-to-source voltage. 

CMOS Complementary MOS; the technology that uses both p- and n-channel devices in an electronic circuit fabricated in a single semiconductor chip. 

conduction parameter The multiplying coeffi cient of the voltage terms to obtain the MOSFET drain current. 

cutoff frequency The signal frequency at which the input ac gate current is equal to the output ac drain current. 

depletion mode MOSFET The type of MOSFET in which a gate voltage must be applied to turn the device off. 

enhancement mode MOSFET The type of MOSFET in which a gate voltage must be applied to turn the device on. 

equivalent fi xed oxide charge The effective fi xed charge in the oxide, $\boldsymbol { Q } _ { s s } ^ { \prime } ,$ directly adjacent to the oxide–semiconductor interface. 

fi eld-effect The phenomenon by which an electric fi eld perpendicular to the surface of a semiconductor can modulate the conductance. 

fl at-band voltage The gate voltage that must be applied to create the fl at-band condition in which there is no space charge region in the semiconductor under the oxide. 

interface states The allowed electronic energy states within the bandgap energy at the oxide–semiconductor interface. 

inversion layer charge The induced charge directly under the oxide, which is the opposite type compared with the semiconductor doping. 

inversion layer mobility The mobility of carriers in the inversion layer. 

metal–semiconductor work function difference The parameter $\phi _ { m s } ,$ , a function of the difference between the metal work function and semiconductor electron affi nity. 

oxide capacitance The ratio of oxide permittivity to oxide thickness, which is the capacitance per unit area, $C _ { \mathrm { o x } } .$ . 

process conduction parameter The product of carrier mobility and oxide capacitance. 

saturation The condition in which the inversion charge density is zero at the drain and the drain current is no longer a function of the drain-to-source voltage. 

strong inversion The condition in which the inversion charge density is larger than the magnitude of the semiconductor doping concentration. 

threshold inversion point The condition in which the inversion charge density is equal in magnitude to the semiconductor doping concentration. 

threshold voltage The gate voltage that must be applied to achieve the threshold inversion point. 

transconductance The ratio of an incremental change in drain current to the corresponding incremental change in gate voltage. 

weak inversion The condition in which the inversion charge density is less than the magnitude of the semiconductor doping concentration. 

## CHECKPOINT

After studying this chapter, the reader should have the ability to: 

■ Sketch the energy-band diagrams in the semiconductor of the MOS capacitor under various bias conditions. 

■ Describe the process by which an inversion layer of charge is created in a MOS capacitor. 

■ Discuss the reason the space charge width reaches a maximum value once the inversion layer is formed. 

■ Discuss what is meant by the metal–semiconductor work function difference and why this value is different between aluminum, n polysilicon, and $\mathfrak { p } ^ { + }$ polysilicon gates. 

■ Describe what is meant by fl at-band voltage. 

■ Defi ne threshold voltage. 

■ Sketch the C–V characteristics of a MOS capacitor with p-type and n-type semiconductor substrates under high-frequency and low-frequency conditions. 

■ Discuss the effects of fi xed trapped oxide charge and interface states on the C–V characteristics. 

■ Sketch the cross sections of n-channel and p-channel MOSFET structures. 

■ Explain the basic operation of the MOSFET. 

■ Discuss the I–V characteristics of the MOSFET when biased in the nonsaturation and saturation regions. 

■ Describe the substrate bias effects on the threshold voltage. 

■ Sketch the small-signal equivalent circuit, including capacitances, of the MOSFET, and explain the physical origin of each capacitance. 

■ Discuss the condition that defi nes the cutoff frequency of a MOSFET. 

■ Sketch the cross section of a CMOS structure. 

■ Discuss what is meant by latch-up in a CMOS structure. 

## REVIEW QUESTIONS

1. Sketch the energy-band diagrams in a MOS capacitor with an n-type substrate in accumulation, depletion, and inversion modes. 

2. Describe what is meant by an inversion layer of charge. Describe how an inversion layer of charge can be formed in a MOS capacitor with a p-type substrate. 

3. Why does the space charge region in the semiconductor of a MOS capacitor reach a maximum width once the inversion layer is formed? 

4. Defi ne surface potential. Does the surface potential change signifi cantly with gate voltage once threshold is reached? 

5. Sketch the energy-band diagram through a MOS structure with a p-type substrate and an $\mathrm { n ^ { + } }$ polysilicon gate under zero bias. 

6. Defi ne the fl at-band voltage. Sketch the energy-band diagram in a MOS capacitor at fl at band. 

7. Defi ne the threshold voltage. What is the surface potential at the threshold voltage? 

8. Sketch the C–V characteristics of a MOS capacitor with an n-type substrate under the low-frequency condition. How do the characteristics change for the high-frequency condition? 

9. Indicate the approximate capacitance at fl at band on the C–V characteristic of a MOS capacitor with a p-type substrate under the high-frequency condition. 

10. What is the effect on the C–V characteristics of a MOS capacitor with a p-type substrate if the amount of positive trapped oxide charge increases? 

11. Qualitatively sketch the inversion charge density in the channel region when the transistor is biased in the nonsaturation region. Repeat for the case when the transistor is biased in the saturation region. 

12. Defi ne $V _ { D S } ( \mathrm { s a t } )$ . 

13. Defi ne enhancement mode and depletion mode for both n-channel and p-channel devices. 

14. Sketch the charge distribution through a MOS capacitor with a p-type substrate when biased in the inversion mode. Write the charge neutrality equation. 

15. Discuss why the threshold voltage changes when a reverse-biased source-to-substrate voltage is applied to a MOSFET. 

## PROBLEMS

(Note: In the following problems, assume the semiconductor and oxide in the MOS system are silicon and silicon dioxide, respectively, and assume the temperature is $T = 3 0 0 \mathrm { ~ k ~ }$ K unless otherwise stated. Use Figure 10.16 to determine the metal–semiconductor work function difference.) 

## Section 10.1 The Two-Terminal MOS Structure

10.1 The dc charge distributions of four ideal MOS capacitors are shown in Figure P10.1. For each case: (a) Is the semiconductor n or p type? (b) Is the device biased in the accumulation, depletion, or inversion mode? (c) Draw the energyband diagram in the semiconductor region. 

10.2 (a) Calculate the maximum space charge width $x _ { d T }$ and the maximum space charge density $| Q _ { S D } ^ { \prime } ( \mathrm { { m a x } ) } |$ in a MOS capacitor with a p-type silicon substrate at $T = 3 0 0$ K for doping concentrations of ( $) N _ { a } = 7 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and $( i i ) N _ { a } = 3 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . (b) Repeat part (a) for $T = 3 5 0 \mathrm { K }$ . 

10.3 (a) Consider a MOS capacitor at $T = 3 0 0 \mathrm { K }$ with an n-type silicon substrate. Determine the silicon doping concentration such that $\big \vert Q _ { S D } ^ { \prime } ( \mathrm { m a x } ) \big \vert = 1 . 2 5 \times 1 0 ^ { - 8 } \mathrm { C } / \mathrm { c m } ^ { - 2 }$ . (b) What is the surface potential that results in the maximum space charge width? 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/3062d891d35e0cd0d08795fc256416fb443a7eb2e1663bbadaba2086d1102338.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/36e1c5f68eed975d0bacd09c0130b9ebf94ab338012e0487a73e7ab9eae460be.jpg)



(b)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/5621dfe631c5a51a0c99c1f9e1cecb9a69b47ed84912e8604608fa4a09649713.jpg)



(c)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/a86549fb88e808fa5cbafa6dde8932c52067e1862abfc8e2643a65a389040f5b.jpg)



Figure P10.1 | Figure for Problem 10.1.


10.4 Determine the metal–semiconductor work function difference $\phi _ { m s }$ in a MOS structure with p-type silicon for the case when the gate is (a) aluminum, (b) $\mathrm { n } ^ { - }$ polysilicon, and $( c ) { \mathfrak { p } } ^ { + }$ polysilicon. Let $N _ { a } = 6 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . 

10.5 The silicon impurity doping concentration in an aluminum–silicon dioxide-silicon MOS device is $N _ { a } = 4 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Using the parameters in Example 10.2, determine the metal–semiconductor work function difference $\phi _ { m s }$ . 

10.6 Consider a MOS capacitor with an n-type silicon substrate. A metal–semiconductor work function difference of $\phi _ { m s } = - 0 . 3 0 \ : \mathrm { V }$ is required. Determine the silicon doping concentration required to meet this specifi cation when the gate is $( a ) \mathrm { n } ^ { + } \mathrm { p o l y } -$ silicon, $( b ) { \mathfrak { p } } ^ { + }$ polysilicon, and (c) aluminum. If a particular gate cannot meet this specifi cation, explain why. 

10.7 (a) Consider the MOS capacitor described in Problem 10.5. For an oxide thickness of $t _ { o x } = 2 0 \mathrm { n m } = 2 0 0$ Å and an oxide charge of $Q _ { s s } ^ { \prime } = 5 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 } ,$ , calculate the fl at-band voltage. (b) Repeat part (a) for an oxide thickness of $t _ { o x } = 8 \mathrm { n m } = 8 0 \mathring \mathrm { A }$ . 

10.8 (a) Consider an $\mathrm { n ^ { + } }$ polysilicon–silicon dioxide–n-type silicon MOS structure. Let $N _ { d } = 4 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . Calculate the ideal fl at-band voltage for $t _ { o x } = 2 0 \mathrm { n m } = 2 0 0 \mathring \mathrm { \ A }$ . (b) Considering the results of part (a), determine the shift in fl at-band voltage for (i) $Q _ { s s } ^ { \prime } = 4 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ and (ii) $Q _ { s s } ^ { \prime } = 1 0 ^ { 1 1 } \mathrm { c m } ^ { - 2 }$ . (c) Repeat parts (a) and (b) for an oxide thickness of $t _ { o x } = 1 2 \mathrm { n m } = 1 2 0 \mathring \mathrm { A }$ . 

10.9 Consider an aluminum gate–silicon dioxide–p-type silicon MOS structure with $t _ { \mathrm { o x } } = 4 5 0 \mathrm { ~ \AA ~ }$ . The silicon doping is $N _ { a } = 2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and the fl at-band voltage is $V _ { F B } = - 1 . 0 \ : \mathrm { V } .$ Determine the fi xed oxide charge $Q _ { s s } ^ { \prime }$ . 

10.10 Consider a MOS device with a p-type silicon substrate with $N _ { a } = 2 \times 1 0 ^ { 1 6 }$ cm3. The oxide thickness is $t _ { o x } = 1 5 \mathrm { n m } = 1 5 0 \mathring \mathrm { A }$ and the equivalent oxide charge is $Q _ { s s } ^ { \prime } = 7 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . Calculate the threshold voltage for (a) an $\mathrm { n ^ { + } }$ polysilicon gate, $\left( b \right) \mathsf { a } \mathsf { p } ^ { + }$ polysilicon gate, and (c) an aluminum gate. 

10.11 Repeat Problem 10.10 for an n-type silicon substrate with a doping of $N _ { d } = 3 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 } .$ . 

10.12 A 400-Å oxide is grown on p-type silicon with $N _ { a } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The fl at-band voltage is 0.9 V. Calculate the surface potential at the threshold inversion point as well as the threshold voltage assuming negligible oxide charge. Also fi nd the maximum space charge width for this device. 

10.13 A MOS device with an aluminum gate is fabricated on a p-type silicon substrate. The oxide thickness is $t _ { o x } = 2 2 \mathrm { n m } = 2 2 0 \mathring \mathrm { A }$ and the trapped oxide charge is $Q _ { s s } ^ { \prime } = 4 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . The measured threshold voltage is $V _ { T } = + 0 . 4 5 \ : \mathrm { V } .$ Determine the p-type doping concentration. 

10.14 Consider a MOS device with the following parameters: $\mathrm { p } ^ { + }$ polysilicon gate, n-type silicon substrate, $t _ { o x } = 1 8 \mathrm { { n m } = 1 8 0 \mathring { A } }$ , and $Q _ { s s } ^ { \prime } = 4 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . Determine the silicon doping concentration such that the threshold voltage is in the range $- 0 . 3 5 \leq V _ { T P } \leq - 0 . 2 5 \mathrm { { V } } .$ 

10.15 Repeat Problem 10.13 for an n-type silicon substrate if the measured threshold voltage is $V _ { T } = - 0 . 9 7 5 \mathrm { V } .$ Determine the n-type doping concentration. 

10.16 An n polysilicon gate–silicon dioxide–silicon MOS capacitor has an oxide thickness of $t _ { o x } = 1 8 \mathrm { n m } = 1 8 0 \mathring \mathrm { A }$ and a doping of $N _ { a } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . The oxide charge density is $Q _ { s s } ^ { \prime } = 6 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . Calculate the (a) fl at-band voltage and (b) threshold voltage. 

10.17 An n-channel depletion mode MOSFET with an $\mathrm { n ^ { + } }$ polysilicon gate is shown in Figure 10.41. The n-channel doping is $N _ { d } = 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ and the oxide thickness is $t _ { \mathrm { o x } } = 5 0 0 \mathring { \mathrm { A } } .$ . The equivalent fi xed oxide charge is $Q _ { s s } ^ { \prime } = 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ . The n-channel thickness $t _ { c }$ is equal to the maximum induced space charge width. (Disregard the space charge region at the n-channel–p-substrate junction.) (a) Determine the channel thickness $t _ { c }$ and (b) calculate the threshold voltage. 

10.18 Consider a MOS capacitor with an $\mathrm { n ^ { + } }$ polysilicon gate and n-type silicon substrate. Assume $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and let $E _ { F } - E _ { c } = 0 . 2 \ : \mathrm { e V }$ in the $\mathrm { n ^ { + } }$ polysilicon. Assume the oxide has a thickness of $t _ { \mathrm { o x } } = 3 0 0 \mathring { \mathrm { A } }$ . Also assume that $\chi ^ { \prime } \left( \mathrm { p o l y s i l i c o n } \right) = \chi ^ { \prime }$ (singlecrystal silicon). (a) Sketch the energy-band diagrams (i) for $V _ { G } = 0$ and (ii) at fl at band. (b) Calculate the metal–semiconductor work function difference. (c) Calculate the threshold voltage for the ideal case of zero fi xed oxide charge and zero interface states. 

*10.19 The threshold voltage of an n-channel MOSFET is given by Equation (10.31a). Plot $V _ { T }$ versus temperature over the range $2 0 0 \le T \le 4 5 0 \mathrm { K }$ . Consider both an aluminum gate and an $\mathrm { n ^ { + } }$ polysilicon gate. Assume the work functions are independent of temperature and use device parameters similar to those in Example 10.4. 

*10.20 Plot the threshold voltage of an n-channel MOSFET versus p-type substrate doping concentration similar to Figure 10.21. Consider both $\mathrm { n ^ { + } }$ and $\mathfrak { p } ^ { + }$ polysilicon gates. Use reasonable device parameters. 

*10.21 Plot the threshold voltage of a p-channel MOSFET versus n-type substrate doping concentration similar to Figure 10.22. Consider both $\mathrm { n ^ { + } }$ and $\mathfrak { p } ^ { + }$ polysilicon gates. Use reasonable device parameters. 

10.22 Consider an NMOS device with the parameters given in Problem 10.12. Plot $V _ { T }$ versus $t _ { \mathrm { o x } }$ over the range $2 0 \leq t _ { \mathrm { o x } } \leq 5 0 0 \mathrm { ~ \AA ~ }$ . 

## Section 10.2 Capacitance–Voltage Characteristics

10.23 An ideal MOS capacitor with an $\mathrm { n ^ { + } }$ polysilicon gate has a silicon dioxide thickness of $t _ { o x } = 1 2 \mathrm { n m } = 1 2 0 \mathring \mathrm { A }$ on a p-type silicon substrate doped at $N _ { a } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ . Determine the capacitance $C _ { o x } , C _ { F B } ^ { \prime } , C _ { m i n } ^ { \prime } ,$ and $C ^ { \prime } ( \mathrm { i n v } )$ at $( a ) f = 1$ Hz and $( b ) f = 1 \mathrm { { M H z } } .$ (c) Determine $V _ { F B }$ and $V _ { T } , \left( d \right)$ Sketch $C ^ { \prime } / C _ { o x }$ versus $V _ { G }$ for parts (a) and (b). 

10.24 Repeat Problem 10.23 for an ideal MOS capacitor with a $\mathfrak { p } ^ { + }$ polysilicon gate and an n-type silicon substrate doped at $N _ { d } = 5 \times 1 0 ^ { 1 4 } \mathrm { c m } ^ { - 3 }$ . 

*10.25 Using superposition, show that the shift in the fl at-band voltage due to a fi xed charge distribution $\rho ( x )$ in the oxide is given by 

$$
\Delta V _ {F B} = - \frac {1}{C _ {\mathrm{ox}}} \int_ {0} ^ {t _ {\mathrm{ox}}} \frac {x \rho (x)}{t _ {\mathrm{ox}}} d x
$$

10.26 Using the results of Problem 10.25, calculate the shift in fl at-band voltage for $t _ { o x } = 2 0 \mathrm { n m } = 2 0 0 \mathring \mathrm { A }$ for the following oxide charge distributions: 

(a) $Q _ { s s } ^ { \prime } = 8 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ is entirely located at the oxide–semiconductor interface, (b) $Q _ { s s } ^ { \prime } = 8 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 }$ is uniformly distributed throughout the oxide, and (c) $Q _ { s s } ^ { \prime } = 8 \times 1 0 ^ { 1 0 }$ cm2 forms a triangular distribution with the peak at the oxide– semiconductor interface and is zero at the metal–oxide interface. 

10.27 An ideal MOS capacitor is fabricated by using intrinsic silicon and an $\mathrm { n ^ { + } }$ polysilicon gate. (a) Sketch the energy-band diagram through the MOS structure under fl at-band conditions. (b) Sketch the low-frequency $C { - } V$ characteristics from negative to positive gate voltage. 

10.28 Consider a MOS capacitor with a p-type substrate. Assume that donor-type interface traps exist only at midgap (i.e., at $E _ { F i } )$ . Sketch the high-frequency $C { - } V$ curve from accumulation to inversion. Compare this sketch to the ideal C–V plot. 

10.29 Consider an SOS capacitor as shown in Figure P10.29. Assume the $\mathrm { S i O } _ { 2 }$ is ideal (no trapped charge) and has a thickness of $t _ { \mathrm { o x } } = 5 0 0 \mathrm { \AA }$ . The doping concentrations are $N _ { d } = 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ and $N _ { a } = 1 0 ^ { 1 6 } \thinspace { \mathrm { c m } } ^ { - 3 } . \thinspace ( a )$ Sketch the energy-band diagram through the device for (i) fl at band, (ii) $V _ { G } = + 3 \mathrm { V } ,$ and (iii) $V _ { G } = - 3 \mathrm { V } .$ (b) Calculate the fl at-band voltage. (c) Estimate the voltage across the oxide for (i) $V _ { G } = + 3 \mathrm { ~ V ~ }$ and (ii) $V _ { G } = - 3 \mathrm { ~ V } .$ (d) Sketch the high-frequency C–V characteristic curve. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ab72008f58a48b01378457bff4ff958cd4b34b64c8f7cbf2ddb1cf2b44c36321.jpg)



Figure P10.29 | Figure for Problem 10.29.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/e562345211c2c293d76110d58df8a35fedac03e3ea991827003ee286bccec905.jpg)



Figure P10.30 | Figure for Problem 10.30.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/ce3571fd1ca6aba4f755dd2ada0580b334180f512c40d8359cf43fc8de0773b8.jpg)



Figure P10.31 | Figure for Problem 10.31.


10.30 The high-frequency C–V characteristic curve of a MOS capacitor is shown in Figure P10.30. The area of the device is $2 \times 1 0 ^ { - 3 } \mathrm { c m } ^ { 2 } .$ . The metal–semiconductor work function difference is $\phi _ { m s } = - 0 . 5 0 \mathrm { V } ,$ , the oxide is $\mathrm { S i O } _ { 2 } ,$ the semiconductor is silicon, and the semiconductor doping concentration is $2 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 } . ( a )$ Is the semiconductor n or p type? (b) What is the oxide thickness? (c) What is the equivalent trapped oxide charge density? (d) Determine the fl at-band capacitance. 

10.31 Consider the high-frequency C–V plot shown in Figure P10.31. (a) Indicate which points correspond to fl at-band, inversion, accumulation, threshold, and depletion modes. (b) Sketch the energy-band diagram in the semiconductor for each condition. 

## Section 10.3 The Basic MOSFET Operation

10.32 An expression that includes the inversion charge density is given by Equation (10.59). Consider the defi nition of threshold voltage and show that the inversion charge density goes to zero at the drain terminal at saturation. (Hint: Let $V _ { x } = V _ { D S } = V _ { D S } ( \mathrm { s a t } ) . )$ 



10.33 Consider an n-channel MOSFET with the following parameters: $k _ { n } ^ { \prime } = 0 . 1 8 \mathrm { m A } / \mathrm { V } ^ { 2 } ,$ $W / L = 8 ,$ , and $V _ { T } = 0 . 4 \ : \mathrm { V } .$ Determine the drain current $I _ { D }$ for (a) $V _ { G S } = 0 . 8 \ : \mathrm { V } ,$ $V _ { D S } = 0 . 2 \mathrm { ~ V } ; ( b ) V _ { G S } = 0 . 8 \mathrm { ~ V } , V _ { D S } = 1 . 2 \mathrm { ~ V } ; ( c ) V _ { G S } = 0 . 8 \mathrm { ~ V } , V _ { D S } = 2 . 5 \mathrm { ~ V } ;$ and $( d ) \ V _ { G S } = 1 . 2 \mathrm { V } , V _ { D S } = 2 . 5 \mathrm { V } .$ 





10.34 A p-channel MOSFET has the following parameters: $k _ { p } ^ { \prime } = 0 . 1 0 \mathrm { m A } / \mathrm { V } ^ { 2 } , W / L = 1 5 ,$ and $V _ { T } = - 0 . 4 \ : \mathrm { V } .$ Calculate the drain current $I _ { D }$ for (a) $V _ { S G } = 0 . 8 \mathrm { V } , V _ { S D } = 0 . 2 5 \mathrm { V } ; ( b ) V _ { S G } =$ $0 . 8 \mathrm { V } , V _ { S D } = 1 . 0 \mathrm { V } ; ( c ) V _ { S G } = 1 . 2 \mathrm { V } , V _ { S D } = 1 . 0 \mathrm { V } ;$ and (d) $V _ { S G } = 1 . 2 \mathrm { V } , V _ { S D } = 2 . 0 \mathrm { V } .$ 





10.35 The parameters of an n-channel MOSFET are $k _ { n } ^ { \prime } = 0 . 6 \mathrm { m A } / \mathrm { V } ^ { 2 }$ and $V _ { T } = 0 . 8 \ : \mathrm { V } .$ . The drain current is 1 mA with applied voltages of $V _ { G S } = 1 . 4 \mathrm { V } , V _ { S B } = 0 .$ , and $V _ { D S } = 4 \mathrm { V } .$ (a) What is the $W / L$ value? (b) What is the value of $I _ { D }$ for $V _ { G S } = 1 . 8 5 \mathrm { V } , V _ { S B } = 0 ,$ and $V _ { D S } = 6 \mathrm { V } ? ( c )$ Determine the value of $I _ { D }$ for $V _ { G S } = 1 . 2 \mathrm { V } , V _ { S B } = 0 .$ , and $V _ { D S } = 0 . 1 5 \ : \mathrm { V } .$ 





10.36 Consider a p-channel MOSFET with the following parameters: $k _ { p } ^ { \prime } = 0 . 1 2 \mathrm { m A } / \mathrm { V } ^ { 2 }$ and $W / L = 2 0$ . The drain current is $1 0 0 \mu \mathrm { A }$ with applied voltages of $V _ { S G } = 0$ , $V _ { B S } = 0 .$ , and $V _ { S D } = 1 . 0 \mathrm { V } . ( a )$ Determine the $V _ { T }$ value. (b) Determine the drain current $I _ { D }$ for $V _ { S G } = 0 . 4 \mathrm { V } , V _ { S B } = 0$ , and $V _ { S D } = 1 . 5 \ : \mathrm { V } .$ (c) What is the value of $I _ { D }$ for $V _ { S G } = 0 . 6 \mathrm { V } , V _ { S B } = 0$ , and $V _ { S D } = 0 . 1 5 \ : \mathrm { V ? }$ 





10.37 An ideal n-channel MOSFET has the following parameters: $V _ { T } = 0 . 4 5 \ : \mathrm { V } ,$ $\mu _ { n } = 4 2 5 \mathrm { \ c m ^ { 2 } / V { - } s , } t _ { o x } = 1 1 \mathrm { \ n m } = 1 1 0 \mathring { \mathrm { A } } , W = 2 0 \mu \mathrm { m }$ , and $L = 1 . 2 \mu \mathrm { m . } ( a )$ Plot $I _ { D }$ versus $V _ { D S }$ for $0 \leq V _ { D S } \leq 3 \mathrm { V }$ and for VGS  0, 0.6, 1.2, 1.8, and 2.4 V. Indicate on ______ each curve the $V _ { D S } ( s a t )$ point. (b) Plot $\sqrt { I _ { D } ( s a t ) }$ versus $V _ { G S }$ for $0 \leq V _ { G S } \leq 2 . 4 \mathrm { V } .$ (c) Plot $I _ { D }$ versus $V _ { G S }$ for $0 \leq V _ { G S } \leq 2 . 4 \mathrm { V }$ and for $V _ { D S } = 0 . 1 \ : \mathrm { V } .$ 





10.38 Consider an ideal p-channel MOSFET with the following parameters: $V _ { T } = - 0 . 3 5 \ : \mathrm { V } ,$ $\mu _ { p } = 2 1 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - } \mathrm { s } , t _ { o x } = 1 1 \mathrm { n m } = 1 1 0 \mathring { \mathrm { A } } , W = 3 5 \mu \mathrm { m }$ , and $L = 1 . 2 \mu \mathrm { m }$ . (a) Plot $I _ { D }$ versus $V _ { S D }$ for $0 \leq V _ { S D } \leq 3 \mathrm { V }$ and for $V _ { S G } = 0 , 0 . 6 , 1 . 2 , 1 . 8 .$ , and 2.4 V. Indicate on each curve the $V _ { S D } ( s a t )$ point. (b) Plot $\sqrt { I _ { D } ( s a t ) }$ versus $V _ { S G }$ for $0 \leq V _ { S G } \leq 2 . 4 \mathrm { V } .$ (c) Plot $I _ { D }$ versus $V _ { S G }$ for $0 \leq V _ { S G } \leq 2 . 4 \mathrm { V }$ and for $V _ { S D } = 0 . 1 \mathrm { V } .$ 





10.39 Consider an n-channel MOSFET with the same parameters as described in Problem 10.37 except that $V _ { T } = - 0 . 8 \ : \mathrm { V } .$ (a) Plot $I _ { D }$ versus $V _ { D S }$ for $0 \leq V _ { D S } \leq 3 \mathrm { V }$ and for $V _ { G S } = - 0 . 8 .$ , $0 , + 0 . 8 .$ , and 1.6 V. (b) Plot $\sqrt { I _ { D } ( s a t ) }$ versus $V _ { G S } \mathrm { f o r } - 0 . 8 \leq V _ { G S } \leq 1 . 6 \mathrm { V } .$ 





10.40 Consider an n-channel enhancement mode MOSFET biased as shown in Figure P10.40. Sketch the current–voltage characteristics, $I _ { D }$ versus $V _ { D S } ,$ for (a) $V _ { G D } = 0 , ( b ) V _ { G D } = V _ { T } / 2 .$ , and (c) $V _ { G D } = 2 V _ { T } .$ 





10.41 Figure P10.41 shows the cross section of an NMOS device that includes source and drain resistances. These resistances take into account the bulk $n ^ { + }$ semiconductor resistance and the ohmic contact resistance. The current–voltage relations can be generated by replacing $V _ { G S }$ by $V _ { G } - I _ { D } R _ { S }$ and $V _ { D S }$ by $V _ { D } - I _ { D } ( R _ { S } + R _ { D } )$ in the ideal equations. Assume transistor parameters of $V _ { T } = 1 \mathrm { V }$ and $K _ { n } = 1 \mathrm { m A } / \mathrm { V } ^ { 2 } . ( a )$ Plot the following curves on the same graph: $I _ { D }$ versus $V _ { D }$ for $V _ { G } = 2 \mathrm { \Delta V }$ and $V _ { G } = 3 \mathrm { V }$ over the range $0 \le V _ { D } \le 5 \mathrm { V }$ for (i ) $R _ { S } = R _ { D } = 0$ and (ii )__ $R _ { S } = R _ { D } = 1 { \mathrm { k } } \Omega$ . (b) Plot the following curves on the same graph: $\sqrt { I _ { D } }$ versus $V _ { G }$ for $V _ { D } = 0 . 1 \ : \mathrm { V }$ and $V _ { D } = 5 \mathrm { V }$ over the range $0 \le I _ { D } \le 1  { \mathrm { m A } }$ for (i ) $R _ { S } = R _ { D } = 0$ and (ii ) $R _ { S } = R _ { D } = 1 { \mathrm k } \Omega$ . 





10.42 An n-channel MOSFET has the same parameters as given in Problem 10.37. The gate terminal is connected to the drain terminal. Plot $I _ { D }$ versus $V _ { D S }$ for $0 \le { \cal V } _ { D S } \le$ $5 \mathrm { V } .$ Determine the range of $V _ { D S }$ over which the transistor is biased in the nonsaturation and saturation regions. 





10.43 The channel conductance for a p-channel MOSFET is defi ned as 



$$
g _ {d} = \left. \frac {\partial I _ {D}}{\partial V _ {S D}} \right| _ {V _ {S D \rightarrow 0}}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/6a50336b7a4709e819adfedbb7f02a133ed27014b0994f1d5d1391ec0db08876.jpg)



Figure P10.40 | Figure for Problem 10.40.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/01f6a5a904deaf81321cb37fdcfd42eeb3147057aa89e65796f43624918b56e4.jpg)



Figure P10.41 | Figure for Problem 10.41.


Plot the channel conductance for the p-channel MOSFET described in Problem 10.38 for $0 \leq V _ { S G } \leq 2 . 4 .$ . 

10.44 The transconductance of an n-channel MOSFET is found to be $g _ { m } = \partial I _ { D } / \partial V _ { G S } =$ 1.25 mA/V when measured at $V _ { D S } = 5 0$ mV. The threshold voltage is $V _ { T } = 0 . 3 \ : \mathrm { V } .$ 

(a) Determine the conductance parameter $K _ { n \bullet } \left( b \right)$ What is the current at $V _ { G S } = 0 . 8 \ : \mathrm { V }$ and $V _ { D S } = 5 0 \mathrm { m V ? } \left( c \right)$ Determine the current at $V _ { G S } = 0 . 8 \ : \mathrm { V }$ and $V _ { D S } = 1 . 5 \ : \mathrm { V } .$ 

10.45 The experimental characteristics of an ideal n-channel MOSFET biased in the satu ration region are shown in Figure P10.45. If $W / L = 1 0 \mathrm { a n d } t _ { \mathrm { o x } } = 4 2 5 \mathring { \mathrm { A } }$ , determine $V _ { T }$ and $\mu _ { n } .$ 

10.46 One curve of an n-channel MOSFET is characterized by the following parameters: $I _ { D } ( \mathrm { s a t } ) = 2 \times 1 0 ^ { - 4 } \mathrm { A } , V _ { D S } ( \mathrm { s a t } ) = 4 \mathrm { V } ,$ and $V _ { T } = 0 . 8 \ : \mathrm { V } .$ 

(a) What is the gate voltage? 

(b) What is the value of the conduction parameter? 

(c) If $V _ { G } = 2 \mathrm { V }$ and $V _ { D S } = 2 \mathrm { V } ,$ determine $I _ { D } .$ 

(d) If $V _ { G } = 3 \mathrm { ~ V ~ }$ and $V _ { D S } = 1 \mathrm { V } ,$ determine $I _ { D } .$ 

(e) For each of the conditions given in (c) and $( d )$ , sketch the inversion charge density and depletion region through the channel. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-06-16/84c3eb41-ff12-40b1-9e82-61bf4f208bfd/14f1670efaa81ab766d0f365e176dcd2f45a0c048d2e3858ebef5564b13a7350.jpg)



Figure P10.45 | Figure for Problem 10.45.


10.47 (a) An ideal n-channel MOSFET has parameters $t _ { o x } = 1 8 \ \mathrm { n m } = 1 8 0 \textup { \AA } , \mu _ { n } = 4 5 0 \ \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } ,$ and $V _ { T } = 0 . 4 \ : \mathrm { V } .$ The measured current in the saturation region is $I _ { D } ( s a t ) = 0 . 8 \mathrm { m A }$ when biased at $V _ { G S } = 2 . 0 ~ \mathrm { V } .$ Determine the (i) process conduction parameter and (ii) width-to-length ratio. (b) An ideal p-channel MOSFET has the same oxide thickness as given in part (a), a mobility of $\mu _ { p } = 2 1 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { \mathrm { - s } } ,$ , and a threshold voltage of $V _ { T } = - 0 . 4 \ : \mathrm { V } .$ The measured current in the saturation region is also $I _ { D } ( s a t ) = 0 . 8$ mA when biased at $V _ { S G } = 2 . 0 ~ \mathrm { V } .$ . Determine the (i) process conduction parameter and (ii) width-to-length ratio. 

10.48 Consider the n-channel MOSFET described in Problem 10.37. (a) Calculate $g _ { m L }$ for $V _ { D S } = 0 . 1 0 \mathrm { V } .$ (b) Find $g _ { m s }$ for $V _ { G S } = 1 . 5 \ : \mathrm { V } .$ 

10.49 Consider the p-channel MOSFET described in Problem 10.38. (a) Calculate $g _ { m L }$ for $V _ { S D } = 0 . 1 0 \mathrm { V } . ( b )$ Find $g _ { m s }$ for $V _ { S G } = 1 . 5 \ : \mathrm { V } .$ 

10.50 An n-channel MOSFET has the following parameters: $N _ { a } = 5 \times 1 0 ^ { 1 6 } \mathrm { c m } ^ { - 3 }$ , $t _ { o x } = 1 5 \ \mathrm { n m } = 1 5 0 \textup { \AA } , \mu _ { n } = 4 5 0 \ c \mathrm { m } ^ { 2 } / \mathrm { V } \mathrm { - s } , V _ { F B } = - 0 . 5 \mathrm { V } , L = 1 . 2 \ \mu \mathrm { m }$ , and $W = 8 \mu \mathrm { m }$ . (a) Determine the body-effect coeffi cient. (b) Plot $\sqrt { I _ { D } ( s a t ) }$ versus $V _ { G S }$ over the range $0 \le I _ { D } \le 0 . 5$ mA for source-to-body voltages of (i) $V _ { S B } = 0 , ( i i ) \ V _ { S B } = 1 \mathrm { V } ,$ (iii) $V _ { S B } = 2 \mathrm { V } ,$ and (iv) $V _ { S B } = 4 \mathrm { V } . ( c )$ What are the threshold voltages for the conditions given in part (b)? 

10.51 The substrate doping and body-effect coeffi cient of an n-channel MOSFET are $N _ { a } = 1 0 ^ { 1 6 } \thinspace \mathrm { c m } ^ { - 3 }$ and $\gamma = 0 . 1 2 \mathrm { V } ^ { 1 / 2 }$ , respectively. The threshold voltage is found to be $V _ { T } = 0 . 5 \ : \mathrm { V }$ when biased at $V _ { S B } = 2 . 5 \ : \mathrm { V } .$ What is the threshold voltage at $V _ { S B } = 0 ?$ 

10.52 A p-channel MOSFET has an oxide thickness of $t _ { o x } = 2 0 \mathrm { n m } = 2 0 0 \mathring \mathrm { A }$ and a substrate doping of $N _ { d } = 5 \times 1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ . (a) Find the body-effect coeffi cient. (b) Determine the body-to-source voltage, $V _ { B S } ,$ , such that the shift in threshold voltage, $\Delta V _ { T } ,$ from the $V _ { B S } = 0$ curve is $\Delta V _ { T } = - 0 . 2 2 \ : \mathrm { V } .$ . 

10.53 An NMOS device has the following parameters: $\mathrm { n ^ { + } }$ poly gate, $t _ { \mathrm { o x } } = 4 0 0 \mathring { \mathrm { A } } , N _ { a } =$ $1 0 ^ { 1 5 } \mathrm { c m } ^ { - 3 }$ , and $Q _ { s s } ^ { \prime } = 5 \times 1 0 ^ { 1 0 } \mathrm { c m } ^ { - 2 } .$ . (a) Determine $V _ { T } , \left( b \right)$ Is it possible to apply a $V _ { S B }$ voltage such that $V _ { T } = 0 ? \ : \mathrm { I f } \ : \mathrm { s o }$ , what is the value of $V _ { S B } \mathrm { ' }$ 

10.54 Investigate the threshold voltage shift due to substrate bias. The threshold shift is given by Equation (10.81). Plot $\Delta V _ { T }$ versus $V _ { S B }$ over the range $0 \le V _ { S B } \le 5 \mathrm { V }$ for several values of $N _ { a }$ and $t _ { \mathrm { o x } }$ . Determine the conditions for which $\Delta V _ { T }$ is limited to a maximum value of $0 . 7 \mathrm { V }$ over the range of $V _ { S B }$ . 

## Section 10.4 Frequency Limitations

10.55 Consider an ideal n-channel MOSFET with a width-to-length ratio of $( W / L ) = 1 0 $ , an electron mobility of $\mu _ { n } = 4 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s } .$ , an oxide thickness of $t _ { \mathrm { o x } } = 4 7 5 \mathrm { ~ \AA ~ }$ , and a threshold voltage of $V _ { T } = \mathrel { + } 0 . 6 5 \mathrm { V } . ( a )$ Determine the maximum value of source resistance so that the saturation transconductance $g _ { m s }$ is reduced by no more than 20 percent from its ideal value when $V _ { G S } = 5 \mathrm { V } . ( b )$ Using the value of $r _ { s }$ calculated in part (a), how much is $g _ { m s }$ reduced from its ideal value when $V _ { G S } = 3 \mathrm { V } ?$ 

10.56 An n-channel MOSFET has the following parameters: 

$$
\mu_ {n} = 4 0 0 \mathrm{cm} ^ {2} / \mathrm{V} - \mathrm{s} \quad t _ {\mathrm{ox}} = 5 0 0 \AA
$$

$$
L = 2 \mu \mathrm{m} \quad W = 2 0 \mu \mathrm{m}
$$

$$
V _ {T} = + 0. 7 5 \mathrm{V}
$$

Assume the transistor is biased in the saturation region at $V _ { G S } = 4 \mathrm { V . } ( a )$ Calculate the ideal cutoff frequency. (b) Assume that the gate oxide overlaps both the source and drain contacts by 0.75 m. If a load resistance of $R _ { L } = 1 0 \mathrm { k } \Omega$ is connected to the output, calculate the cutoff frequency. 

10.57 Repeat Problem 10.56 for the case when the electrons are traveling at a saturation velocity of $v _ { \mathrm { s a t } } = 4 \times 1 0 ^ { 6 }$ cm /s. 



5. Ng, K. K. Complete Guide to Semiconductor Devices. New York: McGraw-Hill, 1995. 



## Summary and Review



6. Nicollian, E. H., and J. R. Brews. MOS Physics and Technology. New York: Wiley, 1982. 



*10.58 Design an ideal silicon n-channel MOSFET with a polysilicon gate to have a threshold voltage of $V _ { T } = 0 . 6 5 \ : \mathrm { V } .$ . Assume an oxide thickness of $t _ { \mathrm { o x } } = 3 0 0 \mathring { \mathrm { A } } , \mathrm { a }$ channel length of $L = 1 . 2 5 \mu \mathrm { m }$ , and a nominal value of $Q _ { s s } ^ { \prime } = 1 . 5 \times 1 0 ^ { 1 1 } \mathrm { c m } ^ { - 2 }$ . It is desired to have a drain current of $I _ { D } = 5 0 \mu \mathrm { A }$ at $V _ { G S } = 2 . 5 \ : \mathrm { V }$ and $V _ { D S } = 0 . 1 \ : \mathrm { V } .$ Determine the substrate doping concentration, channel width, and type of gate required. 



7. Ong, D. G. Modern MOS Technology: Processes, Devices, and Design. New York: McGraw-Hill, 1984. 



*10.59 Design an ideal silicon n-channel depletion mode MOSFET with a polysilicon gate to have a threshold voltage of $V _ { T } = - 0 . 6 5 \ : \mathrm { V } .$ Assume an oxide thickness of $t _ { \mathrm { o x } } = 3 0 0 \mathring \mathrm { A }$ , a channel length of $L = 1 . 2 5 \mu \mathrm { m }$ , and a nominal value of $Q _ { s s } ^ { \prime } = 1 . 5 \times 1 0 ^ { 1 1 } \mathrm { c m } ^ { - 2 }$ . It is desired to have a drain current of $I _ { D } ( \mathrm { s a t } ) = 5 0 \mu \mathrm { A }$ at $V _ { G S } = 0$ . Determine the type of gate, substrate doping concentration, and channel width required. 



8. Pierret, R. F. Semiconductor Device Fundamentals. Reading, MA: Addison-Wesley, 1996. 



*10.60 Consider the CMOS inverter circuit shown in Figure 10.59a. Ideal n- and p-channel devices are to be designed with channel lengths of $L = 2 . 5 \mu \mathrm { m }$ and oxide thicknesses of $t _ { \mathrm { o x } } = 4 5 0 \mathrm { ~ \AA ~ }$ . Assume the inversion channel mobilities are one-half the bulk values. The threshold voltages of the n- and p-channel transistors are to be 0.5 V and 0.5 V, respectively. The drain current is to be $I _ { D } = 0 . 2 5 6$ mA when the input voltage to the inverter is 1.5 V and 3.5 V with $V _ { D D } = 5 \mathrm { V } .$ The gate material is to be the same in each device. Determine the type of gate, substrate doping concentrations, and channel widths. 



9. Roulston, D. J. An Introduction to the Physics of Semiconductor Devices. New York: Oxford University Press, 1999. 



*10.61 A complementary pair of ideal n-channel and p-channel MOSFETs is to be designed to produce the same I–V characteristics when they are equivalently biased. The devices are to have the same oxide thickness of 250 Å and the same channel length of L  2 m. Assume the SiO2 layer is ideal. The n-channel device is to have a channel width of W  20 m. Assume constant inversion layer mobilities of $\mu _ { n } = 6 0 0 \mathrm { c m } ^ { 2 } / \mathrm { V } \mathrm { - s }$ and $\mu _ { p } = 2 2 0 \mathrm { c m } ^ { 2 } / \mathrm { V } { - \mathrm { s } } .$ (a) Determine p-type and n-type substrate doping concentrations. (b) What are the threshold voltages? (c) What is the width of the p-channel device? 



10. Schroder, D. K. Advanced MOS Devices, Modular Series on Solid State Devices. Reading, MA: Addison-Wesley, 1987. 



## READING LIST



11. Shur, M. Introduction to Electronic Devices. New York: John Wiley & Sons, Inc., 1996. 





*12. Physics of Semiconductor Devices. Englewood Cliffs, NJ: Prentice Hall, 1990. 





1. Dimitrijev, S. Principles of Semiconductor Devices. New York: Oxford University, 2006. 





13. Singh, J. Semiconductor Devices: An Introduction. New York: McGraw-Hill, 1994. 





2. Hu, C. C. Modern Semiconductor Devices for Integrated Cicuits. Upper Saddle River, NJ: Pearson Prentice Hall, 2010. 





14. Semiconductor Devices: Basic Principles. New York: Wiley, 2001. 





3. Kano, K. Semiconductor Devices. Upper Saddle River, NJ: Prentice Hall, 1998. 





15. Streetman, B. G., and S. K. Banerjee. Solid State Electronic Devices. 6th ed. Upper Saddle River, NJ: Pearson Prentice Hall, 2006. 





4. Muller, R. S., and T. I. Kamins. Device Electronics for Integrated Circuits. 2nd ed. New York: Wiley, 1986. 





16. Sze, S. M. High-Speed Semiconductor Devices. New York: Wiley, 1990. 





17. Sze, S. M. and K. K. Ng. Physics of Semiconductor Devices, 3rd ed. Hoboken, NJ: John Wiley & Sons, Inc., 2007. 





18. Taur, Y. and T. H. Ning. Fundamentals of Modern VLSI Devices, 2nd ed. Cambridge University Press, 2009. 





*19. Tsividis, Y. Operation and Modeling of the MOS Transistor. 2nd ed. Burr Ridge, IL: McGraw-Hill, 1999. 





20. Werner, W. M. “The Work Function Difference of the MOS System with Aluminum Field Plates and Polycrystalline Silicon Field Plates.” Solid State Electronics 17, (1974), pp. 769–775. 





21. Yamaguchi, T., S. Morimoto, G. H. Kawamoto, and J. C. DeLacy. “Process and Device Performance of 1 m-Channel n-Well CMOS Technology.” IEEE Transactions on Electron Devices ED-31 (February 1984), pp. 205–214. 





22. Yang, E. S. Microelectronic Devices. New York: McGraw-Hill, 1988. 

