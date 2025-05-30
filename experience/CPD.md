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



<div class="carousel">
  <img id="carousel-img" src="{{ site.baseurl }}/assets/images/CPD_images/band 1.png" alt="Plot" />
  <div class="carousel-buttons">
   <button class="slider-arrow left" onclick="prevSlide()">&#9664;</button>
   <button class="slider-arrow right" onclick="nextSlide()">&#9654;</button>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const images = [
      "{{ site.baseurl }}/assets/images/CPD_images/band 1.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 3.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 4.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 5.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 6.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 7.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 8.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 9.png",
      "{{ site.baseurl }}/assets/images/CPD_images/band 10.png"
    ];

    let index = 0;
    const img = document.getElementById("carousel-img");

    function showImage(i) {
      img.src = images[i];
    }

    window.nextSlide = function () {
      index = (index + 1) % images.length;
      showImage(index);
    };

    window.prevSlide = function () {
      index = (index - 1 + images.length) % images.length;
      showImage(index);
    };
  });
</script>


## Results

![Cosmic Ray Plot]({{ site.baseurl }}/assets/images/cosmic-ray-plot.png)

Our simulation shows a 3σ excess in one sky region, potentially indicating magnetic lensing.



<div class="carousel">
  <img id="carousel-img" src="{{ site.baseurl }}/assets/images/CPD_images/C10_1_36000_pwv1.fits-image-2025-04-04-23-41-49.png" alt="Plot" />
  <div class="carousel-buttons">
   <button class="slider-arrow left" onclick="prevSlide()">&#9664;</button>
   <button class="slider-arrow right" onclick="nextSlide()">&#9654;</button>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const images = [
      "{{ site.baseurl }}/assets/images/CPD_images/C10_1_36000_pwv1.fits-image-2025-04-04-23-41-49.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_3_36000_pwv1.fits-image-2025-04-04-23-42-51.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_4_36000_pwv1.fits-image-2025-04-04-23-44-20.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_5_36000_pwv1.fits-image-2025-04-04-23-45-34.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_6_36000_pwv1.fits-image-2025-04-04-23-47-28.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_7_36000_pwv1.fits-image-2025-04-04-23-48-47.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_8_36000_pwv1.fits-image-2025-04-04-23-50-02.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_9_36000_pwv1.fits-image-2025-04-04-23-51-46.png",
      "{{ site.baseurl }}/assets/images/CPD_images/C10_10_36000_pwv1.fits-image-2025-04-04-23-52-38.png"
    ];

    let index = 0;
    const img = document.getElementById("carousel-img");

    function showImage(i) {
      img.src = images[i];
    }

    window.nextSlide = function () {
      index = (index + 1) % images.length;
      showImage(index);
    };

    window.prevSlide = function () {
      index = (index - 1 + images.length) % images.length;
      showImage(index);
    };
  });
</script>





## Conclusion
This pattern could inform our understanding of cosmic ray origins and Galactic magnetic fields.


---

<a href="{{ site.baseurl }}/experience/" class="back-link">← </a>
