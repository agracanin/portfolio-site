<script setup>
</script>

<template>
    <section class="projects" id="projects">
        <h2>Projects</h2>
        <div class="project-container">
            <div class="project-display">
                <h1>PLACEHOLDER</h1>
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
        <div class="project-container">
            <div class="project-details details-left">
                <h3 class="project-title">Weather App</h3>
                <p class="project-desc">Built a Weather App using OpenWeather API with asynchronous JavaScript</p>
                <div class="project-buttons">
                    <a href="" class="project-link live-demo">VIEW LIVE</a>
                    <a href="" class="project-link live-demo">VIEW SOURCE</a>
                </div>
            </div>
            <div class="project-display">
                <h1>PLACEHOLDER</h1>
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

.project-container {
    width: 100%;
    display: flex;
    padding: 0 5em;
}

.project-details {
    display: flex;
    flex-direction: column;
    gap: 1em;
    padding-left: 1em;
    width: 30vw;
    margin-top: 5em;

}

.project-display {
    height: 80vh;
    width: 60vw;
    margin-left: 1em;
    background-color: rgba(46, 46, 46, 0.1);
    display: flex;
    align-items: center;
    justify-content: center;
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
    text-align: center;
    color: inherit;
    font-size: 1em;
    padding: 1em 2em;
    transition: box-shadow .15s ease-in-out;
    font-weight: 500;
    box-shadow: inset 0 -5px 0 -1px #ff4d5a;
}

.project-link:hover {
    box-shadow: inset 0 -100px 0 -1px #ff4d5a;
}

.project-desc {
    padding-right: 5em;
}

.project-img {
    width: 90%;
    height: 90%;
    object-fit: cover;
}
</style>
