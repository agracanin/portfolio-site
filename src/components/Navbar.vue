<script setup>
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
    }, { threshold: 0.3 });

    sections.forEach(section => observer.observe(section));
});
</script>

<template>
    <nav class="nav-bar">
        <ul class="navigation">
            <a href="#home">
                <li class="nav-item" :class="{ active: activeSection === 'home' }">Home</li>
            </a>
            <a href="#about">
                <li class="nav-item" :class="{ active: activeSection === 'about' }">About</li>
            </a>
            <a href="#projects">
                <li class="nav-item" :class="{ active: activeSection === 'projects' }">Projects</li>
            </a>
            <a href="#contact">
                <li class="nav-item" :class="{ active: activeSection === 'contact' }">Contact</li>
            </a>
        </ul>
    </nav>
</template>

<style scoped>
.nav-bar {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    position: sticky;
    top: 0;
    height: 3em;
    background-color: rgba(40, 40, 40, 0.95);
    border-bottom: 1px solid #1a1a1a;
    backdrop-filter: blur(8px);
    box-shadow: 0 4px 4px rgba(0, 0, 0, 0.3);
    z-index: 9999999;
}

.navigation {
    display: flex;
    list-style: none;
    padding-right: 2em;
    gap: 2em;
}

.nav-item {
    cursor: pointer;
    font-weight: 500;
    font-size: 1.2em;
    transition: 200ms ease-in-out;
}

.nav-item:hover {
    color: #ff4d5a;
}

a {
    text-decoration: none;
    color: inherit;
}


@media (max-width: 840px) {
    .nav-bar {
        justify-content: center;
        font-size: 0.8em;
    }

    .navigation {
        padding-right: 0;
    }
}

@media(max-width: 650px) {
    .nav-bar {
        font-size: 0.7em;
    }
}
</style>
