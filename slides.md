<script>
// Слайдер на JavaScript
let currentSlide = 0;
const slides = document.querySelectorAll('.slide');

function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.style.display = i === index ? 'block' : 'none';
    });
}

function nextSlide() {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
}

function prevSlide() {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
}

window.onload = function() {
    showSlide(currentSlide);
}
</script>

---
# Slide 1
![Image 1](https://via.placeholder.com/600x400?text=Image+1)

---
# Slide 2
![Image 2](https://via.placeholder.com/600x400?text=Image+2)

---
# Slide 3
![Image 3](https://via.placeholder.com/600x400?text=Image+3)

<!-- Controls -->
<button onclick="prevSlide()">❮ Prev</button>
<button onclick="nextSlide()">Next ❯</button>
