<template>
    <NavBar id="nav-bar"/>
    <NavMenu id="nav-menu"/>
    <router-view/>
    <ThemeButton/>
</template>

<script>
import NavBar from "@/components/NavBar.vue"
import ThemeButton from "@/components/ThemeButton.vue"
import NavMenu from "@/components/NavMenu.vue"

export default {
    components: {
        NavBar,
        ThemeButton,
        NavMenu
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
    --background-color-primary: #cacaca;
    --background-color-secondary: #ebebeb;
    --accent-color: #fafafa;
    --text-primary-color: #222;
    --element-size: 4rem;
    --accent-bright: #5a24a7;
    
}

/* Define styles for the root window with dark - mode preference */
:root.dark-theme {
    --background-color-primary: #0c0c0c;
    --background-color-secondary: #1e1e1e;
    /* --background-color-secondary: #2d2d30; */
    --accent-color: #3f3f3f;
    --text-primary-color: #ddd;
    --accent-bright: #76f843;
}

p, a{
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

/* Mobile size */
@media screen and (max-width: 740px) {
    #nav-bar {
        display: none;
    }
}

@media screen and (max-width: 600px) {
    h1 {
        font-size: 4em;
    }

    h2 {
        font-size: 3em;
    }

    h3 {
        font-size: 2em;
    }

    h4 {
        font-size: 1em;
    }

    article p {
        margin: 20px 15px 0px 15px !important;
        font-size: 1.3em !important;
    }

    article h2, article h3 {
        margin-left: 15px !important;
    }
}
</style>
