<template>
  <div id="home">
    <span id="intro">
        <section>
            <div id="hello" @mouseenter="startWave" @mouseleave="endWave">
                <h1>Hello!</h1>
                <h1 id="wave-emoji" v-if="!wave">👋</h1>
                <img id="wave-gif"
                    src="@/assets/img/emoji-wave.gif"
                    alt="Waving emoji"
                    v-if="wave"
                />
            </div>
            <p>My name is Riley Farrell.<br/>I'm a Computer Scientist specialising in Data Science and Engineering.</p>
        </section>
        <div id="profile-pic">
            <img src="@/assets/img/profile.jpg" alt="Profile picture">
        </div>
    </span>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  components: {

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
    background-image: url("../assets/img/terminal.gif");
    background-size: cover;
}

#intro {
    display: flex;
    justify-content: space-between;
    height: 100vh;
}

#intro section:first-of-type {
    margin: auto 0;
}

#profile-pic {
    margin: 5vh 5vw 0 30px
}

#profile-pic img {
    border-radius: 20px;
    /* box-shadow: 2px 5px rgba(0,0,0,0.2); */
}

#hello {
    display: flex;
    align-items: center;
    justify-content: start;
    margin: 10vh 0 0 5vw;
}

#hello h1 {
    font-family: 'VT323', monospace;
    font-size: 5em;
    margin: 0;
}

#wave-emoji {
    font-size: 144px;
    width: 144px;
    height: 144px;

}

#wave-gif {
    width: 144px;
    height: 144px;
}

p {
    font-family: 'Roboto', sans-serif;
    font-size: 2em;
    margin-left: 5vw;
    color: #ddd;
}

h1 {
    color: #ddd;
}
</style>
