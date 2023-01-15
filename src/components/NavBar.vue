<template>
    <nav id="nav-bar">
        <ul id="nav-items">
            <li>
                <RouterLink :to="{name: 'home'}">Home</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'about'}">About</RouterLink>
            </li>
            <li>
                <RouterLink :to="{name: 'projects'}">Projects</RouterLink>
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
    position: fixed;
    top: 0;
    width: 100%;
    height: 75px;
    background-color: var(--background-color-secondary);
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
    align-items: center;
    justify-content: space-around;
    list-style: none;
    margin: 0;
}
</style>