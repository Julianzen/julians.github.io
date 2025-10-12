---
layout: default
title: "Home"
---

# Hi, I'm Julian Shyu

Welcome to my website!  


Explore the pages below to learn more:
- [About Me](about.md)
- [Projects](projects.md)
- [Resume](resume.md)
- [Contact](contact.md)


<div style="text-align:center; margin-top: 30px;">
  <img id="mainImage" src="{{ '/assets/images/pic1.jpg' | relative_url }}" 
       alt="Gallery image"
       style="width:60%; max-width:500px; border-radius:10px; transition: opacity 0.5s ease;">

  <div style="margin-top:15px;">
    <button onclick="prevImage()">⬅️ Previous</button>
    <button onclick="nextImage()">Next ➡️</button>
  </div>
</div>

<script>
const images = [
  "{{ '/assets/images/main1.png' | relative_url }}",
  "{{ '/assets/images/main2.jpg' | relative_url }}"
];
let current = 0;

function showImage(index) {
  const img = document.getElementById("mainImage");
  img.style.opacity = 0;
  setTimeout(() => {
    img.src = images[index];
    img.style.opacity = 1;
  }, 300);
}

function nextImage() {
  current = (current + 1) % images.length;
  showImage(current);
}

function prevImage() {
  current = (current - 1 + images.length) % images.length;
  showImage(current);
}
</script>
