<script setup>
import HeroCanvas from './HeroCanvas.vue';
</script>

<template>
    <div class="hero" id="home">
        <HeroCanvas />
        <div class="heading-container">
            <h1 class="heading line1">Hello, I'm <span>Alen.</span></h1>
            <h1 class="heading line2">Front-end web developer.</h1>
        </div>
        <a href="#about">
            <button class="heading-button">View my work
                <svg xmlns="http://www.w3.org/2000/svg" width="30" height="24" viewBox="0 0 24 24" fill="none"
                    stroke="#ff4d5a" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    class="feather feather-arrow-down">
                    <line x1="12" y1="5" x2="12" y2="19"></line>
                    <polyline points="19 12 12 19 5 12"></polyline>
                </svg>
            </button>
        </a>
    </div>
</template>

<style scoped>
.hero {
    position: relative;
    z-index: 99999;
    display: flex;
    height: 100vh;
    width: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.heading {
    font-weight: 300;
    text-align: center;
    position: relative;
    z-index: 999;
    font-size: 4em;
}

h1>span {
    color: #ff4d5a;
}

.heading-button {
    background: none;
    display: flex;
    align-items: center;
    padding: 0.5em 1.3em;
    outline: none;
    border: 2px solid #ff4d5a;
    color: #ff4d5a;
    cursor: pointer;
    font-size: 1.4em;
    transition: 0.2s ease-in-out;
    transition-property: transform, background-color, color;
    border-radius: 5px;
}

.heading-button:hover,
.heading-button:hover>svg {
    transform: scale(1.1);
    background-color: #ff4d5a;
    color: #fafafa;
    stroke: #fafafa;
}

svg {
    margin-left: 0.5em;
}

a {
    text-decoration: none;
    margin-top: 1em;
    position: relative;
    z-index: 9999;
}
</style>
