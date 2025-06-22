---
layout: default
title: Observability of Circumplanetary Disks
---
## Thesis Summary

These slides summarize my MSci thesis work modeling circumplanetary disk observability using RADMC-3D and ALMA synthetic imaging.


<div class="carousel" data-carousel="slides">
  <img class="carousel-image" src="{{ site.baseurl }}/assets/images/slides/slide1.png" alt="Slide 1" />
  <button class="carousel-btn prev">&#9664;</button>
  <button class="carousel-btn next">&#9654;</button>
</div>


<!-- === FIRST CAROUSEL === -->
<div class="carousel" data-carousel="1">
  <img class="carousel-image" src="{{ site.baseurl }}/assets/images/CPD_images/band 1.png" alt="Band image" />
  <button class="carousel-btn prev">&#9664;</button>
  <button class="carousel-btn next">&#9654;</button>
</div>



## Simulation Images




<!-- === SECOND CAROUSEL === -->
<div class="carousel" data-carousel="2">
  <img class="carousel-image" src="{{ site.baseurl }}/assets/images/CPD_images/C10_1_36000_pwv1.fits-image-2025-04-04-23-41-49.png" alt="Fits Image" />
  <button class="carousel-btn prev">&#9664;</button>
  <button class="carousel-btn next">&#9654;</button>
  <p class="carousel-caption">Band 1</p>
</div>





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
      ],
      slides: [
        "{{ site.baseurl }}/assets/images/slides/slide1.png",
        "{{ site.baseurl }}/assets/images/slides/slide2.png",
        "{{ site.baseurl }}/assets/images/slides/slide3.png",
        "{{ site.baseurl }}/assets/images/slides/slide4.png",
        "{{ site.baseurl }}/assets/images/slides/slide5.png",
        "{{ site.baseurl }}/assets/images/slides/slide6.png",
        "{{ site.baseurl }}/assets/images/slides/slide7.png",
        "{{ site.baseurl }}/assets/images/slides/slide8.png",
        "{{ site.baseurl }}/assets/images/slides/slide9.png",
        "{{ site.baseurl }}/assets/images/slides/slide10.png",
        "{{ site.baseurl }}/assets/images/slides/slide11.png",
        "{{ site.baseurl }}/assets/images/slides/slide12.png",
        "{{ site.baseurl }}/assets/images/slides/slide13.png",
        "{{ site.baseurl }}/assets/images/slides/slide14.png",
        "{{ site.baseurl }}/assets/images/slides/slide15.png"
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
