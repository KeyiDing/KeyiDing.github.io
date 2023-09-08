---
title: "PFS M31 Target Selection"
excerpt: "Machine Learning Techniques to Distinguish M-Giant Stars from M-Dwarf Stars for the PFS M31 Survey Target Selection<br/><img src='/images/mastar_apogee_logg.png'>"
collection: portfolio
---

The Andromeda Galaxy, also known as M31, is a spiral galaxy in the Local Group. It is the closest large spiral galaxy at a distance of 770 kpc and has a structure similar to the Milky Way: a bulge in the middle, surrounded by a stellar plus dark matter halo and a disk of stars, gas, and dust. Therefore, while our view of the Milky Way is limited by our position inside it, observing M31 from an “external” perspective provides a whole picture of a Milky Way-like galaxy.

The Subaru Telescope Prime Focus Spectrograph (PFS) Collaboration is planning to measure line-of-sight velocities and chemical abundances for a large-scale sample of M31 stars to study the structure and merger history of the galaxy. One issue for the study is to distinguish M31 member giant stars from foreground Milky Way dwarf stars before obtaining spectra as part of the survey. M31 giants and Milky Way dwarfs have the same colors but different intrinsic luminosities. The dwarfs are intrinsically faint and nearby while the giants are intrinsically bright and far away, and thus they have the same observed brightness and cannot be straightforwardly distinguished, especially for the coolest stars classified as M-stars.

A potential solution to this problem is narrow-band photometry. A key physical parameter that differentiates dwarf stars and giant stars is surface gravity, as dwarfs have higher surface gravity than giants. The PFS Collaboration intends to use the photometry of a narrow band filter, NB515, as an indicator of the stars' surface gravity. NB515 is a narrow-band filter on the Subaru Telescope sensitive to the MgH + Mgb absorption features around 515 nm, the strength of which is strongly dependent on surface gravity. Historically targets are selected based within a polygon on the color-color diagram of g-i vs NB515-g colors, but the polygon does not extend to the regime of the M-stars (Komiyama et al. 2018). Such selection method might be biased and thus cannot construct a complete chemical profile of M31.

<figure style="width:50%; text-align: center;">
<img src='/images/hsc.png'>
<figcaption>Image credit: Komiyama et al. 2018</figcaption>
</figure>

In my research project, I use machine learning methods to improve the robustness of the target selection method. To model NB515's sensitivity to stellar parameters and chemical abundances, I use synthetic photometry of high-resolution spectra from the MaNGA Stellar Library (MaStar) (Yan et al. 2019). As shown in the color-color diagram, the high surface gravity dwarfs and low surface gravity giants are well-separated within a restricted color range.

<figure style="width:50%; text-align: center;">
<img src='/images/mastar_apogee_logg.png'>
<figcaption>Image credit: Komiyama et al. 2018</figcaption>
</figure>


I built a training dataset with synthetic colors of MaStar and adjusted the stellar population in the training set to match the expected stellar population in both M31 and foreground M31 fields. I used theoretical models of the Milky Way, such as the Besancon model (Czekaj et al. 2014) and the TRILEGAL model (Girardi et al. 2005), to simulate photometric surveys of the M31 fields and estimate the color, magnitude, chemical abundance, and kinematics of the foreground stars. The stellar population of M31 is modelled based on past photometric and spectroscopic surveys of M31, including The Pan-Andromeda Archaeological Survey (PandAS - McConnachie el al. 2018) and the Dark Energy Spectroscopic Survey (DESI - Dey et al. 2022). 

I trained a neural network model with the input synthetic colors to predict the probability of a star being a giant. The model is tested with the Ursa Minor dwarf galaxy. According to the color-magnitude diagram, the model is able to select most of the red giant branch stars as member stars of Ursa Minor.