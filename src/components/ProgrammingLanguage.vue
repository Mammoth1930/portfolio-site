<template>
    <ul>
        <li v-for="language in languages" :class="language.rating">{{ language.name }}</li>
    </ul>
</template>

<script>
export default {
    props: ['languages']
}
</script>

<style scoped>
ul {
    columns: 2;
}

li {
    /* list-style-type: "5"; */
    list-style: none;
    /* padding-inline-start: 1ch; */
    padding-bottom: 20px;
}

.five::before {
    content: "★★★★★";
}

.four::before {
    content: "★★★★☆";
}

.three::before {
    content: "★★★☆☆";
}

.two::before {
    content: "★★☆☆☆";
}

.one::before {
    content: "★☆☆☆☆";
}

li::before {
    font-size: 1em;
    background: var(--background-color-secondary);
    vertical-align: baseline;
    margin-inline-end: 1ch;
    padding-inline: 1ch;
    border-radius: 1ch;
}
</style>