---
title: "Refractive Index Enhancement of Polymer Thin Film using Ce, Cu, and Ti Ions"
excerpt: |
  <p style="margin-bottom:0; font-size:15px; color:#808080;">May 2024 - Present, Paper in progress</p>
  <p style="margin-top:0; font-size:15px; color:#505050;">Under guidance of Professor <a href="https://www.apam.columbia.edu/faculty/nanfang-yu">Nanfang Yu</a>, Columbia University, NY</p>
  
  <img src='/images/research/4thinfilmion/1.jpg' width="30%" align="right" style="margin-left:20px">
  Working with Cheng-Chia Tsai, this project investigates metal-ion doping as a solution-based approach to tune the optical response of SU-8 polymer films.
  Through controlled curing and thermal treatment, it produces uniform, flexible thin films with increased refractive index and subtle color shifts.
  Ellipsometric analysis and Cauchy/Lorentzian optical modeling are used to extract optical constants, and a preliminary machine-learning framework is being developed to correlate refractive-index trends as additional data become available.

  
collection: research
---
This project was conducted in collaboration with Cheng-Chia Tsai under the supervision of Professor [Nanfang Yu](https://www.apam.columbia.edu/faculty/nanfang-yu). It builds upon my previous project ([Refractive Index Enhancement of Polymer Thin Film using CeO₂ Nanoparticles](https://kunlun-wu.github.io/research/research-2/)), extending the approach from nanoparticle doping to metal-ion incorporation as an alternative pathway for optical tuning. The goal is to enhance the refractive index of SU-8 polymer films through solution-based doping for flexible, high-index thin-film applications in photonics and optical coatings.

The motivation for this project stems from the challenges encountered in achieving uniform nanoparticle dispersion within the polymer matrix, which can lead to film inhomogeneity and optical scattering. Metal-ion doping offers a potentially simpler and more controllable approach to modifying the optical properties of the polymer without the complications associated with nanoparticle aggregation.

Sample Preparation
-------------------------------
The metal-ion doped SU-8 thin films were fabricated using a solution-based approach. Instead of incorporating nanoparticles, metal salts were directly dissolved into the SU-8 precursor solution to achieve doping with cerium (Ce), copper (Cu), and titanium (Ti) ions.
   - The precursors were spin-coated onto cleaned silicon substrates using a rotor controlled with an Arduino.
   - The exposure chamber was made with cardboard and a **50W** everbeam at **365nm** wavelength, with a power density measured at **26mW/cm²** using a UV power meter.
<img src='/images/research/2thinfilmnano/3.png'> 

### For cerium nitrate (Ce(NO₃)₃·6H₂O) and copper nitrate (Cu(NO₃)₂·3H₂O)
1. Metal salts are dissolved directly in the thinner. We produced **10wt%**, **25wt%**, and **50wt%** samples.
2. Stir until fully dissolved. (stir lightly to prevent bubbles)
3. Depending on how much thinner was present in the solution, the same weight of SU8 photoresist is added. So the precursors resulted are **5wt%**, **17.5wt%**, and **25wt%**.
4. Stir until properly mixed. (stir lightly to prevent bubbles)
5. Spin-coat the samples at 100% and 50% speed (**6000rpm at 100%**) for **30 seconds** to achieve thin films of approximately **1000-2500nm** in thickness.
6. Soft-bake at **65 Celsius** for **5 minutes** (added soft-bake due to water and NO₃ contents). 
7. Exposure for **10 minutes** (increased exposure time due to NO₃ neutralizing acid generated from SU8, hindering cross-linking). 
8. Post-exposure-bake at **65 Celsius** for **5 minutes**, **95 Celsius** for **5 minutes**, and **120 Celsius** for **5 minutes**.

### For Ti ions
Due to the unstability of titanium nitrate (Ti(NO₃)₄), I am looking into using titanium isopropoxide (TTIP, Ti[OCH(CH₃)₂]₄) or titanium acetylacetonate (Ti(acac)₄) for Ti ion doping. The spin-coating process will be adjusted if necessary.

Ellipsometry
---------------------------
The optical properties of the fabricated thin films were characterized using a J.A. Woollam VB-400 VASE ellipsometer. Measurements were taken at **70°** angle of incidence over a wavelength range of **400nm to 800nm**.
<img src='/images/research/4thinfilmion/2.png'>

Scanning Electron Microscopy (SEM)
-----------------------------
For providing a reference point in optical modeling, thicknesses of the films were measured using a Zeiss Sigma VP SEM. The samples were cut and the side-profiles were observed.
<img src='/images/research/4thinfilmion/3.jpg'>
<img src='/images/research/2thinfilmnano/6.png'>

Optical Modeling
---------------------
Custom code was developed for optical modeling to provide greater transparency and control than the proprietary WVASE software. (**The code will be made publicly available on GitHub following publication.**) Initial analysis employed a Cauchy model, which adequately described low-absorption samples. However, as nanoparticle or ion concentration increased, absorption in the visible range became non-negligible. To more accurately extract optical constants, a Lorentz oscillator model was implemented, though it could not fully capture the extended absorption tails observed near the UV and IR edges. Ongoing work incorporates a Tauc–Lorentz model to improve fitting accuracy across the full spectral range and to better represent the electronic transitions within the doped polymer system.

Machine Learning Framework
----------------------------
A complementary machine learning framework is under development to explore correlations between composition, processing parameters, and the resulting optical constants. Given the high dimensionality of the feature space (including oscillator parameters, annealing conditions, and dopant properties) and the limited number of experimental samples, the framework emphasizes interpretable, data-efficient models such as support vector regression (SVR) and random forest regression (RFR), with potential extension to neural network architectures as data volume increases. Current work focuses on feature engineering from ellipsometric fits and synthesis metadata to establish a robust basis for predictive modeling. While preliminary, this framework is designed to evolve as more measurements become available, ultimately linking experimental design with optical response prediction.

