<template>
  <div id="home">
    <section id="intro">
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
    </section>
    <section id="about">
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloribus dolorem architecto iste numquam alias corrupti necessitatibus odit soluta, minima amet inventore repellat eligendi consectetur aperiam quasi nam iure aliquam eaque aspernatur ipsa culpa quaerat dignissimos? Consectetur temporibus recusandae reiciendis corrupti quae laborum cupiditate commodi, esse, fugiat quibusdam, omnis odit enim dolores sit voluptatum ipsum adipisci magnam perferendis non nesciunt dolorum eaque qui ad? At, iusto provident natus incidunt numquam ad nulla possimus eaque iure cumque temporibus asperiores placeat dolores vero sapiente molestiae, tempora voluptatum. Impedit, tenetur placeat. Qui incidunt culpa et perspiciatis, quibusdam fugiat eaque atque recusandae, veniam quisquam eius.</p>

        <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Facere consequatur accusantium ut maxime ex assumenda odit deleniti, odio beatae corporis, facilis cum sed illum. Nostrum, doloribus provident. Quidem consectetur ut dicta itaque necessitatibus veniam veritatis reprehenderit voluptates ipsum nesciunt, cum perspiciatis ratione, nostrum doloribus exercitationem nam placeat eum facere! Reiciendis, odio! Harum ea voluptatum, facere minus error praesentium commodi mollitia! Iste pariatur dolores temporibus vel quos. Mollitia, velit maxime, nobis consectetur rerum aut aspernatur vel fugiat soluta doloremque iste nulla reiciendis delectus recusandae beatae excepturi, nemo eos veritatis facilis impedit eum quisquam perspiciatis? Neque voluptates dignissimos commodi dolores perferendis possimus.
        </p>
        <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Facere consequatur accusantium ut maxime ex assumenda odit deleniti, odio beatae corporis, facilis cum sed illum. Nostrum, doloribus provident. Quidem consectetur ut dicta itaque necessitatibus veniam veritatis reprehenderit voluptates ipsum nesciunt, cum perspiciatis ratione, nostrum doloribus exercitationem nam placeat eum facere! Reiciendis, odio! Harum ea voluptatum, facere minus error praesentium commodi mollitia! Iste pariatur dolores temporibus vel quos. Mollitia, velit maxime, nobis consectetur rerum aut aspernatur vel fugiat soluta doloremque iste nulla reiciendis delectus recusandae beatae excepturi, nemo eos veritatis facilis impedit eum quisquam perspiciatis? Neque voluptates dignissimos commodi dolores perferendis possimus.
        </p>


    </section>
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
#intro {
    background-image: url("../assets/img/terminal.gif");
    background-size: cover;
    scroll-snap-align: start;
    display: flex;
    justify-content: space-between;
    height: 100vh;
}

#about {
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
}

#hello {
    display: flex;
    align-items: center;
    justify-content: flex-start;
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

#intro p {
    margin-left: 5vw;
    color: #ddd;
}

#intro h1 {
    color: #ddd;
}
</style>
