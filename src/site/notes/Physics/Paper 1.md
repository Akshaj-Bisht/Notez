---
{"dg-publish":true,"permalink":"/physics/paper-1/","tags":["semester-3","physics"],"created":"2024-12-29T11:39:21.952+05:30","updated":"2024-12-29T12:32:49.480+05:30"}
---




# Thermodynamics Questions and Answers

---

##### 1. (a) Explain the concept of temperature using the zeroth law of thermodynamics. (3 marks)


The zeroth law of thermodynamics states that if two systems are in thermal equilibrium with a third system, they are also in thermal equilibrium with each other. Temperature is the property that determines thermal equilibrium; it provides a measure of the average kinetic energy of particles in a substance.
*Figure 1: Representation of thermal equilibrium based on the zeroth law.*


---

##### 1. (b) Calculate the change in entropy when 1 mole of an ideal gas expands isothermally to three times its original volume. (3 marks)

The change in entropy for isothermal expansion of an ideal gas is given by:  
\[
$\Delta S = nR \ln \frac{V_2}{V_1}$
\]
For $n = 1$, $V_2 = 3V_1$:  
\[
$\Delta S = (1)(8.31) \ln(3) \approx 9.13 \, \mathrm{J/K}$
\] 

*Figure 2: Visualization of entropy change during expansion.*


##### 1. (c) Calculate the most probable velocity of a Maxwellian gas molecule of mass  at 300 K. (3 marks)

The most probable velocity is given by:  
\[
$v_p = \sqrt{\frac{2kT}{m}}$
\]
Substitute $k = 1.38 \times 10^{-23}$, $T = 300$, $m = 5.31 \times 10^{-26}$:  
\[
$v_p = \sqrt{\frac{2(1.38 \times 10^{-23})(300)}{5.31 \times 10^{-26}}} \approx 517 \, \mathrm{m/s}$
\]

*Figure 3: Maxwell-Boltzmann distribution showing the most probable speed.*


---

##### 1. (d) Determine the wavelength corresponding to the maximum emissivity of a black body at a temperature  equal to  and . In what spectral region will the wavelengths be found? (3 marks)

Using Wien’s law:  
\[
$\lambda_{\max} = \frac{b}{T}, \quad b = 2.898 \times 10^{-3} \, \mathrm{m \cdot K}$
\]
For $T = 3 \, \mathrm{K}$:  
\[
$\lambda_{\max} = \frac{2.898 \times 10^{-3}}{3} = 0.966 \, \mathrm{mm} \, (\text{microwave region})$
\]
For $T = 5000 \, \mathrm{K}$:  
\[
$\lambda_{\max} = \frac{2.898 \times 10^{-3}}{5000} = 580 \, \mathrm{nm} \, (\text{visible region})$
\]

*Figure 4: Blackbody radiation spectrum and Wien’s law application.*


---

##### 2. (a) Using the first law of thermodynamics, prove that:

(i) For one mole of an ideal gas,  (4 marks)

The first law is:  
\[
$\Delta Q = \Delta U + P\Delta V$
\]
For constant volume:  
\[
$\Delta Q_V = C_V \Delta T = \Delta U$
\]
For constant pressure:  
\[
$\Delta Q_P = C_P \Delta T = \Delta U + R \Delta T$
\]
Thus:  
\[
$C_P - C_V = R$
\]

(ii) If  and  are adiabatic and isothermal elasticity respectively, then  (4 marks)

Using the definitions:  
\[
$E_T = P, \quad E_s = \gamma P$
\]
Thus:  
\[
$\frac{E_s}{E_T} = \gamma =$

$\frac{C_P}{C_V}$
\]

*Figure 5: Thermodynamic properties derived from the first law.*


---

##### 2. (b) 1 mole of a perfect gas initially at  is compressed adiabatically such that its pressure becomes 10 times its initial value. Calculate:

(i) Its temperature after compression (4 marks)

For adiabatic compression:  
\[
$$T_2 = T_1 \left(\frac{P_2}
{P_1}\right)^{\frac{\gamma - 1}{\gamma}}$$
\]
$Substitute T_1 = 300 \, \mathrm{K}, \gamma = 1.4$:  
\[
$T_2 = 300 (10)^{\frac{0.4}{1.4}} \approx 717 \, \mathrm{K}$
\]

(ii) Work done during the process (4 marks)

Work done:  
\[
$W = \frac{P_1 V_1 \left[(P_2/P_1)^{(\gamma - 1)/\gamma} - 1\right]}{\gamma - 1}$]

For 1 mole, solve using values for $P_1$, $V_1$, and $T_1$. Result will depend on specific values provided.

*Figure 6: Adiabatic compression illustration.*


---

##### 3. (a) What are Kelvin-Planck statement and Clausius statement of the second law of thermodynamics? Show that both statements are equivalent. Hence derive the mathematical expression of the second law in terms of entropy. (8 marks)

The Kelvin-Planck statement states that no process is possible where the sole result is the conversion of heat from a single reservoir into work.  
The Clausius statement says that no process is possible where the sole result is the transfer of heat from a colder to a hotter body.  

Both statements imply the impossibility of perpetual motion machines and the necessity of entropy increases. Deriving entropy:  
\[
$$dS = \frac{\delta Q_{\text{rev}}}{T}$$
\]

*Figure 7: Illustration of entropy changes.*


---

##### 3. (b) The efficiency of Carnot's engine is . By decreasing the temperature of the sink by  while keeping the source at the same temperature, it increases to . Find the temperatures of the source and the sink. (4 marks)

The Carnot efficiency is:  
\[
$$\eta = 1 - \frac{T_{\text{sink}}}{T_{\text{source}}}$$
\]
For $$\eta_1 = 1/5:$$  
\[
$$T_{\text{sink}} = 0.8 T_{\text{source}}$$
\]
For $$\eta_2 = 1/3:$$
\[
$$T_{\text{sink}} - 50 = 0.67 T_{\text{source}}$$
\]
Solve these equations to find $T_{\text{source}} = 300 \, \mathrm{K}$, $T_{\text{sink}} = 240 \, \mathrm{K}$.

*Figure 8: Representation of the Carnot cycle.*

---

##### 4. (a) Define the four thermodynamic potentials. Deduce Maxwell's thermodynamic relations using fundamental equations of thermodynamic potentials. (9 marks)

The four thermodynamic potentials are:  

1. **Internal Energy ($U$)**: $U = Q - W$ (first law).  
2. **Enthalpy ($H$)**: $H = U + PV$.  
3. **Helmholtz Free Energy ($F$)**: $F = U - TS$.  
4. **Gibbs Free Energy ($G$)**: $G = H - TS$.  

Maxwell’s relations are derived using the potentials’ differentials:  

- $U(S, V)$: $\frac{\partial T}{\partial V}\bigg|_S = -\frac{\partial P}{\partial S}\bigg|_V$.  
- $H(S, P)$: $\frac{\partial T}{\partial P}\bigg|_S = \frac{\partial V}{\partial S}\bigg|_P$.  
- $F(T, V)$: $\frac{\partial S}{\partial V}\bigg|_T = \frac{\partial P}{\partial T}\bigg|_V$.  
- $G(T, P)$: $\frac{\partial S}{\partial P}\bigg|_T = -\frac{\partial V}{\partial T}\bigg|_P$.  


*Figure 9: Thermodynamic potentials and their relationships.*


---

##### 4. (b) Prove that . (3 marks)

Start with the definition of enthalpy:
\[
H = U + PV
\]
Take the derivative with respect to $P$ at constant $T$:  
\[
$$\left(\frac{\partial H}{\partial P}\right)_T = \left(\frac{\partial (U + PV)}{\partial P}\right)_T$$
\]
Using thermodynamic identities:
\[
$$\frac{\partial U}{\partial P}\bigg|_T = -T\frac{\partial V}{\partial T}\bigg|_P$$
\]
Thus:
\[
$$\left(\frac{\partial H}{\partial P}\right)_T = V - T\left(\frac{\partial V}{\partial T}\right)_P$$
\]


---

##### 5. (a) Define mean free path () of the molecules of a gas. If  is the diameter of each molecule and  is the number of molecules per unit volume, derive an expression for  assuming that all molecules except one are at rest. (8 marks)

The mean free path ($\lambda$) is the average distance a molecule travels before colliding with another.  

For a stationary molecule:  
\[
$$\lambda = \frac{1}{\sqrt{2} \pi d^2 n}$$
\]
Where $d$ is the molecular diameter and $n$ is the number density. The factor $\sqrt{2}$ accounts for relative motion between molecules.  
  
*Figure 10: Visualization of molecular collisions.*


---

##### 5. (b) Write the expression for the coefficient of viscosity () of an ideal gas in terms of mean free path. How does it vary with absolute temperature of the gas? (4 marks)

The coefficient of viscosity is given by:  
\[
$$\eta = \frac{1}{3} m n \lambda v_{\text{avg}}$$
\]
Where $v_{\text{avg}}$ is the average molecular velocity. Since $\lambda \propto T^{1/2}$, $\eta \propto T^{1/2}$.  


*Figure 11: Viscosity increases with temperature.*


---

##### 6. (a) Describe the spectral distribution of blackbody radiation. How does Planck's radiation law lead to Rayleigh’s radiation law? (9 marks)

The spectral distribution of blackbody radiation describes how energy is emitted at different wavelengths.  
- Planck’s law:  
\[
$$E(\lambda, T) = \frac{2hc^2}{\lambda^5} \frac{1}{e^{hc / \lambda kT} - 1}$$
\]
At long wavelengths ($hc / \lambda kT \ll 1$), Planck’s law reduces to:  
\[
$$E(\lambda, T) \approx \frac{2kT}{\lambda^4} \quad (\text{Rayleigh-Jeans Law})$$
\]

Planck’s law resolves the ultraviolet catastrophe predicted by Rayleigh-Jeans law.  
  
*Figure 12: Blackbody radiation spectrum showing Planck’s law.*


---

##### 6. (b) Determine the temperature and power radiated from 1 cm$^2$ of stellar surface of the Sun with , considering the surface a blackbody. (3 marks)

Using Wien’s law:  
\[
$$T = \frac{b}{\lambda_{\max}} = \frac{2.898 \times 10^{-3}}{5100 \times 10^{-10}} \approx 5686 \, \mathrm{K}$$
\]
Stefan-Boltzmann law for power:  
\[
$$P = \sigma T^4 = (5.67 \times 10^{-8})(5686)^4 \times 10^{-4}$$

$$\approx 6.4 \times 10^5 \, \mathrm{W/m^2}$$
\]

*Figure 13: Sun’s blackbody spectrum.*


---

##### 7. (a) What are the salient features of Maxwell-Boltzmann statistics? Describe qualitatively how these features differ from Bose-Einstein and Fermi-Dirac statistics. (8 marks)

Maxwell-Boltzmann statistics applies to classical particles:  
- Particles are distinguishable.  
- No quantum restrictions (multiple particles in one state allowed).  
- Valid at high temperatures and low densities.  

Differences:  
- **Bose-Einstein**: Identical, indistinguishable particles; bosons can occupy the same state (e.g., photons).  
- **Fermi-Dirac**: Identical fermions obey Pauli Exclusion Principle; no two fermions can occupy the same state.  

*Figure 14: Comparison of statistical distributions.*

---

##### 7. (b) Calculate and show the number of ways of arranging four bosons in seven different states. (4 marks)

The number of arrangements is given by the formula:  
\[
$$\text{Ways} = \frac{(n + r - 1)!}{r!(n - 1)!}$$
\]
Where $n = 7$ (states) and $r = 4$ (bosons):  
\[
$$\text{Ways} = \frac{(7 + 4 - 1)!}{4! \times (7 - 1)!} = \frac{10!}{4! \times 6!} = 210$$
\]

*Figure 15: Example visualization of boson arrangements.*


---

Values of Constants Used

- Boltzmann’s constant: $k = 1.38 \times 10^{-23} \, \mathrm{JK^{-1}}$.  
- Universal gas constant: $R = 8.31 \, \mathrm{Jmol^{-1}K^{-1}}$.  
- Wien’s constant: $b = 2.898 \times 10^{-3} \, \mathrm{m \cdot K}$.  
- Stefan-Boltzmann constant: $\sigma = 5.67 \times 10^{-8} \, \mathrm{Wm^{-2}K^{-4}}$.


---




