<template>
<a :href="link" target="_blank" rel="noopener noreferrer">{{ text }}</a>
</template>

<script>
export default {
    props: [
        'link',
        'text'
    ]
}
</script>

<style scoped>
a {
    display: inline-block;
    background-color: transparent;
    color: var(--text-primary-color);
    font-size: 1.7em;
    text-decoration: none;
    text-align: center;
    padding: 16px 32px;
    margin: 4px 2px;
    border: 2px solid var(--accent-bright);
    border-radius: 1ch;
    transition-duration: 0.4s;
    cursor: pointer;
}

a:hover {
    background-color: var(--accent-bright);
    text-decoration: none;
    color: #222;
}

@media screen and (max-width: 420px) {
    a {
        font-size: 1.5em;
    }
}
</style>