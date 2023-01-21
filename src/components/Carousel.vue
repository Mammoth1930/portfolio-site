<template>
    <carousel
        id="carousel-main"
        :items-to-show="1"
        :wrapAround="true"
        v-model="currentSlide"
        :autoplay="0"
        :pause-autoplay-on-hover="true"
    >
      <slide v-for="slide in images" :key="slide">
        <div class="carousel__item">
            <img class="carousel-img" :src="getImgUrl(slide)"/>
        </div>
      </slide>
  
      <template #addons>
        <navigation />
      </template>
    </carousel>
    <Carousel
        id="thumbnails"
        :items-to-show="6"
        :wrap-around="true"
        v-model="currentSlide"
        ref="carousel"
    >
        <Slide v-for="slide in images" :key="slide">
            <div class="carousel__item" @click="slideTo(images.indexOf(slide))">
                <img class="carousel-thumb" :src="getImgUrl(slide)"/>
            </div>
        </Slide>
    </Carousel>
  </template>
  
  <script>
  import 'vue3-carousel/dist/carousel.css'
  import { Carousel, Slide, Navigation } from 'vue3-carousel'
import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'CarouselGallery',
    components: {
      Carousel,
      Slide,
      Navigation,
    },
    methods: {
        getImgUrl(pic) {
            return require('../assets/img/virality/'+pic)
        },
        slideTo(val) {
            this.currentSlide = val
        }
    },
    data() {
        return {
            currentSlide: 0,
            images: [
                'showcase.jpg',
                'showcase2.jpg',
                'chat.png',
                'crossword.png',
                'demo.png',
                'glossary.png',
                'home.png',
                'leaderboard.png',
                'prototype.png',
                'sequence.png'
            ]
        }
    }
  })
  </script>

<style>
#carousel-main {
    margin-top: 5ch;
}

#thumbnails {
    margin: 0;
}

.carousel-thumb {
    max-height: 100px;
    max-width: 300px;
    cursor: pointer;
}

.carousel-img {
    max-width: 100%;
    max-height: 700px;
}

.carousel__item {
  min-height: 200px;
  width: 100%;
  background-color: transparent;
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  color: var(--text-primary-color);
  /* border: 5px solid var(--text-primary-color); */
}

.carousel__prev:hover,
.carousel__next:hover {
  box-sizing: content-box;
  color: var(--accent-bright);
  /* border: 5px solid var(--text-primary-color); */
}
</style>
  