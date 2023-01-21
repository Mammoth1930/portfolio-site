<template>
    <NavBar/>
    <section id="contact">
        <article>
            <h2>Reach out!</h2>
        </article>
    </section>
    <ThemeButton/>
  </template>

<script>
import NavBar from "@/components/NavBar.vue"
import ThemeButton from "@/components/ThemeButton.vue";

export default {
    components: {
        NavBar,
        ThemeButton
    }
}
</script>