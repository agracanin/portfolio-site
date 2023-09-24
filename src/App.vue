<script setup>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
import BackgroundCanvas from './components/BackgroundCanvas.vue';
import { ref, onMounted } from 'vue';

const activeSection = ref('home');

onMounted(() => {
  const sections = document.querySelectorAll('.hero, section');

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        activeSection.value = entry.target.id;
      }
    });
  }, { threshold: 0.5 });

  sections.forEach(section => observer.observe(section));
});

</script>

<template>
  <Hero />
  <Navbar />
  <BackgroundCanvas />
  <About />
</template>

<style scoped></style>
