---
title: "PFS M31 Target Selection"
excerpt: "Machine Learning Techniques to Distinguish M-Giant Stars from M-Dwarf Stars for the PFS M31 Survey Target Selection<br/><img src='/images/mastar_apogee_logg.png'>"
collection: portfolio
---

The Andromeda Galaxy, also known as M31, is a spiral galaxy in the Local Group. It is the closest large spiral galaxy at a distance of 770 kpc and has a structure similar to the Milky Way: a bulge in the middle, surrounded by a stellar plus dark matter halo and a disk of stars, gas, and dust. Therefore, while our view of the Milky Way is limited by our position inside it, observing M31 from an “external” perspective provides a whole picture of a Milky Way-like galaxy.

The Subaru Telescope Prime Focus Spectrograph (PFS) Collaboration is planning to measure line-of-sight velocities and chemical abundances for a large-scale sample of M31 stars to study the structure and merger history of the galaxy. One issue for the study is to distinguish M31 member giant stars from foreground Milky Way dwarf stars before obtaining spectra as part of the survey. M31 giants and Milky Way dwarfs have the same colors but different intrinsic luminosities. The dwarfs are intrinsically faint and nearby while the giants are intrinsically bright and far away, and thus they have the same observed brightness and cannot be straightforwardly distinguished, especially for the coolest stars classified as M-stars.

A potential solution to this problem is narrow-band photometry. A key physical parameter that differentiates dwarf stars and giant stars is surface gravity, as dwarfs have higher surface gravity than giants. The PFS Collaboration intends to use the photometry of a narrow band filter, NB515, as an indicator of the stars' surface gravity. NB515 is a narrow-band filter on the Subaru Telescope sensitive to the MgH + Mgb absorption features around 515 nm, the strength of which is strongly dependent on surface gravity. 

I developed machine learning techniques to distinguish likely member stars of M31 - which are predominantly red giant stars - from foreground Milky Way contamination prior to fiber assignment and observation. Most fields to be targeted have been pre-imaged with Hyper Suprime Cam in both broad-band g and i filters and the gravity-sensitive narrow-band NB515 filter and our machine learning algorithm aims to find the separation between foreground dwarfs and target giants on the 2-color diagram.

<!-- <figure style="width:100%; text-align: center;">
<img src='/images/mastar_apogee_logg.png'>
</figure> -->

<p align="center" width="100%">
    <img width="100%" src="/images/mastar_apogee_logg.png"> 
</p>

I modeled the NB515 filter's sensitivity to stellar atmospheric parameters and chemical abundances through the creation of synthetic photometry of a wide range of spectral types from the large empirical MaNGA Stellar Library (MaStar), and constructed training sets with this synthetic photometry. To reduce the covariate shift in machine learning, I used theoretical models and existing observations to simulate observational data for fields centered on M31, to ensure our training data represent the expected stellar populations of both foreground and M31 member stars. The stellar population of M31 is modelled based on past photometric and spectroscopic surveys of M31, including The Pan-Andromeda Archaeological Survey (PandAS - McConnachie el al. 2018) and the Dark Energy Spectroscopic Survey (DESI - Dey et al. 2022). 

I trained a neural network model with the input synthetic colors to predict the probability of a star being a giant. Tested with existing spectroscopic catalogs, the model reaches over 90 percent accuracy.