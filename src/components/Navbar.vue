<script setup>
</script>

<template>
    <nav class="nav-bar">
        <ul class="navigation">
            <li class="nav-item">Home</li>
            <li class="nav-item">About</li>
            <li class="nav-item">Projects</li>
            <li class="nav-item">Contact</li>
        </ul>
    </nav>
</template>

<style scoped>
.nav-bar {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    position: sticky;
    height: 3em;
    background-color: rgba(40, 40, 40, 0.95);
    border-bottom: 1px solid #1a1a1a;
    backdrop-filter: blur(8px);
    box-shadow: 0 4px 4px rgba(0, 0, 0, 0.3);
    z-index: 999;
}

.navigation {
    display: flex;
    list-style: none;
    padding-right: 1.5em;
    gap: 1em;
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
</style>
