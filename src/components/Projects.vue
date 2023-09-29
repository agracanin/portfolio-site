<script setup>
</script>

<template>
    <section class="projects" id="projects">
        <h2>Projects</h2>
        <div class="project-container project-left">
            <div class="project-display">
                <img src="../assets/images/etch-a-sketch.png" alt="Project image">
            </div>
            <div class="project-details">
                <h3 class="project-title">Etch A Sketch</h3>
                <p class="project-desc">Create pixel art using a variety of features and colors! Made with JavaScript, HTML
                    and CSS.</p>
                <div class="project-buttons">
                    <a href="https://agracanin.github.io/etch-a-sketch/" class="project-link">VIEW LIVE</a>
                    <a href="https://github.com/agracanin/etch-a-sketch" class="project-link">VIEW SOURCE</a>
                </div>
            </div>
        </div>
        <div class="project-container project-right">
            <div class="project-details">
                <h3 class="project-title">Weather App</h3>
                <p class="project-desc">A Weather App that uses WeatherAPI with asynchronous JavaScript to fetch the
                    current forecast of an entered location.</p>
                <div class="project-buttons">
                    <a href="https://agracanin.github.io/weather-app/" class="project-link">VIEW LIVE</a>
                    <a href="https://github.com/agracanin/weather-app" class="project-link">VIEW SOURCE</a>
                </div>
            </div>
            <div class="project-display">
                <img src="../assets/images/weatherapp.png" alt="Project image">
            </div>
        </div>
        <div class="project-container project-left">
            <div class="project-display">
                <img src="../assets/images/calculator.png" alt="Project image">
            </div>
            <div class="project-details">
                <h3 class="project-title">Calculator App</h3>
                <p class="project-desc">A basic calculator with basic arithmetic operations, decimal
                    inputs, and a user-friendly interface that supports both mouse clicks and keyboard inputs.</p>
                <div class="project-buttons">
                    <a href="https://agracanin.github.io/Calculator/" class="project-link">VIEW LIVE</a>
                    <a href="https://github.com/agracanin/Calculator" class="project-link">VIEW SOURCE</a>
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

.project-container {
    width: 100%;
    display: flex;
}

.project-details {
    display: flex;
    flex-direction: column;
    gap: 0.5em;
    width: 25%;
    justify-content: center;
}

.project-title {
    font-size: 2em;
    color: #ff4d5a;
}

.project-display {
    height: 80vh;
    width: 75%;
    background-color: rgba(46, 46, 46, 0.1);
    display: flex;
    align-items: center;
    justify-content: center;
}

.project-left {
    padding-left: 6em
}

.project-left>.project-details {
    transform: translateX(-25%);
}


.project-right {
    padding-right: 6em;
}

.project-right>.project-details {
    transform: translateX(50%);
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

img {
    width: 80%;
    height: 80%;
    object-fit: cover;
}


@media(max-width: 650px) {
    .project-display {
        width: 65%;
        height: 30vh;
        background-color: transparent;
    }

    img {
        width: 100%;
        height: 100%;
    }

    .project-display>h1 {
        display: none;
    }

    .project-details {
        width: 35%;
        background-color: rgba(26, 26, 26, 0.5);
    }

    .project-link {
        font-size: 12px;
    }

    .project-title {
        font-size: 1.1em;
    }

    .project-desc {
        font-weight: 500;
        font-size: 12px;
    }

    .project-left>.project-details {
        transform: translateX(-20%);
        padding-left: 5px;
    }

    .project-right>.project-details {
        transform: translateX(15%);
    }
}

@media (max-width: 840px) {
    .project-container {
        padding: 0;
    }
}
</style>
