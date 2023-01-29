<template>
    <div id="home">
        <section id="intro">
            <div id="first-col">
                <div id="first-row">
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
                    <div id="profile-pic">
                        <img src="@/assets/img/profile.jpg" alt="Profile picture">
                    </div>
                </div>
                <p id="byline">My name is Riley Farrell.<br/>I'm a Computer Scientist specialising in Data Science and Engineering.</p>
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
    margin-top: 75px;
    height: 100%;
    background-image: url("../assets/img/terminal.gif");
    background-size: cover;
}

#first-row {
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
}

#first-col {
    max-width: 1400px;
    margin: auto;
    padding-top: 10vh;
}

#byline {
    margin-top: 0px;
}

#profile-pic {
    margin: 5vh 5vw 0 30px;
    max-width: 100%;
    flex-shrink: 2;
}

#profile-pic img {
    border-radius: 20px;
}

#hello {
    display: flex;
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
    white-space: nowrap;
}

/* Laptop size */
@media screen and (max-width: 1200px) {
    #profile-pic img {
        max-width: 100%;
        max-height: 100%;
    }
}

@media screen and (max-width: 780px) {
    #first-row {
        align-items: center;
    }
}

/* Tablet size */
@media screen and (max-width: 740px) {
    #intro {
        margin: 0;
    }

    #first-row {
        flex-direction: column;
        justify-content: center;
    }

    #first-col {
        padding: 0px;
    }

    #profile-pic {
        margin: 45px 20px;
    }

    #profile-pic img {
        max-height: 300px;
    }

    #hello {
        margin-left: 0px;
    }

    #hello h1{
        white-space: pre-wrap;
    }

    #hello div {
        display: none;
    }
}

/* Mobile size */
@media screen and (max-width: 420px) {
    #hello h1 {
        font-size: 4em;
        text-align: center;
    }

    #byline {
        font-size: 1.5em;
    }

    #first-col {
        margin-bottom: 100px;
    }
}
</style>
