<script setup>

</script>

<template>
    <div class="hero">
        <div class="heading-container">
            <h1 class="heading line1">Hello, I'm <span>Alen.</span></h1>
            <h1 class="heading line2">I'm a full stack web developer.</h1>
        </div>
        <a href="">
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
    display: flex;
    height: 100vh;
    width: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.heading {
    font-weight: 400;
    text-align: center;
}

h1>span {
    color: #ff4d5a;
}

.heading-button {
    background: none;
    display: flex;
    align-items: center;
    padding: 0.3em 1.5em;
    outline: none;
    border: 2px solid #ff4d5a;
    color: #ff4d5a;
    cursor: pointer;
    font-size: 1.4em;
}

svg {
    margin-left: 0.5em;
}

a {
    text-decoration: none;
    margin-top: 1em;
}
</style>
