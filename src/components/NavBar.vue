<template>
    <nav id="nav-bar">
        <ul id="nav-items">
            <li>
                <RouterLink :to="{name: 'Home'}">Home</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'About'}">About</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'Projects'}">Projects</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'Contact'}">Contact</RouterLink>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            current: null
        }
    }
}
</script>

<style scoped>
nav {
    display: flex;
    justify-content: center;
    position: fixed;
    top: 0;
    width: 100%;
    height: 75px;
    background-color: var(--background-color-secondary);
    z-index: 1000;
}

a {
    font-family: 'VT323', monospace;
    font-size: 4em;
    font-weight: 500;
    text-decoration: none;
    color: var(--text-primary-color);
}

.router-link-exact-active {
    text-decoration: underline;
    color: var(--accent-bright);
}

a::before, a::after{
    content: ">";
    color: rgba(0,0,0,0);
    display: inline-block;
}

a:hover::before {
    content: ">";
    color: var(--accent-bright);
}

#nav-items{
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-around;
    list-style: none;
    margin: 0;
    padding: 0;
}

/* Laptop size */
@media screen and (max-width: 1200px) {
    a {
        font-size: 3em;
    }
}

/* Tablet size */
@media screen and (max-width: 800px) {

}
</style>