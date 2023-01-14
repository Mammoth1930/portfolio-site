<template>
    <router-view/>
    <theme-button />
</template>

<script>
import ThemeButton from "@/components/ThemeButton.vue"
export default {
    components: {
        ThemeButton
    }
}
</script>

<style>
html,
body {
    scroll-snap-type: y mandatory;
    padding: 0;
    margin: 0;
    background-color: var(--background-color-primary);
    color: var(--text-primary-color);
}
/* Define styles for the default root window element */
:root {
    --background-color-primary: #ebebeb;
    --background-color-secondary: #fafafa;
    --accent-color: #cacaca;
    --text-primary-color: #222;
    --element-size: 4rem;
}

/* Define styles for the root window with dark - mode preference */
:root.dark-theme {
    --background-color-primary: #0c0c0c;
    --background-color-secondary: #1e1e1e;
    /* --background-color-secondary: #2d2d30; */
    --accent-color: #3f3f3f;
    --text-primary-color: #ddd;
}

p {
    font-family: 'Roboto', sans-serif;
    font-size: 2em;
}

h1, h2, h3, h4, h5, h6 {
    font-family: 'VT323', monospace;
    margin: 0;
}

h1 {
    font-size: 5em;
}

h2 {
    font-size: 4em;
}

h3 {
    font-size: 3em;
}

h4 {
    font-size: 2em;
}

.container-center {
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
}

.card {
    padding: 2rem 4rem;
    height: 200px;
    width: 300px;
    text-align: center;
    border: 1px solid var(--accent-color);
    border-radius: 4px;
    background-color: var(--background-color-secondary);
}
</style>
