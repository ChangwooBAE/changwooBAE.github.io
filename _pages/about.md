---
layout: about
title: about
permalink: /
subtitle:

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  # more_info: >
  #   <p>555 your office number</p>
  #   <p>123 your address street</p>
  #   <p>Your City, State 12345 test</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

Hello, I am Changwoo Bae, a mechanical engineer and a physicist.

I received my Bachelor's and Master's degrees of Mechanical Engineer in [Soft Interface Laboratory](https://ifluid.khu.ac.kr) at Kyung Hee University advised by Prof. [Choongyeop Lee](https://scholar.google.com/citations?hl=en&user=4X93y-oAAAAJ) in South Korea. Later, I moved to France and received my PhD degree in Physics at [Institut Lumière Matière, Université de Lyon](https://ilm.univ-lyon1.fr) advised by Dr. [Anne-Laure Biance](https://scholar.google.com/citations?hl=en&user=aIZPs7oAAAAJ).

My primary research focuses on fluid dynamics at interfaces, such as superhydrophilic, superhydrophobic, surfactant laden interfaces, etc.

<div style="margin-top: 8rem;"></div>

## Research Highlights

<style>
.slideshow-container {
  position: relative;
  width: 100%;
  height: 500px;
  margin: 2rem 0 4rem 0;
  overflow: hidden;
}

.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding-top: 2rem;
}

.slide.active {
  opacity: 1;
}

.slide img {
  max-width: 100%;
  max-height: 80%;
  object-fit: contain;
  margin-top: 1rem;
  display: block; /* Ensure image is displayed as block */
}

.slide-title {
  margin-bottom: 1rem;
  font-size: 1.2rem;
  font-weight: bold;
  color: var(--global-theme-color);
  text-align: center;
  width: 100%;
  padding: 0 1rem;
}

@keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@keyframes fadeOut {
  0% { opacity: 1; }
  100% { opacity: 0; }
}

.slide {
  animation: fadeOut 2s forwards;
}

.slide.active {
  animation: fadeIn 2s forwards;
}

.slide-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
  border-radius: 50%;
  font-size: 1.2rem;
  transition: background-color 0.3s;
  z-index: 10;
}

.slide-nav:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.slide-nav.prev {
  left: 20px;
}

.slide-nav.next {
  right: 20px;
}
</style>

<div class="slideshow-container">
  <button class="slide-nav prev" id="prevButton">❮</button>
  <button class="slide-nav next" id="nextButton">❯</button>
  <div class="slide">
    <div class="slide-title">Rebound of a water drop from oil surface</div>
    <img src="{{ site.url }}{{ '/assets/img/webcover/Rebound.gif' | relative_url }}" alt="Rebound" loading="eager" onerror="this.onerror=null; this.src='{{ site.url }}{{ '/assets/img/webcover/Rebound.gif' | relative_url }}?t=' + new Date().getTime();"/>
  </div>
  <div class="slide">
    <div class="slide-title">Rotation of a water drop after bouncing</div>
    <img src="{{ site.url }}{{ '/assets/img/webcover/Rotation.gif' | relative_url }}" alt="Rotation" loading="eager" onerror="this.onerror=null; this.src='{{ site.url }}{{ '/assets/img/webcover/Rotation.gif' | relative_url }}?t=' + new Date().getTime();"/>
  </div>
  <div class="slide">
    <div class="slide-title">Reversal motion of a bubble with surfactant concentration</div>
    <img src="{{ site.url }}{{ '/assets/img/webcover/bubble_video.gif' | relative_url }}" alt="Bubble Video" loading="eager" onerror="this.onerror=null; this.src='{{ site.url }}{{ '/assets/img/webcover/bubble_video.gif' | relative_url }}?t=' + new Date().getTime();"/>
  </div>
  <div class="slide">
    <div class="slide-title">Multiple Bubble</div>
    <img src="{{ site.url }}{{ '/assets/img/webcover/multiplebubble.gif' | relative_url }}" alt="Multiple Bubble" loading="eager" onerror="this.onerror=null; this.src='{{ site.url }}{{ '/assets/img/webcover/multiplebubble.gif' | relative_url }}?t=' + new Date().getTime();"/>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  let currentSlide = 0;
  const slides = document.querySelectorAll('.slide');
  const totalSlides = slides.length;
  const prevButton = document.getElementById('prevButton');
  const nextButton = document.getElementById('nextButton');

  function showSlide(index) {
    // Hide all slides
    slides.forEach(slide => {
      slide.classList.remove('active');
      const img = slide.querySelector('img');
      // Force GIF to restart by updating src with timestamp
      const currentSrc = img.src.split('?')[0];
      img.src = currentSrc + '?t=' + new Date().getTime();
    });
    
    // Show current slide
    slides[index].classList.add('active');
  }

  function nextSlide() {
    currentSlide = (currentSlide + 1) % totalSlides;
    showSlide(currentSlide);
  }

  function prevSlide() {
    currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
    showSlide(currentSlide);
  }

  // Show first slide immediately
  showSlide(0);

  // Change slide every 20 seconds
  let slideInterval = setInterval(nextSlide, 20000);

  // Reset interval when manually changing slides
  function resetInterval() {
    clearInterval(slideInterval);
    slideInterval = setInterval(nextSlide, 20000);
  }

  // Add event listeners to buttons
  prevButton.addEventListener('click', function() {
    prevSlide();
    resetInterval();
  });

  nextButton.addEventListener('click', function() {
    nextSlide();
    resetInterval();
  });
});
</script>

