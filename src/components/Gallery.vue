<template>
    <div id="gallery">
        <div class="row">
            <div class="col" v-for="img in imgs">
                <img :src="getImgUrl(img.name)" :alt="img.alt" :title="img.alt"/>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['imgs'],
    methods: {
        getImgUrl(pic) {
            return require('../assets/img/technologies/'+pic)
        }
    }
}
</script>

<style scoped>
#gallery {
    background: var(--background-color-secondary);
    border-radius: 1ch;
    margin: 50px 100px;
}

.row {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-evenly;
}

.col {
    /* background-color: grey; */
    /* border-radius: 1ch; */
    width: 150px;
    height: 150px;
    margin: 20px;
    display: flex;
    align-items: center;

}

img {
    max-width: 150px;
    max-height: 150px;
}

/* Tablet size */
@media screen and (max-width: 740px) {
    #gallery {
        margin: 50px;
    }
}

@media screen and (max-width: 600px) {
    #gallery {
        margin: 50px 15px;
    }
}

@media screen and (max-width: 420px) {
    .col {
        width: 60px;
        height: 60px;
    }

    img {
        max-width: 60px;
        max-height: 60px;
    }
}
</style>