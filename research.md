---
layout: page
title: Research
permalink: /research/
---

My current research focuses on how energy from active galactic nuclei (AGN)  
and large-scale shock structures in the cosmic web shape the evolution of  
galaxies and their surrounding gas. On this page you can find a short overview
of my work on [AGN feedback](#agn-feedback) and
[shocks in the cosmic web](#shocks-in-the-cosmic-web).

## Probing the radio-mechanical AGN feedback using multi-cavity systems {#agn-feedback}
#### AGN feedback in hot atmospheres

In an active galactic nucleus (AGN), found in a giant elliptical galaxy (gE), the cen- tral supermassive black hole (SMBH) prevents the surrounding hot gas from cooling. If some gas cools, it can get accreted onto the SMBH’s in the form of radiatively inefficient disc, launching relativistic jets. These jets inject energy into the gas, creating X-ray cavities that heat the atmosphere as they rise. This cycle repeats, forming a self-regulating feedback loop that suppresses radiative cooling and thus also star formation.

![feedback loop]({{ "assets/img/thesis/feedback_loop.png" | relative_url }})

Illustration of feedback loop in an AGN.
{:.figcaption}

#### X-ray cavities
X-ray cavities, formed by AGN jets displacing hot gas, appear as regions of **reduced** X-ray emission. From their volumes and the thermodynamic properties of the X-ray–emitting gas, we can derive the jet power that inflated them, which allows us to **quantify the AGN feedback history** if multiple generations are present.

The cavity age can be estimated as:
- **sound-speed time:** suitable for an attached cavity expanding mildly supersonically (innermost generation)
- **buoyancy time:** suitable for a cavity rising buoyantly (outer generations)


#### Data analysis
Archival *Chandra X-ray Observatory* data were analysed for four gEs: NGC 5813, NGC 5044, NGC 4649, and NGC 4472. The goal was to obtain an image of the galaxy to identify cavities and establish their parameters, and to obtain spectra to derive electron density and temperature radial profiles.

Spectral analysis was performed in XSPEC, where spectra were extracted from concentric annuli disecting the atmosphere, fitted with a model corresponding to X-ray emission and correctly deprojected. Cavities were identified in the residual images after subtraction of surface brightness model **$$\beta$$-model** or by deploying a machine-learning pipeline **CADET**. 

It is important to note that in our work, we reflected different physical
conditions in the **timescale corrections** and **energy corrections**
compared to the standard procedure.

<div class="galaxy-grid">
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc5044.png" | relative_url }}" alt="NGC 5044">
    <figcaption>NGC 5044</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc4472.png" | relative_url }}" alt="NGC 4472">
    <figcaption>NGC 4472</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc5813.png" | relative_url }}" alt="NGC 5813">
    <figcaption>NGC 5813</figcaption>
  </figure>
  <figure>
    <img src="{{ "/assets/img/thesis/galaxies/ngc4649.png" | relative_url }}" alt="NGC 4649">
    <figcaption>NGC 4649</figcaption>
  </figure>
</div>

![Resulting jet powers.]({{ "/assets/img/thesis/pjet_vs_distance_d.png" | relative_url }})

Resulting jet powers.
{:.figcaption}


#### Toy model

To probe how the **inclination** affects our measurements, we calculated how
the jet power changes with increasing inclination angle for
both **oblate** (e.g. NGC 5813 – G3) and
**prolate** cavities (e.g. NGC 4649 – G2). First,
we calculated the projected distance and cavity length, latter being a function of cavity's elongation. Followingly, we recalculated other cavity parameters at the given inclination angle.

![Relative jet power change as a function of cavity's elongation τ. Left panel shows a cavity expanding mildly supersonically, others show buoyant cavities.]({{ "/assets/img/thesis/relative_pjet_change.png" | relative_url }})

Relative jet power change as a function of cavity's elongation τ. Left panel shows a cavity expanding mildly supersonically, others show buoyant cavities.
{:.figcaption}

For systems showing an increasing jet power trend trend, we reversed the process
and calculated what would be the intrinsic jet power if we assumed that we
measured the projected jet power at a given inclination angle. 

![Increasing jet power trend alleviated for NGC 5044 and NGC 4472 when we take inclination into account.]({{ "/assets/img/thesis/inclined_jetpowers.png" | relative_url }})

Increasing jet power trend alleviated for NGC 5044 and NGC 4472 when we take inclination into account.
{:.figcaption}


### Key takeaways

- For aligned systems, the jet power seems to be roughly **constant**.  
- Inclination always causes the jet powers to be **overestimated**, and it can
  help explain the increasing trend in two of the studied
  systems.  
- Jet powers are affected by inclination more in **oblate** cavities. In
  general, **buoyant** cavities are affected more than cavities expanding
  supersonically.  


If you are interested in more detail, you can read the full thesis [here](https://is.muni.cz/th/xdxlp/BM_thesis_agn_feedback.pdf).




## Exploring Shock Structures in the Cosmic Web {#shocks-in-the-cosmic-web}

For my Master’s thesis, I am going to investigate accretion and merger shocks in 
the state-of-the-art cosmological simulation Illustris-TNG. The project aims to develop a robust pipeline deploying machine-learning algorithms to detect the shock structures. 