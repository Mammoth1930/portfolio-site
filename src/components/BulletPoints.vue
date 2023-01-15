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
</style>