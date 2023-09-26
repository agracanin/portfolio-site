<script setup>
</script>

<template>
    <section class="projects" id="projects">
        <h2>Projects</h2>
        <div class="project-left">
            <div class="project-display">
            </div>
            <div class="project-details">
                <h3 class="project-title">Weather App</h3>
                <p class="project-desc">Built a Weather App using OpenWeather API with asynchronous JavaScript</p>
                <div class="project-buttons">
                    <a href="" class="project-link live-demo">VIEW LIVE</a>
                    <a href="" class="project-link live-demo">VIEW SOURCE</a>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.projects {
    gap: 3em;
}

section>h2 {
    padding-top: 0;
}

.project-left {
    width: 100%;
    display: flex;
    padding: 0 5em;
}

.project-details {
    display: flex;
    flex-direction: column;
    gap: 1em;
    padding-left: 1em;
}

.project-display {
    background-image: url(../assets/images/weatherapp.png);
    width: 800px;
    height: 500px;
    background-position: center;
    background-size: cover;
    border-radius: 15px;
}

.project-buttons {
    display: flex;
    flex-direction: column;
    width: fit-content;
    gap: 1em;
}

.project-link {
    text-decoration: none;
    background-color: none;
    border-bottom: 5px solid #ff4d5a;
    text-align: center;
    color: inherit;
    font-size: 1em;
    padding: 1em 2em;
    transition: 500ms;
    font-weight: 500;
}

.project-link:hover {
    background-color: #ff4d5a;
}
</style>
