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



<!-- === FIRST CAROUSEL === -->
<div class="carousel" data-carousel="1">
  <img class="carousel-image" src="{{ site.baseurl }}/assets/images/CPD_images/band 1.png" alt="Band image" />
  <button class="carousel-btn prev">&#9664;</button>
  <button class="carousel-btn next">&#9654;</button>
</div>



## Results

![Cosmic Ray Plot]({{ site.baseurl }}/assets/images/cosmic-ray-plot.png)

Our simulation shows a 3σ excess in one sky region, potentially indicating magnetic lensing.



<!-- === SECOND CAROUSEL === -->
<div class="carousel" data-carousel="2">
  <img class="carousel-image" src="{{ site.baseurl }}/assets/images/CPD_images/C10_1_36000_pwv1.fits-image-2025-04-04-23-41-49.png" alt="Fits Image" />
  <button class="carousel-btn prev">&#9664;</button>
  <button class="carousel-btn next">&#9654;</button>
  <p class="carousel-caption">Band 1</p>
</div>





## Conclusion
This pattern could inform our understanding of cosmic ray origins and Galactic magnetic fields.


<script>
  document.addEventListener("DOMContentLoaded", function () {
    const imageSets = {
      1: [
        "{{ site.baseurl }}/assets/images/CPD_images/band 1.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 3.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 4.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 5.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 6.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 7.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 8.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 9.png",
        "{{ site.baseurl }}/assets/images/CPD_images/band 10.png"
      ],
      2: [
        "{{ site.baseurl }}/assets/images/CPD_images/C10_1_36000_pwv1.fits-image-2025-04-04-23-41-49.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_3_36000_pwv1.fits-image-2025-04-04-23-42-51.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_4_36000_pwv1.fits-image-2025-04-04-23-44-20.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_5_36000_pwv1.fits-image-2025-04-04-23-45-34.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_6_36000_pwv1.fits-image-2025-04-04-23-47-28.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_7_36000_pwv1.fits-image-2025-04-04-23-48-47.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_8_36000_pwv1.fits-image-2025-04-04-23-50-02.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_9_36000_pwv1.fits-image-2025-04-04-23-51-46.png",
        "{{ site.baseurl }}/assets/images/CPD_images/C10_10_36000_pwv1.fits-image-2025-04-04-23-52-38.png"
      ]
    };

    const captions = {
      2: [
        "Band 1",
        "Band 3",
        "Band 4",
        "Band 5",
        "Band 6",
        "Band 7",
        "Band 8",
        "Band 9",
        "Band 10"
      ]
    };

    document.querySelectorAll("[data-carousel]").forEach((carousel) => {
      const id = carousel.getAttribute("data-carousel");
      const images = imageSets[id];
      const hasCaptions = captions[id] !== undefined;
      let index = 0;

      const img = carousel.querySelector(".carousel-image");
      const caption = hasCaptions ? carousel.querySelector(".carousel-caption") : null;

      function updateCarousel() {
        img.src = images[index];
        if (caption) caption.textContent = captions[id][index];
      }

      carousel.querySelector(".prev").addEventListener("click", () => {
        index = (index - 1 + images.length) % images.length;
        updateCarousel();
      });

      carousel.querySelector(".next").addEventListener("click", () => {
        index = (index + 1) % images.length;
        updateCarousel();
      });
    });
  });
</script>

---

<a href="{{ site.baseurl }}/experience/" class="back-link">← </a>
