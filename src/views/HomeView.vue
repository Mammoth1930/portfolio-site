<template>
  <div id="home">
    <section id="intro">
        <section>
            <div id="hello">
                <h1>Hello World!</h1>
                <div @mouseenter="startWave" @mouseleave="endWave">
                    <h1 id="wave-emoji" v-if="!wave">👋</h1>
                    <img id="wave-gif"
                        src="@/assets/img/emoji-wave.gif"
                        alt="Waving emoji"
                        v-if="wave"
                    />
                </div>
            </div>
            <p>My name is Riley Farrell.<br/>I'm a Computer Scientist specialising in Data Science and Engineering.</p>
        </section>
        <div id="profile-pic">
            <img src="@/assets/img/profile.jpg" alt="Profile picture">
        </div>
    </section>
    <section id="about">
        <NavBar/>
        <article>
            <h2>Overview</h2>
            <p>
                I’m a very hard-working, motivated and personable data professional, who recently graduated from one of Australia’s highest ranking universities, The University of Queensland, with a bachelor's degree in Computer Science. While completing this degree I fell in love with the theory and concepts of relational databases, artificial intelligence, and machine learning and as a result chose Data Science as the major for my degree. While studying I also chose to work casually at the university by helping to teach and develop content for a <a href="https://my.uq.edu.au/programs-courses/course.html?course_code=INFS1200&offer=53544c5543314558" target="_blank" rel="noopener noreferrer">first-year course</a> on relational databases and SQL. During my time at university, I was able to learn about and use many different data driven concepts and tools including:
            </p>
            
        </article>


    </section>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue"

export default {
  name: 'HomeView',
  components: {
    NavBar
  },
  data() {
    return {
        wave: false
    }
  },
  methods: {
    startWave() {
        this.wave = true
    },

    endWave() {
        this.wave = false
    }
  }
}
</script>

<style>
#intro {
    background-image: url("../assets/img/terminal.gif");
    background-size: cover;
    scroll-snap-align: start;
    display: flex;
    justify-content: space-between;
    height: 100vh;
}

#about {
    height: 100vh;
    scroll-snap-align: start;
}

#intro section:first-of-type {
    margin: auto 0;
}

#profile-pic {
    margin: 5vh 5vw 0 30px
}

#profile-pic img {
    border-radius: 20px;
    /* box-shadow: 5px 10px #13A10E; */
}

#hello {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin: 10vh 0 0 5vw;
}

#wave-emoji {
    width: 144px;
    height: 144px;

}

#wave-gif {
    width: 144px;
    height: 144px;
}

#intro p {
    margin-left: 5vw;
    color: #ddd;
}

#intro h1 {
    color: #ddd;
}

article h2 {
    margin-left: 100px;
    margin-top: 30px;
}

article p {
    margin: 30px 100px 0px 100px;
    font-size: 1.7em;
}
</style>
