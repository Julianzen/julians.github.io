---
layout: default
title: "Home"
---

# Hi, I'm Julian Shyu

Welcome to my website!  

*This site is currently a work in progress. It will be updated as I go.*

Explore the pages below to learn more:
- [About Me](about.md)
- [Projects](projects.md)
- [Resume](resume.md)
- [Contact](contact.md)


<div style="text-align:center; margin-top: 30px;">
  <img id="mainImage" src="https://julianzen.github.io/julians.github.io/assets/images/IMG_6391.png" 
       alt="Gallery image"
       style="width:60%; max-width:500px; border-radius:10px; transition: opacity 0.5s ease;">

  <div style="margin-top:15px;">
    <button onclick="prevImage()">⬅️ Previous</button>
    <button onclick="nextImage()">Next ➡️</button>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const images = [
    "https://julianzen.github.io/julians.github.io/assets/images/IMG_6391.png",
    "https://julianzen.github.io/julians.github.io/assets/images/IMG_2366.jpg"
  ];
  let current = 0;
  const img = document.getElementById("mainImage");

  function showImage(index) {
    img.style.opacity = 0;
    setTimeout(() => {
      img.src = images[index];
      img.style.opacity = 1;
    }, 300);
  }

  window.nextImage = function() {
    current = (current + 1) % images.length;
    showImage(current);
  };

  window.prevImage = function() {
    current = (current - 1 + images.length) % images.length;
    showImage(current);
  };
});
</script>
