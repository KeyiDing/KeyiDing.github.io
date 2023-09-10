---
title: "Large Scale Photometric Stellar Parameters Inference"
excerpt: "Stellar photospheric and fundamental parameters inference by fitting multi-wavelength photometry, astrometry, and 3-D dustmap to theoretical isochrones<br/><img src='/images/M67_feh_uv.png'>"
collection: portfolio
---

Precision stellar parameters inferences have historically relied on high-resolution spectroscopy. Despite the great precision of spectroscopic parameters inference, stellar spectroscopy suffers from several limitations including expensive hardware and restricted observation depth.

Compared to spectroscopy, imaging data is much easier and more economical to obtain on a large scale. The selection criteria for photometric surveys are much less demanding compared to complex targeting for spectroscopy, leading to better spatial coverage and covering full parameter space.

We tested the precision and accuracy of a novel stellar parameters inference method by fitting multi-wavelength photometry, Gaia astrometry and 3-D dustmap to the MIST Isochrones and Evolution Tracks (Dotter 2016; Choi et al. 2016; Paxton et al. 2011, 2013, 2015). We demonstractes that the precision of the photometric [Fe/H] from our inference is comparable to [Fe/H] from spectroscopic surveys, and the mass/radius inference is accurate in comparison to asteroseismic-inferred mass/radius.

We verified the precision of our [Fe/H] inference with 7 open clusters. Stars in open clusters were formed from the same giant molecular cloud and therefore have approximatelty the same age and chemical compositions. Thus the dispersion of the inferred [Fe/H] within a single open cluster can be used as an indicator of the precision of the inference method. Our analysis shows that our inference method derives accurate [Fe/H] for the turnoff stars and main sequence stars down to the color limit of $G_{\text{BP}}-G_{\text{RP}}$ about 1.5 which corresponds to K5 stars with the typical precision of 0.13 dex. Our inferred [Fe/H] also generally agrees with spectroscopy-inferred [Fe/H] with the offset within the $3\sigma$ confidence interval, and the dispersion of inferred [Fe/H] is comparable to the dispersion of spectroscopy-inferred [Fe/H] within a open cluster.

<p align="center" width="100%">
    <img width="100%" src="/images/M67_feh_uv.png"> 
     <figcaption>
          Inferred metallicities of stars in M 67 as a function of $G_{\text{BP}}-G_{\text{RP}}$ color. The colors of the data points communicate the availability of the ultraviolet passbands: we plot the stars with only SDSS u band in dark blue squares, stars with only GALEX NUV in green squares, stars with both SDSS u and GALEX NUV bands in light blue squares, and stars without ultraviolet data in open circles. The mean [Fe/H] uncertainty is plotted as the black error bar on the top left corner. The plot suggests that the inferred metallicities are concentrated around the metallicity at 0.07 from literature (Donor et al. 2020). For M 67, our analysis derives accurate [Fe/H] for the turnoff stars and main sequence stars, down to the $G_{\text{BP}}-G_{\text{RP}}$ about 1.5 which corresponds to K5 stars, with the precision of 0.13 dex.
      </figcaption>
</p>

To verify the accuracy of inferred mass and radius, we compare our inferred masses and radii with the asteroseismic informed masses and radii from the Kepler Asteroseismic LEGACY Sample (Silva Aguirre et al. 2017). The mean percentage offset the masses is 4.0 \% and the mean percentage offset of the radii is 4.3 \%. Both the inferred radius and mass are consistent with the asteroseismic inferred radius and mass, with most offsets within the $3 \sigma$ confidence interval.

<p align="center" width="100%">
    <img width="100%" src="/images/Kepler_comparison.png"> 
     <figcaption>
          Comparison of our inferred radius and mass with Kepler Asteroseismic LEGACY sample parameters. We plot the mean asteroseismic inferred radii/masses and errors from the 6 pipelines on the x-axis, and the Isochrones inferred radii/masses and the internal uncertainties on the y-axis. The mean percentage offset the masses is 4.0 \% and the mean percentage offset of the radii is 4.3 \%. Both the inferred radius and mass are consistent with the asteroseismic inferred radius and mass, with most offsets within the $3 \sigma$ confidence interval.
      </figcaption>
</p>

The inference method will have wide applicability for Galactic and stellar archaeology in the era of the Vera C.\ Rubin Observatory's Legacy Survey of Space and Time (LSST).