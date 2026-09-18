<script setup lang="ts">
import { ref, onMounted } from 'vue'

const carouselRef = ref<HTMLElement | null>(null)

onMounted(() => {
  const carousel = carouselRef.value
  if (!carousel) return

  const track = carousel.querySelector<HTMLDivElement>('.carousel-slides')
  const slides = carousel.querySelectorAll<HTMLDivElement>('.carousel-slide')
  const dotsWrap = carousel.querySelector<HTMLDivElement>('.carousel-dots')
  const prevBtn = carousel.querySelector<HTMLButtonElement>('.arrow.prev')
  const nextBtn = carousel.querySelector<HTMLButtonElement>('.arrow.next')

  if (!track || !dotsWrap || slides.length === 0 || !prevBtn || !nextBtn) {
    console.warn('Неполная структура карусели', carousel)
    return
  }

  const slideWidth = () => slides[0].offsetWidth

  // Генерация точек
  const dots: HTMLButtonElement[] = []
  slides.forEach((_, i) => {
    const dot = document.createElement('button')
    dot.className = `dot${i === 0 ? ' active' : ''}`
    dot.setAttribute('aria-label', `Слайд ${i + 1}`)
    dot.addEventListener('click', () => {
      track.scrollTo({ left: slides[i].offsetLeft, behavior: 'smooth' })
    })
    dotsWrap.appendChild(dot)
    dots.push(dot)
  })

  // Обновление активной точки при скролле
  const updateDots = (): void => {
    const idx = Math.round(track.scrollLeft / slideWidth())
    dots.forEach((dot, i) => {
      dot.classList.toggle('active', i === idx)
    })
  }

  track.addEventListener('scroll', updateDots, { passive: true })

  prevBtn.addEventListener('click', () => {
    track.scrollBy({ left: -slideWidth(), behavior: 'smooth' })
  })

  nextBtn.addEventListener('click', () => {
    track.scrollBy({ left: slideWidth(), behavior: 'smooth' })
  })
})
</script>


<template>
  <section class="gallery" id="works">
    <div class="container">
      <div class="section-tag">Наши работы</div>
      <div class="carousel" ref="carouselRef">
        <div class="carousel-slides">
          <div class="carousel-slide" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTs6S9b8X3a5RIFw91HX5fvnmxfwuTuD3XS4PjqeVJ8UQ&s=10')"></div>
          <div class="carousel-slide" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQkPvVV9wff5252qq7hJlpHTmEXNYY-tyrv_4ZtoUDpJQ&s=10')"></div>
          <div class="carousel-slide" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTJzhC2HYR5Y5hehWN9F35Iv6tIXaj4v_azZIlYiy_Z3A&s=10')"></div>
        </div>

        <button class="arrow prev" aria-label="Назад">❮</button>
        <button class="arrow next" aria-label="Вперед">❯</button>

        <div class="carousel-dots"></div>
      </div>
  </div>
  </section>
</template>


<style scoped>
.gallery {
  background-color: #F1ECE9;
}

.container {
  max-width: 1240px;
  margin: 0 auto;
  padding: 0 32px;
}
.carousel {
  position: relative;
  width: 100%;
  margin: 0 auto;
  aspect-ratio: 16 / 9;
  border-radius: 10px;
  overflow: hidden;
  border: #1F272E solid 5px;
}
.section-tag 
{
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    text-transform: uppercase;
    letter-spacing: 0.2em;
    display: inline-flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 24px;
}
.section-tag::before 
{ 
    content: "";
    width: 40px;
    height: 1px;
    background-color: black;
}

.carousel-slides {
  display: flex;
  width: 100%;
  height: 100%;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;
  scrollbar-width: none; 
}

.carousel-slides::-webkit-scrollbar {
  display: none; 
}

.carousel-slide {
  flex: 0 0 100%;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  scroll-snap-align: start;
}

.arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  background-color: #F1ECE9;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  font-size: 20px;
  color: #333;
  z-index: 10;
  transition: background-color 0.2s;
}
section { padding: 120px 0; }

.arrow.prev { left: 20px; }
.arrow.next { right: 20px; }
.arrow:hover { background-color: #F96F52; }

.carousel-dots {
  position: absolute;
  bottom: 15px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 10px;
  z-index: 10;
}

.dot {
  width: 12px;
  height: 12px;
  background-color: rgba(255, 255, 255, 0.5);
  border: none;
  border-radius: 50%;
  cursor: pointer;
  transition: background-color 0.2s, transform 0.2s;
}

.dot.active {
  background-color: #F1ECE9;
  transform: scale(1.2);
}

</style>