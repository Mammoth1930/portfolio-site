<template>
    <div id="home">
        <NavBar/>
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
        <ThemeButton/>
    </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue"
import ThemeButton from "@/components/ThemeButton.vue"

export default {
  name: 'HomeView',
  components: {
    NavBar,
    ThemeButton
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
#home {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

#intro {
    background-image: url("../assets/img/terminal.gif");
    background-size: cover;
    display: flex;
    flex-grow: 1;
    justify-content: space-between;
    margin-top: 75px;
}

#intro section:first-of-type {
    margin: auto 0;
}

#profile-pic {
    margin: 5vh 5vw 0 30px
}

#profile-pic img {
    border-radius: 20px;
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
</style>
