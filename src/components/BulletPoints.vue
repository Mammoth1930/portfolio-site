<template>
    <ul>
        <li v-for="point in points">{{ point }}</li>
    </ul>
</template>

<script>
export default {
    props: ['points']
}
</script>

<style scoped>
ul {
    columns: 2;
}

li {
    list-style-type: "🎓";
    padding-inline-start: 1ch;
    padding-bottom: 20px;
    margin-right: 50px;
}

li::marker {
    font-size: 1em;
}

/* Tablet size */
@media screen and (max-width: 740px) {
    ul {
        columns: 1;
    }
}
</style>