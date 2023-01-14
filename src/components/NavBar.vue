<template>
    <nav>
        <ul id="nav-items">
            <li>
                <RouterLink :to="{name: 'home'}">About</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'projects'}">Projects</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'resume'}">Resume</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'contact'}">Contact</RouterLink>
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
    position: sticky;
    background-color: var(--background-color-secondary);
}

a {
    font-family: 'VT323', monospace;
    font-size: 4em;
    font-weight: 500;
    text-decoration: none;
    color: var(--text-primary-color);
}

a:hover, .router-link-exact-active {
    text-decoration: underline;
    color: var(--accent-color);
}

#nav-items{
    display: flex;
    align-items: center;
    justify-content: space-around;
    list-style: none;
    margin: 0;
}
</style>