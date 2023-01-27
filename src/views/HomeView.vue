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
                <p id="byline">My name is Riley Farrell.<br/>I'm a Computer Scientist specialising in Data Science and Engineering.</p>
            </section>
            <div id="profile-pic">
                <img src="@/assets/img/profile.jpg" alt="Profile picture">
            </div>
        </section>
    </div>
</template>

<script>
export default {
  name: 'HomeView',
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
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    margin: 10vh 0 0 5vw;
}

#wave-emoji {
    width: 144px;
    height: 144px;
    text-align: center;

}

#wave-gif {
    width: 144px;
    height: 140px;
}

#intro p {
    margin-left: 5vw;
    color: #ddd;
}

#intro h1 {
    color: #ddd;
}

/* Laptop size */
@media screen and (max-width: 1200px) {
    #profile-pic {
        width: 80vw;
    }

    #profile-pic img {
        max-width: 100%;
        max-height: 100%;
    }
}

/* Tablet size */
@media screen and (max-width: 800px) {
    
}

/* Mobile size */
@media screen and (max-width: 480px) {
    NavBar {
        display: none;
    }
}
</style>
