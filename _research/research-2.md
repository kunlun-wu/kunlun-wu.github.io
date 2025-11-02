---
title: "Refractive Index Enhancement of Polymer Thin Film using CeO₂ Nanoparticles"
excerpt: |
  <p style="margin-bottom:0; font-size:15px; color:#808080;">Aug 2023 - May 2024, Carried over to new project with modification using ions</p>
  <p style="margin-top:0; font-size:15px; color:#505050;">Senior Design Project, Columbia University, NY</p>
  
  <img src='/images/research/2thinfilmnano/1.jpg' width="30%" align="right" style="margin-left:20px">
  Working with Cheng-Chia Tsai, this project explores the incorporation of nanocrystalline ceria (CeO₂) particles into polymer matrices to enhance the refractive index for photonic and optical-coating applications.
  Using ellipsometry and optical modeling, it investigates how nanoparticle loading influences optical constants in flexible, transparent nanocomposite thin films, revealing a nontrivial increase in refractive index while posing challenges for maintaining film uniformity.

collection: research
---
The senior design project was conducted in collaboration with Cheng-Chia Tsai under the supervision of Professor [Simon Billinge](https://www.engineering.columbia.edu/faculty-staff/directory/simon-jl-billinge) (Senior Design Project Supervisor), Professor [Siu-Wai Chan](https://www.apam.columbia.edu/faculty/siu-wai-chan) (Nanoparticle Production Advisor), and Professor [Nanfang Yu](https://www.apam.columbia.edu/faculty/nanfang-yu) (Optics Advisor). It explores the use of cerium oxide (CeO₂) nanoparticles as dopants to enhance the refractive index of SU-8 polymer thin films for potential applications in photonics and optical coatings.

The motivation for this project stems from the need for materials with high refractive indices in various optical applications, such as lenses, waveguides, and anti-reflective coatings. Nanoparticle doping presents a promising alternative due to its potential for tunable optical properties and ease of integration into polymer matrices.

Sample Preparation
-------------------------------
The nanoparticle samples were synthesized via coprecipitation at room temperature (around **25.5 °C**). 
### Reactants for Nanoceria Synthesis
- Cerium(III) nitrate hexahydrate, Ce(NO3)3 ∙ 6H2O: `6.5133g`
- HMT, hexamethylenetetramine, (CH2)6N4: `28.0372g`
- Deionized water (18 MΩ)

### Co-percipitation
1. Dissolve the cerium nitrate and HMT in separate beakers, each containing **400mL** deionized water.
2. Stir both beakers for **30** **minutes** 
3. Combine the contents of each beaker in and stir for **any number of minutes** (in this project we tried **6-hour** samples and **72-hour** samples)
4. Dry the beaker, cover with aluminum foil, and refrigerate to stop the growth of particles

### Centrifugation and Drying
- The procedure is the same as described in [Low Temperature Conductivity and Structural Analysis of Cu-CeO₂ Nanoparticles](https://kunlun-wu.github.io/research/research-1/), we also tried copper-doped nanoceria samples left this project (**2%** and **16%** Cu-CeO₂).

### Nanoparticle Size Characterization
- Dynamic Light Scattering (DLS) was first attempted, but the results were inconclusive due to the high polydispersity of the samples from nanoparticle clustering, and I forgot to take pictures :disappointed_relieved:.
- Scanning Electron Microscopy (SEM) imaging was then performed using a Zeiss Sigma VP SEM. The samples were prepared by drop-casting a dilute nanoparticle suspension onto silicon wafers and allowing them to dry under ambient conditions.
<img src='/images/research/2thinfilmnano/5.png'>
<img src='/images/research/2thinfilmnano/6.png'>

### Nanocomposite Thin Film Fabrication
1. Precursor Preparation 
   - The SU-8 polymer matrix was prepared by diluting SU-8 with the thinner to achieve a viscosity suitable for spin coating. The synthesized CeO₂ nanoparticles were dispersed in the SU-8 solution at varying weight percentages (**0%**, **0.1%**, **0.5%**, and **1%**) using ultrasonication to ensure uniform distribution. 
   - A DIY cooling container with ice packs was used to maintain a low temperature during sonication, minimizing solvent evaporation, preventing early cross-linking of polymer, and promoting uniform film formation.
<img src='/images/research/2thinfilmnano/2.png'>

2. Spin Coating
   - The nanocomposite solutions were spin-coated onto cleaned silicon substrates using a rotor controlled with an Arduino.
   - The exposure chamber was made with cardboard and a **50W** everbeam at **365nm** wavelength, with a power density measured at **26mW/cm²** using a UV power meter.
<img src='/images/research/2thinfilmnano/3.png'> 

   1. Spin coat at 100% speed (**6000rpm**) for **30 seconds** to achieve thin films of approximately **800nm** in thickness.
   2. Expose the coated substrates to UV light for **5 minutes** to initiate cross-linking.
   3. Post-exposure bake at **65 Celsius** for **2 minutes**.
   4. Post-exposure bake at **95 Celsius** for **3 minutes**. 

Ellipsometry
-------------------------------
The optical properties of the fabricated nanocomposite thin films were characterized using a J.A. Woollam alpha-SE ellipsometer. Measurements were taken at **70°** angle of incidence over a wavelength range of **400nm to 1000nm**.
<img src='/images/research/2thinfilmnano/4.png'>

Results and Discussion
-------------------------------
1. Pure CeO₂ Nanoparticle Samples (varying synthesis times, namely particle size)
<img src='/images/research/2thinfilmnano/7.png'>
2. Copper-doped CeO₂ Nanoparticle Samples (varying Cu %, same size)
<img src='/images/research/2thinfilmnano/8.png'>
3. Optical Constants of Nanocomposite Thin Films
<img src='/images/research/2thinfilmnano/9.png'>

Smaller nanoparticles exhibit more pronounced surface effects and quantum confinement, which can disrupt the uniformity of the electronic structure and widen the band gap, thereby reducing the refractive index. As particle size increases, these effects diminish, and the electronic structure approaches that of bulk ceria. This trend is consistent with the attenuation of quantum confinement and surface polarization effects, particularly in our samples where partial clustering of ceria nanoparticles was observed.  

From a free-carrier perspective, the Drude model describes how conduction electrons contribute to the optical response. An increase in free-carrier concentration raises the plasma frequency (ωₚ), shifting the frequency at which the real part of the dielectric permittivity changes sign from negative to positive. Below the plasma frequency, the material exhibits a positive real permittivity and thus a higher apparent refractive index. For Cu-doped CeO₂, ωₚ is estimated to be on the order of 3.6 × 10¹⁵Hz, corresponding to a wavelength near 84nm, suggesting that the visible range lies well below this threshold where the material behaves as a dielectric with enhanced refractive response.

To improve the experiment, it would be beneficial to:
- Test multiple spin rates for cross-verification of optical constants.
- Develop a home-code for optical modeling to have more control over fitting parameters and models.
- Further explore the distribution mechanism of the ceria nanoparticles in SU8 films. (e.g. products like pd-100 column)
- Use a polymer that has lower refractive indices to better show the change in refractive index. 
- Directly dissolve metal salts into the polymer matrix for better dispersion.