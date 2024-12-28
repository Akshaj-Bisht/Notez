---
{"updated":"2024-12-28T15:11:11.567+05:30","dg-publish":true,"dg-home":false,"tags":["Semester-3","Physics"],"permalink":"/physics/paper-1/","dgPassFrontmatter":true,"created":"2024-12-28T12:47:12.971+05:30"}
---


### Question 1:

#### (a)  Explain the concept of temperature using the zeroth law of thermodynamics.
The zeroth law of thermodynamics states that if two systems (A and B) are each in thermal equilibrium with a third system (c) , then A and B are in thermal equilibrium with each other. This establishes the concept of temperature as a fundamental and measurable property. Temperature quantifies the thermal state of a system, and systems in thermal equilibrium have the same temperature.


---

#### (b)  Calculate the change in entropy when 1 mole of an ideal gas expands isothermally to three times its original volume.
For an isothermal process, entropy change () is given by:

$$
\Delta S = nR \ln \frac{V_f}{V_i}
$$
$$\Delta S = (1)(8.31) \ln(3) \approx 9.13 \, \text{J/K}
$$

---

#### (c)  Calculate the most probable velocity of a Maxwellian gas molecule of mass  at 300K.
The most probable velocity  is given by:
$$
v_p = \sqrt{\frac{2kT}{m}}
$$
$$
v_p = \sqrt{\frac{2(1.38 \times 10^{-23})(300)}{5.31 \times 10^{-26}}} \approx 422 \, \text{m/s}
$$

---

#### (d)  Determine the wavelength corresponding to the maximum emissivity of a black body at 3 K and 5000 K.
Using Wien's law, , where :

For :


- $$\lambda_{\text{max}} = \frac{2.898 \times 10^{-3}}{3}$$ $$\approx 9.66 \times 10^{-4} \, \text{m} \, (\text{infrared})$$

- $$\lambda_{\text{max}} = \frac{2.898 \times 10^{-3}}{5000} $$ $$\approx 5.8 \times 10^{-7} \, \text{m} \, (\text{visible light, green region})$$


---

### Question 2:

#### (a)  Using the first law of thermodynamics, prove:

1.  for one mole of an ideal gas:
From the first law, . For an ideal gas:



$C_V = \left( \frac{dU}{dT} \right), \quad C_P = \left( \frac{dQ}{dT} \right)_P = C_V + R$

2. :
Adiabatic elasticity  is given by , and isothermal elasticity  is :



$\frac{E_s}{E_T} = \gamma = \frac{C_P}{C_V}$


---

#### (b)  Compression of 1 mole of a gas adiabatically (initial , ):

1. Final temperature ():
For an adiabatic process:



$T_f = T_i \left( \frac{P_f}{P_i} \right)^{\frac{\gamma - 1}{\gamma}} = 300 \times 10^{\frac{0.4}{1.4}} \approx 586 \, \text{K}$

2. Work done ():



$W = \frac{P_iV_i \left[ 1 - \left( \frac{P_f}{P_i} \right)^{\frac{\gamma - 1}{\gamma}} \right]}{\gamma - 1}$


---

### Question 3:

#### (a)  What are Kelvin-Planck and Clausius statements of the second law of thermodynamics? Show that both are equivalent. Derive the second law mathematically in terms of entropy.

Kelvin-Planck Statement: It is impossible to construct a heat engine that operates in a cycle and converts all the heat absorbed from a reservoir into work.

Clausius Statement: It is impossible to construct a device that operates in a cycle and transfers heat from a colder body to a hotter body without any work input.


Equivalence:

If Kelvin-Planck's statement is violated, work could be extracted to drive a device violating Clausius' statement, and vice versa.


Entropy Derivation:
For a reversible process:

$dS = \frac{dQ}{T}$

$\Delta S_{\text{total}} = \Delta S_{\text{system}} + \Delta S_{\text{surroundings}} \geq 0$


---

#### (b)  Efficiency of a Carnot engine with  (source) and  (sink):

Initial efficiency:

$\eta = 1 - \frac{T_2}{T_1} = \frac{1}{5} \implies \frac{T_2}{T_1} = \frac{4}{5}$

$\eta' = 1 - \frac{T_2 - 50}{T_1} = \frac{1}{3} \implies \frac{T_2 - 50}{T_1} = \frac{2}{3}$

$T_1 = 750 \, \text{K}, \quad T_2 = 600 \, \text{K}$


---

### Question 4:

#### (a)  Define the four thermodynamic potentials. Deduce Maxwell's thermodynamic relations.

1. Thermodynamic Potentials:

Internal Energy (U): Function of .

Enthalpy (H): .

Helmholtz Free Energy (F): .

Gibbs Free Energy (G): .



2. Maxwell Relations:
From  and :



$\frac{\partial T}{\partial V} = -\frac{\partial P}{\partial S}, \quad \frac{\partial T}{\partial P} = \frac{\partial V}{\partial S}$


---

#### (b)  Proof of the given thermodynamic relationship:
Proof will depend on the specific thermodynamic identity provided. It will use the first and second laws of thermodynamics along with state variables and potentials.


---

### Question 5:

#### (a)  Define mean free path . Derive its expression.

The mean free path () is the average distance a gas molecule travels before colliding with another molecule.

Expression for :

$\lambda = \frac{1}{\sqrt{2} \pi d^2 n}$


---

#### (b)  Coefficient of viscosity () and its variation with temperature:

The coefficient of viscosity is given by:

$\eta = \frac{1}{3} \rho \lambda v$

Viscosity increases with temperature as  increases due to higher molecular speeds.


---

### Question 6:

#### (a)  Describe the spectral distribution of black body radiation. How does Planck's law lead to Rayleigh's law?

The spectral distribution shows that intensity first rises with wavelength, peaks, and then decreases.

Planck’s Law:


$I(\lambda, T) = \frac{2hc^2}{\lambda^5} \frac{1}{e^{\frac{hc}{\lambda kT}} - 1}$

$I(\lambda, T) = \frac{2ckT}{\lambda^4}$


---

#### (b)  Temperature and power radiated from stellar surface ():

From Wien’s Law:

$T = \frac{b}{\lambda_{\text{max}}} = \frac{2.898 \times 10^{-3}}{5100 \times 10^{-10}} \approx 5700 \, \text{K}$

$P = \sigma T^4 = (5.67 \times 10^{-8})(5700^4)$
$\approx 6.43 \times 10^7 \, \text{W/m}^2$


---

### Question 7:

#### (a)  Salient features of Maxwell-Boltzmann statistics. Differences from Bose-Einstein and Fermi-Dirac statistics:

Maxwell-Boltzmann (MB): Classical, indistinguishable particles, no quantum restrictions.

Bose-Einstein (BE): Particles are bosons, follow symmetry, can occupy the same state.

Fermi-Dirac (FD): Particles are fermions, Pauli exclusion applies, each state can hold one particle.


Differences arise from quantum effects and distinguishability.


---

#### (b)  Number of ways to arrange 4 bosons in 7 states:

For bosons:

$\text{Number of ways} = \binom{n + r - 1}{r} = \binom{7 + 4 - 1}{4} = \binom{10}{4} = 210$


---

 



