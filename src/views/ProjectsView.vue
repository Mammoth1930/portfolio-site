<template>
    <NavBar/>
    <section id="projects">
        <article>
            <h2>This Website</h2>
            <p>
                This portfolio site was designed and coded completely from scratch by me! The site demonstrates much of what I have learned in university about the principles of design and user experience. It also shows off some of my skills in web development languages such as HTML, CSS and JavaScript. This site was built using Vue.js a JavaScript framework I’d never used before undertaking this project.
            </p>
            <h2>Virality</h2>
            <p>
                Virality was my capstone project at university and was developed with the assistance of five other UQ computer science students in the final semester of their degree. Virality is a mobile game designed to educate users about the spread of infectious diseases.
            </p>
            <p>
                The premise of the game was that at the beginning of every week, a new mysterious virus would begin infecting a portion of the game's player base. The players then had one week to complete various educational minigames and puzzles which would allow them to unlock and share information about the mystery virus and contribute research points towards a vaccine. If the player base was able to work together and develop a vaccine for the correct disease by the end of the week they won.
            </p>
            <p>
                Perhaps the biggest feature and point of difference for Virality was the fact that it utilised Bluetooth connectivity on mobile devices to simulate the spread of infectious diseases. If a player who was infected in the game came within approximately thirty meters of a healthy player the two devices would connect via Bluetooth and the infected player would infect the healthy player with a random chance. Players who were infected would contribute less research to a vaccine upon completion of a puzzle. This meant that the player base had to avoid getting infected to increase the likelihood of them winning the game for that week.
            </p>
            <p>
                Virality also had a variety of other notable features such as built-in instant messaging, a glossary of over 10 unique potential diseases and three different educational puzzle types. At the end of the semester, our team was able to develop a fully featured prototype of the app which was available for download on any Android device. We also developed a backend web server for the app which allowed the application to communicate with our SQLite database via API requests. All of this was done in approximately nine weeks by our group of six students with a full-time university load.
            </p>
            <p>
                Our project was considered one of the best in our cohort and was nominated for <em>Best Software Project</em> in the UQ ITEE Innovation Showcase.
            </p>
            <p>
                The code for the application and backend is available to view on GitHub, however, unfortunately, UQ is no longer hosting our web server so the application will not work.
            </p>
            <Carousel/>
        </article>
    </section>
    <ThemeButton/>
  </template>

<script>
import NavBar from "@/components/NavBar.vue"
import ThemeButton from "@/components/ThemeButton.vue";
import Carousel from "@/components/Carousel.vue"

export default {
    name: "ProjectsView",
    components: {
        NavBar,
        ThemeButton,
        Carousel
    }
}
</script>

<style>

</style>