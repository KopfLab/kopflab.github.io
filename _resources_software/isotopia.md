---
layout: resource
title: isotopia R package
weight: 3
picture: 
github: sebkopf/isotopia
---

In stable isotope geochemical calculations, we use a number of different representations of isotopic information and processes (ratios, abundances, delta values, alpha values, epsilon values, fractionation factors, refereence frame shifts, mass balance calculations, mass-independent effects, etc., etc.) that are constantly being converted back and forth and used for different kinds of isotope arithmetic. Very frequently, the tangle of keeping track of this information and how all the calculations are done properly makes code very hard to read, difficult to communicate - or even understand oneself later on, and as anyone knows who's ever dropped a -1 or x1000 at the wrong place, prone to small mistakes that can make a huge difference. Isotopia is an R package that uses the S4 object system of R to define elemental isotopic data classes so that it can automatically keep track of what is a ratio, what is a delta value (and is it in permil notation or in ppm), etc., and perform isotope arithmetic accordingly.
