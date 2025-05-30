---
layout: default
title: Observability of Circumplanetary Disks
---




# Observability of Circum-Planetary Disk


Circum-planetary disks（CPDs）are accretion disks surrounding gas giants that play a crucial role in both planet and moon formation. 
In 2021, the first confirmed detection of a CPD around the protoplanet PDS 70c was made using the Atacama
Large Millimeter/submillimeter Array (ALMA) (Myriam Benisty et al. 2021). 

The ALMA is what: add an image 
Why important to study its observability 

This project aims to simulate radiation from a modeled CPD system and evaluate its observability with ALMA
under realistic observing conditions.


A Python-based modeling pipeline was developed to generate wavelength-dependent dust
continuum emission maps from a physically motivated CPD model embedded within a
protoplanetary disk (PPD), based on the PDS 70 system. The model is processed with the
165 radiative transfer code RADMC-3D, simulating the effects of both stellar and planetary
irradiation using 108 photon packets. Given parameters T∗ = 4000K, M∗ = 1.65M⊙,
Tp = 1200K, Mp = 3MJ , the resulting mass-weighted average temperature of the CPD region
is found to be approximately 45.75K. The normalized intensity maps are then generated across
the ALMA bands, taking into account dust composition, temperature, and density structure.

 
 Using CASA (Common Astronomy Software Applications), synthetic ALMA observations
are created from these maps, incorporating telescope configuration, source location, noise, and
observing. A 3-hour integration under ideal conditions is shown to produce 5σ detections
across multiple ALMA bands. Although intrinsic CPD emission is brightest at Band 10, the
structural pattern of the CPD is fragmented in the highest bands due to strong atmospheric
175 attenuation.Future directions include refining the model for specific target systems and extending
the simulation framework to assess observability with other facilities beyond ALMA

##  Methodology
- Data: XYZ survey (1M+ data points)
- Tools: Python, Matplotlib, SciPy
- Filtering: energies > 10^19 eV

## Results

![Cosmic Ray Plot]({{ site.baseurl }}/assets/images/cosmic-ray-plot.png)

Our simulation shows a 3σ excess in one sky region, potentially indicating magnetic lensing.

## Conclusion
This pattern could inform our understanding of cosmic ray origins and Galactic magnetic fields.


<div class="grid-plot">
  <img src="{{ site.baseurl }}/assets/images/plot1.png" alt="Plot 1">
  <img src="{{ site.baseurl }}/assets/images/plot2.png" alt="Plot 2">
  <img src="{{ site.baseurl }}/assets/images/plot3.png" alt="Plot 3">
  <img src="{{ site.baseurl }}/assets/images/plot4.png" alt="Plot 4">
  <img src="{{ site.baseurl }}/assets/images/plot5.png" alt="Plot 5">
  <img src="{{ site.baseurl }}/assets/images/plot6.png" alt="Plot 6">
  <img src="{{ site.baseurl }}/assets/images/plot7.png" alt="Plot 7">
  <img src="{{ site.baseurl }}/assets/images/plot8.png" alt="Plot 8">
  <img src="{{ site.baseurl }}/assets/images/plot9.png" alt="Plot 9">
</div>



---

<a href="{{ site.baseurl }}/experience/" class="back-link">← </a>
