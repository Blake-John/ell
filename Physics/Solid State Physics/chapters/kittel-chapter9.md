# 9

# Fermi Surfaces and Metals

Reduced zone scheme 223 

Periodic zone scheme 225 

CONSTRUCTION OF FERMI SURFACES 226 

Nearly free electrons 228 

ELECTRON ORBITS, HOLE ORBITS, AND OPEN ORBITS 230 

CALCULATION OF ENERGY BANDS 232 

Tight binding method for energy bands 232 

Wigner-Seitz method 236 

Cohesive energy 237 

Pseudopotential methods 239 

EXPERIMENTAL METHODS IN FERMI SURFACE STUDIES 242 

Quantization of orbits in a magnetic field 242 

De Haas-van Alphen effect 244 

Extremal orbits 248 

Fermi surface of copper 249 

Example: Fermi surface of gold 249 

Magnetic breakdown 251 

SUMMARY 252 

PROBLEMS 252 

1. Brillouin zones of rectangular lattice 252 

2. Brillouin zone, rectangular lattice 252 

3. Hexagonal close-packed structure 252 

4. Brillouin zones of two-dimensional divalent metal 253 

5. Open orbits 253 

6. Cohesive energy for a square well potential 253 

7. De Haas-van Alphen period of potassium 253 

8. Band edge structure on k - p perturbation theory 253 

9. Wannier functions 254 

10. Open orbits and magnetoresistance 254 

11. Landau levels 254 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/25fc99ada6160b92be231204112ce7a4665696b5f5dd4557e68d05294b90173a.jpg)



Figure 1 Free electron Fermi surfaces for fcc metals with one (Cu) and three (Al) valence electrons per primitive cell. The Fermi surface shown for copper has been deformed from a sphere to agree with the experimental results. The second zone of aluminum is nearly half-filled with electrons. (A. R. Mackintosh.)


Few people would define a metal as “a solid with a Fermi surface.” This may nevertheless be the most meaningful definition of a metal one can give today; it represents a profound advance in the understanding of why metals behave as they do. The concept of the Fermi surface, as developed by quantum physics, provides a precise explanation of the main physical properties of metals. 

A. R. Mackintosh 

The Fermi surface is the surface of constant energy $\epsilon _ { F }$ in k space. The Fermi surface separates the unfilled orbitals from the filled orbitals, at absolute zero. The electrical properties of the metal are determined by the volume and shape of the Fermi surface, because the current is due to changes in the occupancy of states near the Fermi surface. 

The shape may be very intricate as viewed in the reduced zone scheme below and yet have a simple interpretation when reconstructed to lie near the surface of a sphere. We exhibit in Fig. 1 the free electron Fermi surfaces constructed for two metals that have the face-centered cubic crystal structure: copper, with one valence electron, and aluminum, with three. The free electron Fermi surfaces were developed from spheres of radius $k _ { F }$ determined by the valence electron concentration. The surface for copper is deformed by interaction with the lattice. How do we construct these surfaces from a sphere? The constructions require the reduced and also the periodic zone schemes. 

## Reduced Zone Scheme

It is always possible to select the wavevector index k of any Bloch function to lie within the first Brillouin zone. The procedure is known as mapping the band in the reduced zone scheme. 

If we encounter a Bloch function written as $\psi _ { \mathbf { k } ^ { \prime } } ( \mathbf { r } ) = e ^ { i \mathbf { k } ^ { \prime } \cdot \mathbf { r } } u _ { \mathbf { k } ^ { \prime } } ( \mathbf { r } )$ , with $\mathbf { k } ^ { \prime }$ outside the first zone, as in Fig. 2, we may always find a suitable reciprocal lattice vector G such that $\mathbf { k } = \mathbf { k } ^ { \prime } + \mathbf { G }$ lies within the first Brillouin zone. Then 

$$
\begin{array}{l} \psi_ {\mathbf {k} ^ {\prime}} (\mathbf {r}) = e ^ {i \mathbf {k} ^ {\prime} \cdot \mathbf {r}} u _ {\mathbf {k} ^ {\prime}} (\mathbf {r}) = e ^ {i \mathbf {k} \cdot \mathbf {r}} (e ^ {- i \mathbf {G} \cdot \mathbf {r}} u _ {\mathbf {k} ^ {\prime}} (\mathbf {r})) \tag {1} \\ = e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) = \psi_ {\mathbf {k}} (\mathbf {r}), \\ \end{array}
$$

where $u _ { \bf k } ( { \bf r } ) = e ^ { - i { { \bf G } \cdot { \bf r } } } u _ { { \bf k } ^ { \prime } } ( { \bf r } )$ . Both $e ^ { - i \mathbf { G } \cdot \mathbf { r } }$ and $u _ { \mathbf { k } ^ { \prime } } ( \mathbf { r } )$ are periodic in the crystal lattice, so $u _ { \bf k } ( { \bf r } )$ is also, whence $\psi _ { k } ( \mathbf { r } )$ is of the Bloch form. 

Even with free electrons it is useful to work in the reduced zone scheme, as in Fig. 3. Any energy $\epsilon _ { \mathbf { k } ^ { \prime } }$ for $\mathbf { k } ^ { \prime }$ outside the first zone is equal to an $\epsilon _ { \mathbf { k } }$ in the first zone, where $\mathbf { k } = \mathbf { k } ^ { \prime } + \mathbf { G }$ . Thus we need solve for the energy only in the first Brillouin zone, for each band. An energy band is a single branch of the $\epsilon _ { \mathbf { k } }$ versus k surface. In the reduced zone scheme we may find different energies at the same value of the wavevector. Each different energy characterizes a different band. Two bands are shown in Fig. 3. 


Figure 2 First Brillouin zone of a square lattice of side a. The wavevector k can be carried into the first zone by forming $\mathbf { k } ^ { \prime } + \mathbf { G }$ . The wavevector at a point A on the zone boundary is carried by G to the point $A ^ { \prime }$ on the opposite boundary of the same zone. Shall we count both A and $A ^ { \prime }$ as lying in the first zone? Because they can be connected by a reciprocal lattice vector, we count them as one identical point in the zone.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/858c7257064374a0863b0a490b64335086a4638460228029e184317a4ee60514.jpg)



Figure 3 Energy-wavevector relation $\epsilon _ { k } = \hbar ^ { 2 } k ^ { 2 } / 2 m$ for free electrons as drawn in the reduced zone scheme. This construction often gives a useful idea of the overall appearance of the band structure of a crystal. The branch AC if displaced by $- 2 \pi / a$ gives the usual free electron curve for negative k, as suggested by the dashed curve. The branch AC if displaced by 2/a gives the usual curve for positive k. A crystal potential U(x) will introduce band gaps at the edges of the zone (as at A and A) and at the center of the zone (as at C). The point C when viewed in the extended zone scheme falls at the edges of the second zone. The overall width and gross features of the band structure are often indicated properly by such free electron bands in the reduced zone scheme.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/c13bb6f8f2d02ba4819149a8a5f1b3240d5fff1fd9743840e6a05db9f5651805.jpg)


Two wavefunctions at the same k but of different energies will be independent of each other: the wavefunctions will be made up of different combinations of the plane wave components $\exp [ i ( \mathbf { k } + \mathbf { G } ) \cdot \mathbf { r } ]$ in the expansion of (7.29). Because the values of the coefficients $C ( \mathbf { k } + \mathbf { G } )$ will differ for the different bands, we should add a symbol, say n, to the $\boldsymbol { C } \boldsymbol { \mathrm { : } }$ to serve as a band index: $C _ { n } ( \mathbf { k } + \mathbf { G } )$ . Thus the Bloch function for a state of wavevector k in the band n can be written as 

$$
\psi_ {n, \mathbf {k}} = \exp (i \mathbf {k} \cdot \mathbf {r}) u _ {n, \mathbf {k}} (\mathbf {r}) = \sum_ {\mathbf {G}} C _ {n} (\mathbf {k} + \mathbf {G}) \exp [ i (\mathbf {k} + \mathbf {G}) \cdot \mathbf {r} ].
$$

## Periodic Zone Scheme

We can repeat a given Brillouin zone periodically through all of wavevector space. To repeat a zone, we translate the zone by a reciprocal lattice vector. If we can translate a band from other zones into the first zone, we can translate a band in the first zone into every other zone. In this scheme the energy $\epsilon _ { \mathbf { k } }$ of a band is a periodic function in the reciprocal lattice: 

$$
\epsilon_ {\mathbf {k}} = \epsilon_ {\mathbf {k} + \mathbf {G}}. \tag {2}
$$

Here $\epsilon _ { \mathbf { k } + \mathbf { G } }$ is understood to refer to the same energy band as $\epsilon _ { \mathbf { k } }$ 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/68c5ce82ed2d408252abab3c0c29bdb70ba500e86be15673fd569ad928bdfedd.jpg)



Figure 4 Three energy bands of a linear lattice plotted in (a) the extended (Brillouin), (b) reduced, and (c) periodic zone schemes.


The result of this construction is known as the periodic zone scheme. The periodic property of the energy also can be seen easily from the central equation (7.27). 

Consider for example an energy band of a simple cubic lattice as calculated in the tight-binding approximation in (13) below: 

$$
\epsilon_ {k} = - \alpha - 2 \gamma (\cos k _ {x} a + \cos k _ {y} a + \cos k _ {z} a), \tag {3}
$$

where  and  are constants. One reciprocal lattice vector of the sc lattice is $\mathbf { G } = ( 2 \pi / a ) \hat { \mathbf { x } }$ ; if we add this vector to k the only change in (3) is 

$$
\cos k _ {x} a \rightarrow \cos (k _ {x} + 2 \pi / a) a = \cos (k _ {x} a + 2 \pi),
$$

but this is identically equal to cos $k _ { x } a$ . The energy is unchanged when the wavevector is increased by a reciprocal lattice vector, so that the energy is a periodic function of the wavevector. 

Three different zone schemes are useful (Fig. 4): 

• The extended zone scheme in which different bands are drawn in different zones in wavevector space. 

• The reduced zone scheme in which all bands are drawn in the first Brillouin zone. 

• The periodic zone scheme in which every band is drawn in every zone. 

# CONSTRUCTION OF FERMI SURFACES

We consider in Fig. 5 the analysis for a square lattice. The equation of the zone boundaries is $2 { \bf k } { \cdot } { \bf G } + G ^ { 2 } = 0$ and is satisfied if k terminates on the plane normal to G at the midpoint of G. The first Brillouin zone of the square lattice is the area enclosed by the perpendicular bisectors of $\mathbf { G } _ { 1 }$ and of the three reciprocal lattice vectors equivalent by symmetry to $\mathbf { G } _ { 1 }$ in Fig. 5a. These four reciprocal lattice vectors are $\pm ( 2 \pi / a ) \dot { \hat { \mathbf { k } } } _ { x }$ and $\pm ( 2 \pi / a ) \hat { \mathbf { k } } _ { y }$ . 

The second zone is constructed from $\mathbf { G } _ { 2 }$ and the three vectors equivalent to it by symmetry, and similarly for the third zone. The pieces of the second and third zones are drawn in Fig. 5b. 

To determine the boundaries of some zones we have to consider sets of several nonequivalent reciprocal lattice vectors. Thus the boundaries of section $3 _ { a }$ of the third zone are formed from the perpendicular bisectors of three G’s, namely $( 2 \pi / a ) \hat { \mathbf { k } } _ { x } ; ( 4 \pi / a ) \hat { \mathbf { k } } _ { y } ;$ and $( 2 \pi / a ) ( \hat { \mathbf { k } } _ { x } \hat { + } \hat { \mathbf { k } _ { y } } )$ . 

The free electron Fermi surface for an arbitrary electron concentration is shown in Fig. 6. It is inconvenient to have sections of the Fermi surface that belong to the same zone appear detached from one another. The detachment can be repaired by a transformation to the reduced zone scheme. 

We take the triangle labeled $2 _ { a }$ and move it by a reciprocal lattice vector ${ \textbf { G } } = - ( 2 \pi / a ) { \hat { \mathbf { k } } } _ { x }$ such that the triangle reappears in the area of the first 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/0f4cc960d2459066675dcf0d1797266928a7c4b5578affa4e7c9b314a7552f71.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/8ed69fee55784580e47b6bd0c57fde0250cfd24e7282b04804127038dddb5647.jpg)



Figure 5 (a) Construction in k space of the first three Brillouin zones of a square lattice. The three shortest forms of the reciprocal lattice vectors are indicated as $\mathbf { G } _ { 1 } , \mathbf { G } _ { 2 } ,$ and $\mathbf { G } _ { 3 } .$ The lines drawn are the perpendicular bisectors of these G’s. (b) On constructing all lines equivalent by symmetry to the three lines in (a) we obtain the regions in k space which form the first three Brillouin zones. The numbers denote the zone to which the regions belong; the numbers here are ordered according to the length of the vector G involved in the construction of the outer boundary of the region.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/3d329309863b56d085c36c38e4a5c527fed40940fb7efe9a764ac2eae9750d23.jpg)



Figure 6 Brillouin zones of a square lattice in two dimensions. The circle shown is a surface of constant energy for free electrons; it will be the Fermi surface for some particular value of the electron concentration. The total area of the filled region in k space depends only on the electron concentration and is independent of the interaction of the electrons with the lattice. The shape of the Fermi surface depends on the lattice interaction, and the shape will not be an exact circle in an actual lattice. The labels within the sections of the second and third zones refer to Fig. 7.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/5db3c6ea3da0ece5142355350cc113523b231eced102f4a1ed6df2bf46ded0bd.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/f404cf0e386fe274e74052ac61663b7201c11c46eb36bbb54774e0bf6eaa87ef.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/c1a9f96dc2a755822f129f8455523715f6173ede8084f1d7cc94bba83e784e08.jpg)



Figure 7 Mapping of the first, second, and third Brillouin zones in the reduced zone scheme. The sections of the second zone in Fig. 6 are put together into a square by translation through an appropriate reciprocal lattice vector. A different G is needed for each piece of a zone.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/cef657c3911a556ac19553d53d1034b288be2401439d26e7689c9384cce5fe2c.jpg)



1st zone


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/d5009b8dd18a0097f99b952f5456a32d5b997b0abe196e0057a9b89400b357d0.jpg)



2nd zone


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/6bdbb2b0b94fe2be32821e4839f49c6b98127a6cf8f43d1acf24f1413bafb101.jpg)



3rd zone



Figure 8 The free electron Fermi surface of Fig. 6, as viewed in the reduced zone scheme. The shaded areas represent occupied electron states. Parts of the Fermi surface fall in the second, third, and fourth zones. The fourth zone is not shown. The first zone is entirely occupied.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/5033faa14ce75c4bc8cdbbe21ad9d039e483f09ccd5a003c5df07acff9855fa6.jpg)



Figure 9 The Fermi surface in the third zone as drawn in the periodic zone scheme. The figure was constructed by repeating the third zone of Fig. 8.


Brillouin zone (Fig. 7). Other reciprocal lattice vectors will shift the triangles $\mathcal { 2 } _ { b } , \mathcal { 2 } _ { c } , \mathcal { 2 } _ { d }$ to other parts of the first zone, completing the mapping of the second zone into the reduced zone scheme. The parts of the Fermi surface falling in the second zone are now connected, as shown in Fig. 8. 

A third zone is assembled into a square in Fig. 8, but the parts of the Fermi surface still appear disconnected. When we look at it in the periodic zone scheme (Fig. 9), the Fermi surface forms a lattice of rosettes. 

## Nearly Free Electrons

How do we go from Fermi surfaces for free electrons to Fermi surfaces for nearly free electrons? We can make approximate constructions freehand by the use of four facts: 

• The interaction of the electron with the periodic potential of the crystal creates energy gaps at the zone boundaries. 

• Almost always the Fermi surface will intersect zone boundaries perpendicularly. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/e19ea4a74b559a85d36272a2110820810bca887aed3627a99c278bcda9459da3.jpg)



2nd zone


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/4daa581f0335a9c4aa8375cf64e1521f07818610da303bd49c4041e15cb9932b.jpg)



3rd zone



Figure 10 Qualitative impression of the effect of a weak periodic crystal potential on the Fermi surface of Fig. 8. At one point on each Fermi surface we have shown the vector gradk-. In the second zone the energy increases toward the interior of the figure, and in the third zone the energy increases toward the exterior. The shaded regions are filled with electrons and are lower in energy than the unshaded regions. We shall see that a Fermi surface like that of the third zone is electronlike, whereas one like that of the second zone is holelike.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/4618bda1f7ad0638924e0a96f18ad93d12e2a6f69665888bcad9caedeeecd73b.jpg)



Figure 11 Harrison construction of free electron Fermi surfaces on the second, third, and fourth zones for a square lattice. The Fermi surface encloses the entire first zone, which therefore is filled with electrons.


• The crystal potential will round out sharp corners in the Fermi surfaces. 

• The total volume enclosed by the Fermi surface depends only on the electron concentration and is independent of the details of the lattice interaction. 

We cannot make quantitative statements without calculation, but qualitatively we expect the Fermi surfaces in the second and third zones of Fig. 8 to be changed as shown in Fig. 10. 

Freehand impressions of the Fermi surfaces derived from free electron surfaces are useful. Fermi surfaces for free electrons are constructed by a procedure credited to Harrison, Fig. 11. The reciprocal lattice points are determined, and a free electron sphere of radius appropriate to the electron concentration is drawn around each point. Any point in k space that lies within at least one sphere corresponds to an occupied state in the first zone. Points within at least two spheres correspond to occupied states in the second zone, and similarly for points in three or more spheres. 

We said earlier that the alkali metals are the simplest metals, with weak interactions between the conduction electrons and the lattice. Because the alkalis have only one valence electron per atom, the first Brillouin zone boundaries are distant from the approximately spherical Fermi surface that fills onehalf of the volume of the zone. It is known by calculation and experiment that the Fermi surface of Na is closely spherical, and that the Fermi surface for Cs is deformed by perhaps 10 percent from a sphere. 

The divalent metals Be and Mg also have weak lattice interactions and nearly spherical Fermi surfaces. But because they have two valence electrons each, the Fermi surface encloses twice the volume in k space as for the alkalis. That is, the volume enclosed by the Fermi surface is exactly equal to that of a zone, but because the surface is spherical it extends out of the first zone and into the second zone. 

# ELECTRON ORBITS, HOLE ORBITS, AND OPEN ORBITS

We saw in Eq. (8.7) that electrons in a static magnetic field move on a curve of constant energy on a plane normal to B. An electron on the Fermi surface will move in a curve on the Fermi surface, because this is a surface of constant energy. Three types of orbits in a magnetic field are shown in Fig. 12. 

The closed orbits of (a) and (b) are traversed in opposite senses. Because particles of opposite charge circulate in a magnetic field in opposite senses, we say that one orbit is electronlike and the other orbit is holelike. Electrons in holelike orbits move in a magnetic field as if endowed with a positive charge. This is consistent with the treatment of holes in Chapter 8. 

In (c) the orbit is not closed: the particle on reaching the zone boundary at A is instantly folded back to B, where B is equivalent to $B ^ { \prime }$ because 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/6737609d7c5be16f1aa6a2deb4840dfbedfec9eaab96640313eb969f79ee5916.jpg)



Figure 12 Motion in a magnetic field of the wavevector of an electron on the Fermi surface, in (a) and (b) for Fermi surfaces topologically equivalent to those of Fig. 10. In (a) the wavevector moves around the orbit in a clockwise direction; in (b) the wavevector moves around the orbit in a counter-clockwise direction. The direction in (b) is what we expect for a free electron of charge $- { e } ;$ the smaller k values have the lower energy, so that the filled electron states lie inside the Fermi surface. We call the orbit in (b) electronlike. The sense of the motion in a magnetic field is opposite in (a) to that in (b), so that we refer to the orbit in (a) as holelike. A hole moves as a particle of positive charge e. In (c) for a rectangular zone we show the motion on an open orbit in the periodic zone scheme. An open orbit is topologically intermediate between a hole orbit and an electron orbit.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/1ae964cef04eced16bfb2523b9d0a76b76d7572522186a995a29a4248d896886.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/98654462fbc81c66262929d27f2d9943e323cbb7e5f67df471e7d222bb852302.jpg)



(b)



Figure 13 (a) Vacant states at the corners of an almost-filled band, drawn in the reduced zone scheme. (b) In the periodic zone scheme the various parts of the Fermi surface are connected. Each circle forms a holelike orbit. The different circles are entirely equivalent to each other, and the density of states is that of a single circle. (The orbits need not be true circles: for the lattice shown it is only required that the orbits have fourfold symmetry.)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/7d549e7e434133c6fab83cb673a583a51c8e81fb00688d80b25f288c190d46b2.jpg)



Figure 14 Vacant states near the top of an almost filled band in a twodimensional crystal. This figure is equivalent to Fig. 12a.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/2f08334aeeb032b5ff4cf39aa223d2c46fffc694e87c0c595f6c765c70ddfb99.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/ce126b2f4bd44892653372d5fc60d4aea370c6f35e61a0844580cfb721b1e486.jpg)



(b)



Figure 15 Constant energy surface in the Brillouin zone of a simple cubic lattice, for the assumed energy band $\epsilon _ { k } = - \alpha - 2 \gamma ($ (cos $k _ { x } a +$ cos $k _ { y } a + \cos { k _ { z } a ) }$ . (a) Constant energy surface $\epsilon = - \alpha .$ . The filled volume contains one electron per primitive cell. (b) The same surface exhibited in the periodic zone scheme. The connectivity of the orbits is clearly shown. Can you find electron, hole, and open orbits for motion in a magnetic field Bzˆ ? (A. Sommerfeld and H. A. Bethe.)


they are connected by a reciprocal lattice vector. Such an orbit is called an open orbit. Open orbits have an important effect on the magnetoresistance. 

Vacant orbitals near the top of an otherwise filled band give rise to holelike orbits, as in Figs. 13 and 14. A view of a possible energy surface in three dimensions is given in Fig. 15. 

Orbits that enclose filled states are electron orbits. Orbits that enclose empty states are hole orbits. Orbits that move from zone to zone without closing are open orbits. 

# CALCULATION OF ENERGY BANDS

Wigner and Seitz, who in 1933 performed the first serious band calculations, refer to afternoons spent on the manual desk calculators of those days, using one afternoon for a trial wavefunction. Here we limit ourselves to three introductory methods: the tight-binding method, useful for interpolation; the Wigner-Seitz method, useful for the visualization and understanding of the alkali metals; and the pseudopotential method, utilizing the general theory of Chapter 7, which shows the simplicity of many problems. 

## Tight Binding Method for Energy Bands

Let us start with neutral separated atoms and watch the changes in the atomic energy levels as the charge distributions of adjacent atoms overlap when the atoms are brought together to form a crystal. Consider two hydrogen atoms, each with an electron in the 1s ground state. The wavefunctions $\psi _ { A } , \psi _ { B }$ on the separated atoms are shown in Fig. 16a. 

As the atoms are brought together, their wavefunctions overlap. We consider the two combinations $\psi _ { A } \pm \psi _ { B }$ . Each combination shares an electron with the two protons, but an electron in the state $\psi _ { A } + \psi _ { B }$ will have a somewhat lower energy than in the state $\psi _ { A } - \psi _ { B }$ . 

In $\psi _ { A } + \psi _ { B }$ the electron spends part of the time in the region midway between the two protons, and in this region it is in the attractive potential of both protons at once, thereby increasing the binding energy. In $\psi _ { A } - \psi _ { B }$ the probability density vanishes midway between the nuclei; an extra binding does not appear. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/afbcc22a4ee960bfc5cc41c176dbaba8ef7101fa201ec8991123a44e24767a42.jpg)



Figure 16 (a) Schematic drawing of wavefunctions of electrons on two hydrogen atoms at large separation. (b) Ground state wavefunction at closer separation. (c) Excited state wavefunction.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/275c3f066c1eb1492beaf8a6f64d1356338f8e0e05b22dfd0ced5869deffef70.jpg)



Figure 17 The 1s band of a ring of 20 hydrogen atoms; the one-electron energies are calculated in the tight-binding approximation with the nearest-neighbor overlap integral of $\operatorname { E q } .$ (9).


As two atoms are brought together, two separated energy levels are formed for each level of the isolated atom. For N atoms, N orbitals are formed for each orbital of the isolated atom (Fig. 17). 

As free atoms are brought together, the coulomb interaction between the atom cores and the electron splits the energy levels, spreading them into bands. Each state of given quantum number of the free atom is spread in the crystal into a band of energies. The width of the band is proportional to the strength of the overlap interaction between neighboring atoms. 

There will also be bands formed from $p , d , \ldots$ . states $( l = 1 , 2 , . . . . )$ of the free atoms. States degenerate in the free atom will form different bands. Each will not have the same energy as any other band over any substantial range of the wavevector. Bands may coincide in energy at certain values of k in the Brillouin zone. 

The approximation that starts out from the wavefunctions of the free atoms is known as the tight-binding approximation or the LCAO (linear combination of atomic orbitals) approximation. The approximation is quite good for the inner electrons of atoms, but it is not often a good description of the conduction electrons themselves. It is used to describe approximately the d bands of the transition metals and the valence bands of diamondlike and inert gas crystals. 

Suppose that the ground state of an electron moving in the potential $U ( \mathbf { r } )$ of an isolated atom is $\varphi ( \mathbf { r } )$ , an s state. The treatment of bands arising from degenerate $( p , d , \ldots )$ atomic levels is more complicated. If the influence of one atom on another is small, we obtain an approximate wavefunction for one electron in the whole crystal by taking 

$$
\psi_ {\mathbf {k}} (\mathbf {r}) = \sum_ {j} C _ {\mathbf {k} j} \varphi (\mathbf {r} - \mathbf {r} _ {j}), \tag {4}
$$

where the sum is over all lattice points. We assume the primitive basis contains one atom. This function is of the Bloch form (7.7) if $\mathbf { \bar { C } _ { k } } _ { j } = N ^ { - 1 / 2 } \ e ^ { \mathrm { i } \mathbf { k } \cdot \mathbf { r } }$ , which gives, for a crystal of N atoms, 

$$
\psi_ {\mathbf {k}} (\mathbf {r}) = N ^ {- 1 / 2} \sum_ {j} \exp (i \mathbf {k} \cdot \mathbf {r} _ {j}) \varphi (\mathbf {r} - \mathbf {r} _ {j}). \tag {5}
$$

We prove (5) is of the Bloch form. Consider a translation T connecting two lattice points: 

$$
\begin{array}{l} \psi_ {\mathbf {k}} (\mathbf {r} + \mathbf {T}) = N ^ {- 1 / 2} \sum_ {j} \exp (i \mathbf {k} \cdot \mathbf {r} _ {j}) \varphi (\mathbf {r} + \mathbf {T} - \mathbf {r} _ {j}) \\ = \exp (i \mathbf {k} \cdot \mathbf {T}) N ^ {- 1 / 2} \sum_ {j} \exp [ i \mathbf {k} \cdot (\mathbf {r} _ {j} - \mathbf {T}) ] \varphi [ \mathbf {r} - (\mathbf {r} _ {j} - \mathbf {T}) ] \tag {6} \\ = \exp (i \mathbf {k} \cdot \mathbf {T}) \psi_ {\mathbf {k}} (\mathbf {r}), \\ \end{array}
$$

exactly the Bloch condition. 

We find the first-order energy by calculating the diagonal matrix elements of the hamiltonian of the crystal: 

$$
\langle \mathbf {k} | H | \mathbf {k} \rangle = N ^ {- 1} \sum_ {j} \sum_ {m} \exp [ i \mathbf {k} \cdot (\mathbf {r} _ {j} - \mathbf {r} _ {m}) ] \left\langle \varphi_ {m} | H | \varphi_ {j} \right\rangle , \tag {7}
$$

where $\varphi _ { m } \equiv \varphi ( { \bf r } - { \bf r } _ { m } )$ . Writing $\pmb { \rho } _ { m } = \mathbf { r } _ { m } - \mathbf { r } _ { j }$ 

$$
\langle \mathbf {k} | H | \mathbf {k} \rangle = \sum_ {m} \exp (- i \mathbf {k} \cdot \boldsymbol {\rho} _ {m}) \int d V \varphi^ {*} (\mathbf {r} - \boldsymbol {\rho} _ {m}) H \varphi (\mathbf {r}). \tag {8}
$$

We now neglect all integrals in (8) except those on the same atom and those between nearest neighbors connected by -. We write 

$$
\int d V \varphi^ {*} (\mathbf {r}) H \varphi (\mathbf {r}) = - \alpha ; \quad \int d V \varphi^ {*} (\mathbf {r} - \boldsymbol {\rho}) H \varphi (\mathbf {r}) = - \gamma ; \tag {9}
$$

and we have the first-order energy, provided k|k  1: 

$$
\langle \mathbf {k} | H | \mathbf {k} \rangle = - \alpha - \gamma \sum_ {m} \exp (- i \mathbf {k} \cdot \boldsymbol {\rho} _ {m}) = \epsilon_ {\mathbf {k}}. \tag {10}
$$

The dependence of the overlap energy  on the interatomic separation  can be evaluated explicitly for two hydrogen atoms in 1s states. In rydberg energy units, $\mathrm { R y } = m e ^ { 4 } / 2 \hbar ^ { 2 }$ we have, 

$$
\gamma (\mathrm{Ry}) = 2 (1 + \rho / a _ {0}) \exp (- \rho / a _ {0}), \tag {11}
$$

where $a _ { 0 } = \hbar ^ { 2 } / m e ^ { 2 }$ The overlap energy decreases exponentially with the. separation. 

For a simple cubic structure the nearest-neighbor atoms are at 

$$
\boldsymbol {\rho} _ {m} = (\pm a, 0, 0) ; \quad (0, \pm a, 0) ; \quad (0, 0, \pm a) , \tag {12}
$$

so that (10) becomes 

$$
\epsilon_ {\mathrm{k}} = - \alpha - 2 \gamma (\cos k _ {x} a + \cos k _ {y} a + \cos k _ {z} a). \tag {13}
$$

Thus the energies are confined to a band of width 12. The weaker the overlap, the narrower is the energy band. A constant energy surface is shown in Fig. 15. For $k a \ll 1 , \epsilon _ { k } \simeq - \alpha - 6 \gamma + \gamma k ^ { 2 } a ^ { 2 }$ . The effective mass is $m ^ { * } =$ $\hbar ^ { 2 } / 2 \gamma a ^ { 2 }$ When the overlap integral  is small, the band is narrow and the effec-. tive mass is high. 

We considered one orbital of each free atom and obtained one band $\epsilon _ { \mathbf { k } } .$ The number of orbitals in the band that corresponds to a nondegenerate atomic level is 2N, for N atoms. We see this directly: values of k within the first Brillouin zone define independent wavefunctions. The simple cubic zone has $- \pi / a < k _ { x } < \pi / a$ , etc. The zone volume is $8 \pi ^ { 3 } / a ^ { 3 }$ . The number of orbitals (counting both spin orientations) per unit volume of k space is $V / 4 { \pi } ^ { 3 } .$ , so that the number of orbitals is $2 V / a ^ { 3 }$ . Here V is the volume of the crystal, and $1 / a ^ { 3 }$ is the number of atoms per unit volume. Thus there are 2N orbitals. 

For the fcc structure with eight nearest neighbors, 

$$
\epsilon_ {\mathbf {k}} = - \alpha - 8 \gamma \cos \frac {1}{2} k _ {x} a \cos \frac {1}{2} k _ {y} a \cos \frac {1}{2} k _ {z} a. \tag {14}
$$

For the fcc structure with 12 nearest neighbors, 

$$
\epsilon_ {\mathbf {k}} = - \alpha - 4 \gamma (\cos \frac {1}{2} k _ {y} a \cos \frac {1}{2} k _ {z} a + \cos \frac {1}{2} k _ {z} a \cos \frac {1}{2} k _ {x} a + \cos \frac {1}{2} k _ {x} a \cos \frac {1}{2} k _ {y} a). \tag {15}
$$

A constant energy surface is shown in Fig. 18. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/bb525faff789dc8a4c418c2ea84935ed5c4f5d0edad347190a7104630546513e.jpg)



Figure 18 A constant energy surface of an fcc crystal structure, in the nearest-neighbor tight-binding approximation. The surface shown has $\epsilon = \bar { \bf \alpha } - \alpha + 2 | \gamma |$ .


## Wigner-Seitz Method

Wigner and Seitz showed that for the alkali metals there is no inconsistency between the electron wavefunctions of free atoms and the nearly free electron model of the band structure of a crystal. Over most of a band the energy may depend on the wavevector nearly as for a free electron. However, the Bloch wavefunction, unlike a plane wave, will pile up charge on the positive ion cores as in the atomic wavefunction. 

A Bloch function satisfies the wave equation 

$$
\left(\frac {1}{2 m} \mathbf {p} ^ {2} + U (\mathbf {r})\right) e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) = \epsilon_ {\mathbf {k}} e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}). \tag {16}
$$

With $\mathbf { p } \equiv - i \hbar$ grad, we have 

$$
\mathbf {p} e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) = \hbar \mathbf {k} e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) + e ^ {i \mathbf {k} \cdot \mathbf {r}} \mathbf {p} u _ {\mathbf {k}} (\mathbf {r});
$$

$$
\mathbf {p} ^ {2} e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) = (\hbar k) ^ {2} e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {\mathbf {k}} (\mathbf {r}) + e ^ {i \mathbf {k} \cdot \mathbf {r}} (2 \hbar \mathbf {k} \cdot \mathbf {p}) u _ {\mathbf {k}} (\mathbf {r}) + e ^ {i \mathbf {k} \cdot \mathbf {r}} \mathbf {p} ^ {2} u _ {\mathbf {k}} (\mathbf {r});
$$

thus the wave equation (16) may be written as an equation for $u _ { { \bf k } } \mathrm { : }$ 

$$
\left(\frac {1}{2 m} (\mathbf {p} + \hbar \mathbf {k}) ^ {2} + U (\mathbf {r})\right) u _ {\mathbf {k}} (\mathbf {r}) = \epsilon_ {\mathbf {k}} u _ {\mathbf {k}} (\mathbf {r}). \tag {17}
$$

At k  0 we have $\psi _ { 0 } = u _ { 0 } ( \mathbf { r } )$ , where $u _ { 0 } ( \mathbf { r } )$ has the periodicity of the lattice, sees the ion cores, and near them will look like the wavefunction of the free atom. 

It is much easier to find a solution at $\mathbf k = 0$ than at a general k, because at $\mathbf k = 0$ a nondegenerate solution will have the full symmetry of $U ( \mathbf { r } )$ , that is, of the crystal. We can then use $u _ { 0 } ( \mathbf { r } )$ to construct the approximate solution 

$$
\psi_ {\mathbf {k}} = \exp (i \mathbf {k} \cdot \mathbf {r}) u _ {0} (r). \tag {18}
$$

This is of the Bloch form, but $u _ { 0 }$ is not an exact solution of (17): it is a solution only if we drop the term in k-p. Often this term is treated as a perturbation, as in Problem 8. The k-p perturbation theory developed there is especially useful in finding the effective mass $m ^ { * }$ at a band edge. 

Because it takes account of the ion core potential the function (18) is a much better approximation than a plane wave to the correct wavefunction. The energy of the approximate solution depends on k as $( \hbar k ) ^ { 2 } / 2 m .$ exactly as, for the plane wave, even though the modulation represented by $u _ { 0 } ( \mathbf { r } )$ may be very strong. Because $u _ { 0 }$ is a solution of 

$$
\left(\frac {1}{2 m} \mathbf {p} ^ {2} + U (\mathbf {r})\right) u _ {0} (\mathbf {r}) = \epsilon_ {0} u _ {0} (\mathbf {r}), \tag {19}
$$

the function (18) has the energy expectation value $\epsilon _ { 0 } + ( \hbar ^ { 2 } k ^ { 2 } / 2 m )$ The . function $u _ { 0 } ( \mathbf { r } )$ often will give us a good picture of the charge distribution within a cell. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/60cd8611a44a48ce6cd14e81e0b7aeb796fdc69e9d4e594ca91bfc8159706609.jpg)



Figure 19 Radial wavefunctions for the 3s orbital of free sodium atom and for the 3s conduction band in sodium metal. The wavefunctions, which are not normalized here, are found by integrating the Schrödinger equation for an electron in the potential well of an $\mathrm { N a ^ { + } }$ ion core. For the free atom the wavefunction is integrated subject to the usual Schrödinger boundary condition $\psi ( r ) \to 0$ as $r \to \infty$ ; the energy eigenvalue is $- 5 . 1 5 \mathrm { e V } .$ The wavefunction for wavevector $k = 0$ in the metal is subject to the Wigner-Seitz boundary condition that $d \psi / d r = 0$ when $r$ is midway between neighboring atoms; the energy of this orbital $\mathrm { i s ~ - 8 . 2 ~ e V } ,$ , considerably lower than for the free atom. The orbitals at the zone boundary are not filled in sodium; their energy is 2.7 eV. (After E. Wigner and F. Seitz.)


Wigner and Seitz developed a simple and fairly accurate method of calculating $u _ { 0 } ( \mathbf { r } )$ . Figure 19 shows the Wigner-Seitz wavefunction for $\mathbf k = 0$ in the 3s conduction band of metallic sodium. The function is practically constant over 0.9 of the atomic volume. To the extent that the solutions for higher k may be approximated by $\exp ( i { \bf k } \cdot { \bf r } ) u _ { 0 } ( { \bf r } )$ , the wavefunctions in the conduction band will be similar to plane waves over most of the atomic volume, but increase markedly and oscillate within the ion core. 

Cohesive Energy. The stability of the simple metals with respect to free atoms is caused by the lowering of the energy of the Bloch orbital with $\mathbf k = 0$ in the crystal compared to the ground valence orbital of the free atom. The effect is illustrated in Fig. 19 for sodium and in Fig. 20 for a linear periodic potential of attractive square wells. The ground orbital energy is much lower (because of lower kinetic energy) at the actual spacing in the metal than for isolated atoms. 

A decrease in ground orbital energy will increase the binding. The decrease in ground orbital energy is a consequence of the change in the boundary condition on the wavefunction: The Schrödinger boundary condition for the free atom is $\psi ( \mathbf { r } ) \to 0$ as $r \to \infty$ . In the crystal the $\mathbf k = 0$ wavefunction $u _ { 0 } ( \mathbf { r } )$ has the symmetry of the lattice and is symmetric about $\mathrm { { r } = 0 }$ . To have this, the normal derivative of $\psi$ must vanish across every plane midway between adjacent atoms. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/a48fa174a2a0f2cf7ea889ab07b0ce5de1be449f7ec3c896f607b9b8e3ce6f51.jpg)



Figure 20 Ground orbital $( k = 0 )$ energy for an electron in a periodic square well potential of depth $\left. U _ { 0 } \right. = 2 \hbar ^ { 2 } / m a ^ { 2 } .$ The energy is lowered as the wells come closer together. Here a is held constant and b is varied. Large b/a corresponds to separated atoms. (Courtesy of C. Y. Fong.)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/bc043fcb4840bd595d199e89fcad13ea3c88eefcf5857ed2befff328421df665.jpg)



Figure 21 Cohesive energy of sodium metal is the difference between the average energy of an electron in the metal $\mathrm { ( - 6 . 3 e V ) }$ and the ground state energy (5.15 eV) of the valence 3s electron in the free atom, referred to an $\mathrm { N a ^ { + } }$ ion plus free electron at infinite separation.


In a spherical approximation to the shape of the smallest Wigner-Seitz cell we use the Wigner-Seitz boundary condition 

$$
(d \psi / d r) _ {r _ {0}} = 0, \tag {20}
$$

where $r _ { 0 }$ is the radius of a sphere equal in volume to a primitive cell of the lattice. In sodium, $r _ { 0 } = 3 . 9 5$ Bohr units, or 2.08 $\mathring \mathrm { A } ;$ the half distance to a nearest neighbor is 1.86 Å. The spherical approximation is not bad for fcc and bcc structures. The boundary condition allows the ground orbital wavefunction to have much less curvature than the free atom boundary condition. Much less curvature means much less kinetic energy. 

In sodium the other filled orbitals in the conduction band can be represented in a rough approximation by wavefunctions of the form (18), with 

$$
\psi_ {\mathbf {k}} = e ^ {i \mathbf {k} \cdot \mathbf {r}} u _ {0} (\mathbf {r}); \quad \epsilon_ {\mathbf {k}} = \epsilon_ {0} + \frac {\hbar^ {2} k ^ {2}}{2 m}.
$$

The Fermi energy is 3.1 eV, from Table 6.1. The average kinetic energy per electron is 0.6 of the Fermi energy, or 1.9 eV. Because $\epsilon _ { 0 } = - 8 . 2 \ \mathrm { e V }$ at $\mathbf { k } = 0 _ { ; }$ the average electron energy is $\langle \epsilon _ { \mathrm { k } } \rangle = - 8 . 2 + 1 . 9 = - 6 . 3 ~ \mathrm { e V } ,$ compared with 5.15 eV for the valence electron of the free atom, Fig. 21. 

We therefore estimate that sodium metal is stable by about 1.1 eV with respect to the free atom. This result agrees well with the experimental value 1.13 eV. 

## Pseudopotential Methods

Conduction electron wavefunctions are usually smoothly varying in the region between the ion cores, but have a complicated nodal structure in the region of the cores. This behavior is illustrated by the ground orbital of sodium, Fig. 19. It is helpful to view the nodes in the conduction electron wavefunction in the core region as created by the requirement that the function be orthogonal to the wavefunctions of the core electrons. This all comes out of the Schrödinger equation, but we can see that we need the flexibility of two nodes in the 3s conduction orbital of Na in order to be orthogonal both to the 1s core orbital with no nodes and the 2s core orbital with one node. 

Outside the core the potential energy that acts on the conduction electron is relatively weak: the potential energy is only the coulomb potential of the singly-charged positive ion cores and is reduced markedly by the electrostatic screening of the other conduction electrons, Chapter 14. In this outer region the conduction electron wavefunctions are as smoothly varying as plane waves. 

If the conduction orbitals in this outer region are approximately plane waves, the energy must depend on the wavevector approximately as $\epsilon _ { \mathbf { k } } = \hbar ^ { 2 } k ^ { 2 } / 2 m$ as for free electrons. But how do we treat the conduction orbitals in the core region where the orbitals are not at all like plane waves? 

What goes on in the core is largely irrelevant to the dependence of - on k. Recall that we can calculate the energy by applying the hamiltonian operator to an orbital at any point in space. Applied in the outer region, this operation will give an energy nearly equal to the free electron energy. 

This argument leads naturally to the idea that we might replace the actual potential energy (and filled shells) in the core region by an effective potential energy1 that gives the same wavefunctions outside the core as are given by the actual ion cores. It is startling to find that the effective potential or 

1 J. C. Phillips and L. Kleinman, Phys. Rev. 116, 287 (1959); E. Antoncik, J. Phys. Chem. Solids 10, 314 (1959). The general theory of pseudopotentials is discussed by B. J. Austin, V. Heine, and L. J. Sham, Phys. Rev. 127, 276 (1962); see also Vol. 24 of Solid state physics. The utility of the empty core model has been known for many years: it goes back to E. Fermi, Nuovo Cimento 2, 157 (1934); H. Hellmann, Acta Physiochimica URSS 1, 913 (1935); and H. Hellmann and W. Kassatotschkin, J. Chem. Phys. 4, 324 (1936), who wrote “Since the field of the ion determined in this way runs a rather flat course, it is sufficient in the first approximation to set the valence electron in the lattice equal to a plane wave.” 

pseudopotential that satisfies this requirement is nearly zero. This conclusion about pseudopotentials is supported by a large amount of empirical experience as well as by theoretical arguments. The result is referred to as the cancellation theorem. 

The pseudopotential for a problem is not unique nor exact, but it may be very good. On the Empty Core Model (ECM) we can even take the unscreened pseudopotential to be zero inside some radius $R _ { e }$ : 

$$
U (r) = \left\{ \begin{array}{l l} 0, & \text { for } r <   R _ {e}; \\ - e ^ {2} / r, & \text { for } r > R _ {e}. \end{array} \right. \tag {21}
$$

This potential should now be screened as described in Chapter 10. Each component ${ \cal U } ( { \bf K } )$ of $U ( r )$ is to be divided by the dielectric constant $\epsilon ( \mathbf { K } )$ of the electron gas. If, just as an example, we use the Thomas-Fermi dielectric function (14.33), we obtain the screened pseudopotential plotted in Fig. 22a. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/fff3d0e11dfe6f80dc274f4b4549ba77643e03be045552b54b4f2d7acd6ec8c8.jpg)



Figure 22a Pseudopotential for metallic sodium, based on the empty core model and screened by the Thomas-Fermi dielectric function. The calculations were made for an empty core radius $\dot { R _ { e } } = 1 . 6 6 a _ { 0 } ,$ where $a _ { 0 }$ is the Bohr radius, and for a screening parameter $k _ { s } a _ { 0 } = 0 . \bar { 7 } 9$ . The dashed curve shows the assumed unscreened potential, as from (21). The dotted curve is the actual potential of the ion core; other values of $U ( r )$ are $- 5 0 . 4 , \ : - 1 1 . 6$ , and $- 4 . 6 .$ , for $r = 0 . 1 5 , 0 . 4 .$ and $0 . 7 ,$ respectively. Thus the actual potential of the ion (chosen to fit the energy levels of the free atom) is very much larger than the pseudopotential, over 200 times larger at $r = 0 . 1 5$ .


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/a4be369b072585e9f4806d8f0f2a0c85d3b1329795ac1923413cd6b02af53554.jpg)



Figure 22b A typical reciprocal space pseudopotential. Values of U(k) for wavevectors equal to the reciprocal lattice vectors, G, are indicated by the dots. For very small k the potential approaches (2/3) times the Fermi energy, which is the screened-ion limit for metals. (After M. L. Cohen.)


The pseudopotential as drawn is much weaker than the true potential, but the pseudopotential was adjusted so that the wavefunction in the outer region is nearly identical to that for the true potential. In the language of scattering theory, we adjust the phase shifts of the pseudopotential to match those of the true potential. 

Calculation of the band structure depends only on the Fourier components of the pseudopotential at the reciprocal lattice vectors. Usually only a few values of the coefficients U(G) are needed to get a good band structure: see the U(G) in Fig. 22b. These coefficients are sometimes calculated from model potentials, and sometimes they are obtained from fits of tentative band structures to the results of optical measurements. Good values of U(0) can be estimated from first principles; it is shown in (14.43) that for a screened coulomb potential $U ( 0 ) = - \frac { 2 } { 3 } \epsilon _ { F }$ . 

In the remarkably successful Empirical Pseudopotential Method (EPM) the band structure is calculated using a few coefficients U(G) deduced from theoretical fits to measurements of the optical reflectance and absorption of crystals, as discussed in Chapter 15. Charge density maps can be plotted from the wavefunctions generated by the EPM—see Fig. 3.11. The results are in excellent agreement with x-ray diffraction determinations; such maps give an understanding of the bonding and have great predictive value for proposed new structures and compounds. 

The EPM values of the coefficients U(G) often are additive in the contributions of the several types of ions that are present. Thus it may be possible to construct the U(G) for entirely new structures, starting from results on known structures. Further, the pressure dependence of a band structure may be determined when it is possible to estimate from the form of the U(r) curve the dependence of U(G) on small variations of G. 

It is often possible to calculate band structures, cohesive energy, lattice constants, and bulk moduli from first principles. In such ab initio pseudopotential calculations the basic inputs are the crystal structure type and the atomic number, along with well-tested theoretical approximations to exchange energy terms. This is not the same as calculating from atomic number alone, but it is the most reasonable basis for a first-principles calculation. The results of Yin and Cohen are compared with experiment in the table that follows. 

<table><tr><td></td><td>Lattice constant (Å)</td><td>Cohesive energy (eV)</td><td>Bulk modulus (Mbar)</td></tr><tr><td colspan="4">Silicon</td></tr><tr><td>Calculated</td><td>5.45</td><td>4.84</td><td>0.98</td></tr><tr><td>Experimental</td><td>5.43</td><td>4.63</td><td>0.99</td></tr><tr><td colspan="4">Germanium</td></tr><tr><td>Calculated</td><td>5.66</td><td>4.26</td><td>0.73</td></tr><tr><td>Experimental</td><td>5.65</td><td>3.85</td><td>0.77</td></tr><tr><td colspan="4">Diamond</td></tr><tr><td>Calculated</td><td>3.60</td><td>8.10</td><td>4.33</td></tr><tr><td>Experimental</td><td>3.57</td><td>7.35</td><td>4.43</td></tr></table>

# EXPERIMENTAL METHODS IN FERMI SURFACE STUDIES

Powerful experimental methods have been developed for the determination of Fermi surfaces. The methods include magnetoresistance, anomalous skin effect, cyclotron resonance, magneto-acoustic geometric effects, the Shubnikow-de Haas effect, and the de Haas-van Alphen effect. Further information on the momentum distribution is given by positron annihilation, Compton scattering, and the Kohn effect. 

We propose to study one method rather thoroughly. All the methods are useful, but need detailed theoretical analysis. We select the de Haas-van Alphen effect because it exhibits very well the characteristic periodicity in 1/B of the properties of a metal in a uniform magnetic field. 

## Quantization of Orbits in a Magnetic Field

The momentum p of a particle in a magnetic field is the sum (Appendix G) of two parts, the kinetic momentum $\mathbf { p } _ { \mathrm { k i n } } = m \mathbf { \mathbf { v } } = \hbar \mathbf { k }$ and the potential momentum or field momentum ${ \bf p } _ { \mathrm { f i e l d } } = q { \bf A } / c$ , where q is the charge. The vector potential is related to the magnetic field by B  curl A. The total momentum is 

$$
\mathbf {p} = \mathbf {p} _ {\text {kin}} + \mathbf {p} _ {\text {field}} = \hbar \mathbf {k} + q \mathbf {A} / c. \tag {22}
$$

In SI the factor $c ^ { - 1 }$ is omitted. 

Following the semiclassical approach of Onsager and Lifshitz, we assume that the orbits in a magnetic field are quantized by the Bohr-Sommerfeld relation 

$$
\oint \mathbf {p} \cdot d \mathbf {r} = (n + \gamma) 2 \pi h, \tag {23}
$$

when n is an integer and  is a phase correction that for free electrons has the value . Then12 

$$
\oint \mathbf {p} \cdot d \mathbf {r} = \oint \hbar \mathbf {k} \cdot d \mathbf {r} + \frac {q}{c} \oint \mathbf {A} \cdot d \mathbf {r}. \tag {24}
$$

The equation of motion of a particle of charge q in a magnetic field is 

$$
\hbar \frac {d \mathbf {k}}{d t} = \frac {q}{c} \frac {d \mathbf {r}}{d t} \times \mathbf {B}. \tag {25a}
$$

We integrate with respect to time to give 

$$
\hbar \mathbf {k} = \frac {q}{c} \mathbf {r} \times \mathbf {B},
$$

apart from an additive constant which does not contribute to the final result. 

Thus one of the path integrals in (24) is 

$$
\oint \hbar \mathbf {k} \cdot d \mathbf {r} = \frac {q}{c} \oint \mathbf {r} \times \mathbf {B} \cdot d \mathbf {r} = - \frac {q}{c} \mathbf {B} \cdot \oint \mathbf {r} \times d \mathbf {r} = - \frac {2 q}{c} \Phi , \tag {25b}
$$

where  is the magnetic flux contained within the orbit in real space. We have used the geometrical result that 

$$
\oint \mathbf {r} \times d \mathbf {r} = 2 \times (\text { area   enclosed   by   the   orbit }).
$$

The other path integral in (24) is 

$$
\frac {q}{c} \oint \mathbf {A} \cdot d \mathbf {r} = \frac {q}{c} \int \mathbf {c u r l} \mathbf {A} \cdot d \boldsymbol {\sigma} = \frac {q}{c} \int \mathbf {B} \cdot d \boldsymbol {\sigma} = \frac {q}{c} \Phi , \tag {25c}
$$

by the Stokes theorem. Here d is the area element in real space. The momentum path integral is the sum of (25b) and (25c): 

$$
\oint \mathbf {p} \cdot d \mathbf {r} = - \frac {q}{c} \boldsymbol {\Phi} = (n + \gamma) 2 \pi \hbar . \tag {26}
$$

It follows that the orbit of an electron is quantized in such a way that the flux through it is 

$$
\Phi_ {n} = (n + \gamma) (2 \pi \hbar c / e). \tag {27}
$$

The flux unit gauss cm2 or T m2 .2ce  4.14 
 10 7 

In the de Haas-van Alphen effect discussed below we need the area of the orbit in wavevector space. We obtained in (27) the flux through the orbit in real space. By (25a) we know that a line element r in the plane normal to B is related to k by $\Delta r = ( \hbar c / e B ) \Delta k$ so that the area, $S _ { n }$ in k space is related to the area $A _ { n }$ of the orbit in r space by 

$$
A _ {n} = (\hbar c / e B) ^ {2} S _ {n}. \tag {28}
$$

It follows that 

$$
\Phi_ {n} = \left(\frac {\hbar c}{e}\right) ^ {2} \frac {1}{B} S _ {n} = (n + \gamma) \frac {2 \pi \hbar c}{e}, \tag {29}
$$

from (27), whence the area of an orbit in k space will satisfy 

$$
S _ {n} = (n + \gamma) \frac {2 \pi e}{\hbar c} B. \tag {30}
$$

In Fermi surface experiments we may be interested in the increment B for which two successive orbits, n and n  1, have the same area in k space on the Fermi surface. The areas are equal when 

$$
S \left(\frac {1}{B _ {n + 1}} - \frac {1}{B _ {n}}\right) = \frac {2 \pi e}{\hbar c}, \tag {31}
$$

from (30). We have the important result that equal increments of 1/B reproduce similar orbits—this periodicity in 1/B is a striking feature of the magnetooscillatory effects in metals at low temperatures: resistivity, susceptibility, heat capacity. 

The population of orbits on or near the Fermi surface oscillates as B is varied, causing a wide variety of effects. From the period of the oscillation we reconstruct the Fermi surface. The result (30) is independent of the gauge of the vector potential used in the expression (22) for momentum; that is, p is not gauge invariant, but $S _ { n }$ is. Gauge invariance is discussed further in Chapter 10 and in Appendix G. 

## De Haas-van Alphen Effect

The de Haas-van Alphen effect is the oscillation of the magnetic moment of a metal as a function of the static magnetic field intensity. The effect can be observed in pure specimens at low temperatures in strong magnetic fields: we do not want the quantization of the electron orbits to be blurred by collisions, and we do not want the population oscillations to be averaged out by thermal population of adjacent orbits. 

The analysis of the dHvA effect is given for absolute zero in Fig. 23. The electron spin is neglected. The treatment is given for a two-dimensional (2D) system; in 3D we need only multiply the 2D wavefunction by plane wave factors $\exp ( i k _ { z } z )$ , where the magnetic field is parallel to the z axis. The area of an orbit in $k _ { x } , k _ { y }$ space is quantized as in (30). The area between successive orbits is 

$$
\Delta S = S _ {n} - S _ {n - 1} = 2 \pi e B / \hbar c. \tag {32}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/f24b7e43068b52894697977a642288bc751a4474654ae83a0a17a06db6cbaa15.jpg)



(a)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/c6a70409d59167b2ceeb7fce33680d5f90392e0c833d44c674d616f99046228f.jpg)



(e)



Figure 23 Explanation of the de Haas-van Alphen effect for a free electron gas in two dimensions in a magnetic field. The filled orbitals of the Fermi sea in the absence of a magnetic field are shaded in a and d. The energy levels in a magnetic field are shown in $b , c ,$ and e. In b the field has a value $B _ { 1 }$ such that the total energy of the electrons is the same as in the absence of a magnetic field: as many electrons have their energy raised as lowered by the orbital quantization in the magnetic field $B _ { 1 } .$ . When we increase the field to $B _ { 2 }$ the total electron energy is increased, because the uppermost electrons have their energy raised. In e for field $B _ { 3 }$ the energy is again equal to that for the field $B = 0$ . The total energy is a minimum at points such as $B _ { 1 } , B _ { 3 } , B _ { 5 } , . . . .$ , and a maximum near points such as $B _ { 2 } , B _ { 4 } , \ldots .$ .


The area in k space occupied by a single orbital is $( { 2 \pi } / { L } ) ^ { 2 }$ , neglecting spin, for a square specimen of side L. Using (32) we find that the number of free electron orbitals that coalesce in a single magnetic level is 

$$
D = (2 \pi e B / \hbar c) (L / 2 \pi) ^ {2} = \rho B, \tag {33}
$$

where $\rho = e L ^ { 2 } / 2 \pi \hbar c$ as in Fig. 24. Such a magnetic level is called a Landau, level. 

The dependence of the Fermi level on B is dramatic. For a system of N electrons at absolute zero the Landau levels are entirely filled up to a magnetic quantum number we identify by s, where s is a positive integer. Orbitals at the next higher level s  1 will be partly filled to the extent needed to accommodate the electrons. The Fermi level will lie in the Landau level $s + 1$ if there are electrons in this level; as the magnetic field is increased the electrons move to lower levels. When $s + 1$ is vacated, the Fermi level moves down abruptly to the next lower level s. 

The electron transfer to lower Landau levels can occur because their degeneracy D increases as B is increased, as shown in Fig. 25. As B is 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/7fe8d1c1dd6675636b3067897c785787c2351baa0bfa37e0c5ee71ec86df20ef.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/a39caba4248ee7021d847f770ebfcd50058547c88714f6e5887b403eb99f4bfd.jpg)



(b)



Figure 24 (a) Allowed electron orbitals in two dimensions in absence of a magnetic field. (b) In a magnetic field the points which represent the orbitals of free electrons may be viewed as restricted to circles in the former $k _ { x } k _ { y }$ plane. The successive circles correspond to successive values of the quantum number n in the energy $( n - \frac { 1 } { 2 } ) k \omega _ { c }$ . The area between successive circles is


$$
\pi \Delta (k ^ {2}) = 2 \pi k (\Delta k) = (2 \pi m / \hbar^ {2}) \Delta \epsilon = 2 \pi m \omega_ {c} / \hbar - 2 \pi e B / \hbar c .
$$

The angular position of the points has no significance. The number of orbitals on a circle is constant and is equal to the area between successive circles times the number of orbitals per unit area in (a), or $( 2 \pi e \bar { B } / \hbar c ) ( L / 2 \pi ) ^ { 2 } = L ^ { 2 } e B / 2$ neglecting electron spin. c, 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/f73e7997fdfdadb1f265e725fee29f8266b3674d3bf45ec616fd065bc356af03.jpg)


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/64f0024941ca8b0eee8629db46d932fa1d95181b1aceefef01ed616b2bca70e8.jpg)



Figure 25 (a) The heavy line gives the number of particles in levels which are completely occupied in a magnetic field B, for a two-dimensional system with $N = 5 0$ and $\rho = 0 . 5 0$ . The shaded area gives the number of particles in levels partially occupied. The value of s denotes the quantum number of the highest level which is completely filled. Thus at $B = 4 0$ we have $s = 2 ;$ the levels $n = 1$ and $n = 2$ are filled and there are 10 particles in the level $n = 3 .$ At $B = 5 0$ the level $n = 3$ is empty. (b) The periodicity in 1/B is evident when the same points are plotted against 1/B.


increased there occur values of B at which the quantum number of the uppermost filled level decreases abruptly by unity. At the critical magnetic fields labeled $B _ { s }$ no level is partly occupied at absolute zero, so that 

$$
s \rho B _ {s} = N. \tag {34}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/3f602bafa9eea49a7106ad726b54b4a4e77798b7b918c6bc6ac85058a0c65661.jpg)



Figure 26 The upper curve is the total electronic energy versus 1/B. The oscillations in the energy U may be detected by measurement of the magnetic moment, given by  U/ B. The thermal and transport properties of the metal also oscillate as successive orbital levels cut through the Fermi level when the field is increased. The shaded region in the figure gives the contribution to the energy from levels that are only partly filled. The parameters for the figure are the same as for Fig. 25, and we have taken the units of B such that $B = \hbar \omega _ { c }$ .


The number of filled levels times the degeneracy at $B _ { s }$ must equal the number of electrons N. 

To show the periodicity of the energy as B is varied, we use the result that the energy of the Landau level of magnetic quantum number n is $E _ { n } = ( n - { \textstyle \frac { 1 } { 2 } } ) \hbar \omega _ { c }$ where, $\omega _ { c } = e B / m ^ { * } c$ is the cyclotron frequency. The result for $E _ { n }$ follows from the analogy between the cyclotron resonance orbits and the simple harmonic oscillator, but now we have found it convenient to start counting at $n = 1$ instead of at $n = 0$ . 

The total energy of the electrons in levels that are fully occupied is 

$$
\sum_ {n = 1} ^ {s} D \hbar \omega_ {c} (n - \frac {1}{2}) = \frac {1}{2} D \hbar \omega_ {c} s ^ {2}, \tag {35}
$$

where D is the number of electrons in each level. The total energy of the electrons in the partly occupied level $s + 1$ is 

$$
\hbar \omega_ {c} (s + \frac {1}{2}) (N - s D), \tag {36}
$$

where sD is the number of electrons in the lower filled levels. The total energy of the N electrons is the sum of (35) and (36), as in Fig. 26. 

The magnetic moment  of a system at absolute zero is given by $\mu =$  U/ B. The moment here is an oscillatory function of 1/B, Fig. 27. This os- cillatory magnetic moment of the Fermi gas at low temperatures is the de Haas-van Alphen effect. From (31) we see that the oscillations occur at equal intervals of 1/B such that 

$$
\Delta \left(\frac {1}{B}\right) = \frac {2 \pi e}{\hbar c S}, \tag {37}
$$

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/ba7debbc150ee739eb5871d7804e1922fec167ea71e2ce7b8fb83e67b6ce0821.jpg)



Figure 27 At absolute zero the magnetic moment is given by  U B. The energy plotted in Fig. 26 leads to the magnetic moment shown here, an oscillatory function of 1/B. In impure specimens the oscillations are smudged out in part because the energy levels are no longer sharply defined.



Figure 28 The orbits in the section $A A ^ { \prime }$ are extremal orbits: the cyclotron period is roughly constant over a reasonable section of the Fermi surface. Other sections such as $B B ^ { \prime }$ have orbits that vary in period along the section.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/e97b440337c8f117fd1a4bd8d5ac27464a6fbbff556918b2eb02f34c8ec81bdc.jpg)


where S is the extremal area (see below) of the Fermi surface normal to the direction of B. From measurements of $\Delta ( 1 / B )$ , we deduce the corresponding extremal areas S; thereby much can be inferred about the shape and size of the Fermi surface. 

Extremal Orbits. One point in the interpretation of the dHvA effect is subtle. For a Fermi surface of general shape the sections at different values of $k _ { \mathrm { B } }$ will have different periods. Here $k _ { B }$ is the component of k along the direction of the magnetic field. The response will be the sum of contributions from all sections or all orbits. But the dominant response of the system comes from orbits whose periods are stationary with respect to small changes in $k _ { B } .$ . Such orbits are called extremal orbits. Thus, in Fig. 28 the section AA dominates the observed cyclotron period. 

The argument can be put in mathematical form, but we do not give the proof here (QTS, p. 223). Essentially it is a question of phase cancellation; the contributions of different nonextremal orbits cancel, but near the extrema the phase varies only slowly and there is a net signal from these orbits. Sharp resonances are obtained even from complicated Fermi surfaces because the experiment selects the extermal orbits. 

Fermi Surface of Copper. The Fermi surface of copper (Fig. 29) is distinctly nonspherical: eight necks make contact with the hexagonal faces of the first Brillouin zone of the fcc lattice. The electron concentration in a monovalent metal with an fcc structure is $n = 4 / a ^ { 3 }$ ; there are four electrons in a cube of volume $a ^ { 3 } .$ The radius of a free electron Fermi sphere is 

$$
k _ {F} = (3 \pi^ {2} n) ^ {1 / 3} = (1 2 \pi^ {2} / a ^ {3}) ^ {1 / 3} \cong (4. 9 0 / a), \tag {38}
$$

and the diameter is 9.80/a. 

The shortest distance across the Brillouin zone (the distance between hexagonal faces) is $( 2 \pi / a ) ( 3 ) ^ { 1 / 2 } = 1 0 . 8 8 / a$ , somewhat larger than the diameter of the free electron sphere. The sphere does not touch the zone boundary, but we know that the presence of a zone boundary tends to lower the band energy near the boundary. Thus it is plausible that the Fermi surface should neck out to meet the closest (hexagonal) faces of the zone (Figs. 18 and 29). 

The square faces of the zone are more distant, with separation 12.57/a, and the Fermi surface does not neck out to meet these faces. 

EXAMPLE: Fermi Surface of Gold. In gold for quite a wide range of field directions Shoenberg finds the magnetic moment has a period of $2 \times 1 0 ^ { - 9 } \ \mathrm { g a u s s ^ { - 1 } }$ . This period corresponds to an extremal orbit of area 

$$
S = \frac {2 \pi e / \hbar c}{\Delta (1 / B)} \cong \frac {9 . 5 5 \times 1 0 ^ {7}}{2 \times 1 0 ^ {- 9}} \cong 4. 8 \times 1 0 ^ {1 6} \mathrm{cm} ^ {- 2}.
$$

From Table 6.1, we have $k _ { F } = 1 . 2 \times 1 0 ^ { 8 } \mathrm { c m } ^ { - 1 }$ for a free electron Fermi sphere for gold, or an extremal area of $4 . 5 \times 1 0 ^ { 1 6 } \ : \mathrm { c m } ^ { - 2 }$ , in general agreement with the experimental value. The actual periods reported by Shoenberg are $2 . 0 5 \times 1 0 ^ { - 9 } \mathrm { g a u s s } ^ { - 1 }$ and $1 . 9 5 \times 1 0 ^ { - 9 } \mathrm { { g a u s s } ^ { - 1 } }$ . In the [111] direction in Au a large period of $6 \times 1 0 ^ { - 8 } \mathrm { g a u s s ^ { - 1 } }$ is also found; the corresponding orbital area is $1 . 6 \times 1 0 ^ { 1 5 } \mathrm { ~ c m ^ { - 2 } }$ . This is the “neck” orbit N. Another extremal orbit, the “dog’s bone,” is shown in Fig. 30; its area in Au is about 0.4 of the belly area. Experimental results are shown in Fig. 31. To do the example in SI, drop c from the relation for S and use as the period $2 \times \mathrm { 1 0 ^ { - 5 } t e s l a ^ { - 1 } }$ . 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/54e77b67b521932c9743f514c0d7ed358fa5f7de2e70f3bb37aaefe78a676d6d.jpg)



Figure 29 Fermi surface of copper, after Pippard. The Brillouin zone of the fcc structure is the truncated octahedron derived in Chapter 2. The Fermi surface makes contact with the boundary at the center of the hexagonal faces of the zone, in the [111] directions in k space. Two “belly” extremal orbits are shown, denoted by B; the extremal “neck” orbit is denoted by N.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/674d39e361c96c6c67c4da621ee5ecf2ce39b4ea2744fd05feeb82d012c37670.jpg)



Figure 30 Dog’s bone orbit of an electron on the Fermi surface of copper or gold in a magnetic field. This orbit is classified as holelike because the energy increases toward the interior of the orbit.


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/21814a57fae5d552f8756cd4acc7adc4cd8166a8f7465e244dc3dcc3882a7d08.jpg)



Figure 31 De Haas-van Alphen effect in gold with B || [110]. The oscillation is from the dog’s bone orbit of Fig. 30. The signal is related to the second derivative of the magnetic moment with respect to field. The results were obtained by a field modulation technique in a high-homogeneity superconducting solenoid at about 1.2 K. (Courtesy of I. M. Templeton.)


The free electron Fermi sphere of aluminum fills the first zone entirely and has a large overlap into the second and third zones, Fig. 1. The third zone Fermi surface is quite complicated, even though it is just made up of certain pieces of the surface of the free electron sphere. The free electron model also gives small pockets of holes in the fourth zone, but when the lattice potential is taken into account these empty out, the electrons being added to the third zone. The general features of the predicted Fermi surface of aluminum are quite well verified by experiment. Figure 32 shows part of the free electron Fermi surface of magnesium. 

![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/3b250ad517cb9a026767ec5b5c14c7361c45a1ea06b365dfa241a946548e7274.jpg)



Figure 32 Multiply-connected hole surface of magnesium in bands 1 and 2, according to L. M. Falicov. (Drawing by Marta Puebla.)



High magnetic field


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/d0b076390159fa7abcb4b4156d9dc08303c5ab041d226e6673c001754ca41e4f.jpg)



Weak magnetic field


![image](https://cdn-mineru.openxlab.org.cn/result/2026-05-28/1bcd423f-8140-4b08-aff1-c0c43bf71638/f1c94fc72622e49fac82a3efb0543d0049be8146f7cb7c5e019a0b55629a1755.jpg)



(b)



Figure 33 Breakdown of band structure by a strong magnetic field. Brillouin zone boundaries are the light lines. The free electron orbits (a) in a strong field change connectivity in a weak field (b) to become open orbits in the first band and electron orbits in the second band. Both bands are mapped together.


Magnetic Breakdown. Electrons in sufficiently high magnetic fields will move in free particle orbits, the circular cyclotron orbits of Fig. 33a. Here the magnetic forces are dominant, and the lattice potential is a slight perturbation. In this limit the classification of the orbitals into bands may have little importance. However, we know that at low magnetic fields the motion is described by (8.7) with the band structure $\epsilon _ { \mathbf { k } }$ that obtains in the absence of a magnetic field. 

The eventual breakdown of this description as the magnetic field is increased is called magnetic breakdown. The passage to strong magnetic fields may drastically change the connectivity of the orbits, as in the figure. The onset of magnetic breakdown will be revealed by physical properties such as magnetoresistance that depend sensitively on the connectivity. The condition for magnetic breakdown is that $\hbar \omega _ { c } \epsilon _ { F } > E _ { \mathrm { g } } ^ { 2 } ,$ approximately. Here $\epsilon _ { F }$ is the free electron Fermi energy and $E _ { \mathrm { g } }$ is the energy gap. This condition is much milder, especially in metals with small gaps, than the naïve condition that the magnetic splitting exceed the gap.
c 

Small gaps may be found in hcp metals where the gap across the hexagonal face of the zone would be zero except for a small splitting introduced by the spin-orbit interaction. In Mg the splitting is of the order of $1 0 ^ { - 3 } \mathrm { e V } ;$ for this gap and $\epsilon _ { F } \sim 1 0 \mathrm { e V }$ the breakdown condition is $\hbar \omega _ { c } > 1 0 ^ { - 5 } \mathrm { e V , o r } B > 1 0 0 0 \mathrm { G }$ . 

# SUMMARY

• A Fermi surface is the surface in k space of constant energy equal to $\epsilon _ { F } .$ The Fermi surface separates filled states from empty states at absolute zero. The form of the Fermi surface is usually exhibited best in the reduced zone scheme, but the connectivity of the surfaces is clearest in the periodic zone scheme. 

• An energy band is a single branch of the $\epsilon _ { \mathbf { k } }$ versus k surface. 

• The cohesion of simple metals is accounted for by the lowering of energy of the $\mathbf k = 0$ conduction band orbital when the boundary conditions on the wavefunction are changed from Schrödinger to Wigner-Seitz. 

• The periodicity in the de Haas-van Alphen effect measures the extremal cross-section area S in k space of the Fermi surface, the cross section being taken perpendicular to B: 

$$
\Delta \left(\frac {1}{B}\right) = \frac {2 \pi e}{\hbar c S} . \tag {CGS}
$$

# Problems

1. Brillouin zones of rectangular lattice. Make a plot of the first two Brillouin zones of a primitive rectangular two-dimensional lattice with axes $a , b = 3 a$ . 

2. Brillouin zone, rectangular lattice. A two-dimensional metal has one atom of valency one in a simple rectangular primitive cell $a = 2 \mathring { \mathrm { A } } ; b = 4 \mathring { \mathrm { A } }$ . (a) Draw the first Brillouin zone. Give its dimensions, in $\mathrm { c m } ^ { - 1 }$ . (b) Calculate the radius of the free electron Fermi sphere, in $\mathrm { c m } ^ { - 1 }$ . (c) Draw this sphere to scale on a drawing of the first Brillouin zone. Make another sketch to show the first few periods of the free electron band in the periodic zone scheme, for both the first and second energy bands. Assume there is a small energy gap at the zone boundary. 

3. Hexagonal close-packed structure. Consider the first Brillouin zone of a crystal with a simple hexagonal lattice in three dimensions with lattice constants a and c. Let $\mathbf { G } _ { c }$ denote the shortest reciprocal lattice vector parallel to the c axis of the 

crystal lattice. (a) Show that for a hexagonal-close-packed crystal structure the Fourier component ${ \cal U } ( { \bf G } _ { c } )$ of the crystal potential U(r) is zero. (b) Is $U ( 2 \mathbf { G } _ { c } )$ also zero? (c) Why is it possible in principle to obtain an insulator made up of divalent atoms at the lattice points of a simple hexagonal lattice? (d) Why is it not possible to obtain an insulator made up of monovalent atoms in a hexagonal-close-packed structure? 

4. Brillouin zones of two-dimensional divalent metal. A two-dimensional metal in the form of a square lattice has two conduction electrons per atom. In the almost free electron approximation, sketch carefully the electron and hole energy surfaces. For the electrons choose a zone scheme such that the Fermi surface is shown as closed. 

5. Open orbits. An open orbit in a monovalent tetragonal metal connects opposite faces of the boundary of a Brillouin zone. The faces are separated by G $= 2 \times 1 0 ^ { 8 } ~ \mathrm { { c m } ^ { - 1 } }$ . A magnetic field $B = 1 0 ^ { 3 } \mathrm { \ g a u s s = 1 0 ^ { - 1 } }$ tesla is normal to the plane of the open orbit. (a) What is the order of magnitude of the period of the motion in k space? Take $v \approx 1 0 ^ { 8 }$ cm/sec. (b) Describe in real space the motion of an electron on this orbit in the presence of the magnetic field. 

6. Cohesive energy for a square well potential. (a) Find an expression for the binding energy of an electron in one dimension in a single square well of depth $U _ { 0 }$ and width a. (This is the standard first problem in elementary quantum mechanics.) Assume that the solution is symmetric about the midpoint of the well. (b) Find a numerical result for the binding energy in terms of $U _ { 0 }$ for the special case $\vert U _ { 0 } \vert = 2 \hbar ^ { 2 } / m a ^ { 2 }$ and compare with the appropriate limit of Fig. 20. In this limit of widely separated wells the band width goes to zero, so the energy for $k = 0$ is the same as the energy for any other k in the lowest energy band. Other bands are formed from the excited states of the well, in this limit. 

7. De Haas-van Alphen period of potassium. (a) Calculate the period $\Delta ( 1 / B )$ expected for potassium on the free electron model. (b) What is the area in real space of the extremal orbit, for $B = 1 0 \mathrm { k G } = 1 \mathrm { T ^ { 2 } }$ The same period applies to oscillations in the electrical resistivity, known as the Shubnikow-de Haas effect. 

* 8. Band edge structure on $k \cdot p$ perturbation theory. Consider a nondegenerate orbital $\psi _ { n \mathrm { k } }$ at $\mathbf k = 0$ in the band n of a cubic crystal. Use second-order perturbation theory to find the result 

$$
\boldsymbol {\epsilon} _ {n} (\mathbf {k}) = \boldsymbol {\epsilon} _ {n} (0) + \frac {\hbar^ {2} k ^ {2}}{2 m} + \frac {\hbar^ {2}}{m ^ {2}} \sum_ {j} ^ {\prime} \frac {| \langle n 0 | \mathbf {k} \cdot \mathbf {p} | j 0 \rangle | ^ {2}}{\boldsymbol {\epsilon} _ {n} (0) - \boldsymbol {\epsilon} _ {j} (0)}, \tag {39}
$$

where the sum is over all other orbitals $\psi _ { j \mathbf { k } }$ at $\mathbf { k } = 0$ . The effective mass at this point is 

$$
\frac {m}{m ^ {*}} \approx 1 + \frac {2}{m} \sum_ {j} ^ {\prime} \frac {| \langle n 0 | \mathbf {p} | j 0 \rangle | ^ {2}}{\epsilon_ {n} (0) - \epsilon_ {j} (0)}. \tag {40}
$$

* This problem is somewhat difficult. 

The mass at the conduction band edge in a narrow gap semiconductor is often dominated by the effect of the valence band edge, whence 

$$
\frac {m}{m ^ {*}} \approx \frac {2}{m E _ {g}} \sum_ {\nu} | \langle c |   \mathbf {p} | \nu \rangle | ^ {2}, \tag {41}
$$

where the sum is over the valence bands; $\mathrm { E _ { g } }$ is the energy gap. For given matrix elements, small gaps lead to small masses. 

9. Wannier functions. The Wannier functions of a band are defined in terms of the Bloch functions of the same band by 

$$
w (\mathbf {r} - \mathbf {r} _ {n}) = N ^ {- 1 / 2} \sum_ {\mathbf {k}} \exp (- i \mathbf {k} \cdot \mathbf {r} _ {n}) \psi_ {\mathbf {k}} (\mathbf {r}), \tag {42}
$$

where $\mathbf { r } _ { n }$ is a lattice point. (a) Prove that Wannier functions about different lattice points n,m are orthogonal: 

$$
\int d V w ^ {*} (\mathbf {r} - \mathbf {r} _ {n}) w (\mathbf {r} - \mathbf {r} _ {m}) = 0, \quad n \neq m. \tag {43}
$$

This orthogonality property makes the functions often of greater use than atomic orbitals centered on different lattice sites, because the latter are not generally orthogonal. (b) The Wannier functions are peaked around the lattice sites. Show that for $\psi _ { k } = N ^ { - 1 / 2 } e ^ { i k x } u _ { 0 } ( x )$ the Wannier function is 

$$
w (x - x _ {n}) = u _ {0} (x) \frac {\sin \pi (x - x _ {n}) / a}{\pi (x - x _ {n}) / a},
$$

for N atoms on a line of lattice constant a. 

10. Open orbits and magnetoresistance. We considered the transverse magnetoresistance of free electrons in Problem 6.9 and of electrons and holes in Problem 8.5. In some crystals the magnetoresistance saturates except in special crystal orientations. An open orbit carries current only in a single direction in the plane normal to the magnetic field; such carriers are not deflected by the field. In the arrangement of Fig. 6.14, let the open orbits be parallel to $k _ { x } ;$ in real space these orbits carry current parallel to the y axis. Let $\sigma _ { y y } = s \sigma _ { 0 }$ be the conductivity of the open orbits; this defines the constant s. The magnetoconductivity tensor in the high field limit $\omega _ { c } \tau \gg 1$ is 

$$
\sigma_ {0} \left( \begin{array}{c c c} Q ^ {- 2} & - Q ^ {- 1} & 0 \\ Q ^ {- 1} & s & 0 \\ 0 & 0 & 1 \end{array} \right)  ,
$$

with $Q = \omega _ { c } \tau . \ ( \mathrm { a } )$ Show that the Hall field is $E _ { y } = - E _ { x } / s Q$ . (b) Show that the effective resistivity in the x direction is $\rho = ( Q ^ { 2 } / \sigma _ { 0 } ) ( s / s + 1 )$ , so that the resistivity does not saturate, but increases as $B ^ { 2 }$ . 

11. Landau levels. The vector potential of a uniform magnetic field is Bzˆ $\mathbf { A } =$ By in the Landau gauge. The hamiltonian of a free electron without spin isxˆ 

$$
H = - (\hbar^ {2} / 2 m) (\partial^ {2} / \partial y ^ {2} + \partial^ {2} / \partial z ^ {2}) + (1 / 2 m) [ - i \hbar \partial / \partial x - e y B / c ] ^ {2}.
$$

We will look for an eigenfunction of the wave equation $H \psi = \epsilon \psi$ in the form 

$$
\psi = \chi (y) \exp [ i (k _ {x} x + k _ {z} z) ].
$$

(a) Show that $\chi ( y )$ satisfies the equation 

$$
(\hbar^ {2} / 2 m) d ^ {2} \chi / d y ^ {2} + [ \epsilon - (\hbar^ {2} k _ {z} ^ {2} / 2 m) - \frac {1}{2} m \omega_ {c} ^ {2} (y - y _ {0}) ^ {2} ] \chi = 0,
$$

where $\omega _ { c } = e B / m c$ and $y _ { 0 } = c \hbar k _ { x } / e B$ (b) Show that this is the wave equation of a . harmonic oscillator with frequency $\omega _ { c } ,$ where 

$$
\epsilon_ {n} = (n + \frac {1}{2}) \hbar \omega_ {c} + \hbar^ {2} k _ {z} ^ {2} / 2 m.
$$