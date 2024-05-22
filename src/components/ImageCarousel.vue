<template>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 1px 1px 2px #333;"
    fade
    controls
    indicators
    background="#ababab"
  >
    <b-carousel-slide
      v-for="(image, index) in images"
      :key="index"
      :img-src="image.src"
      :caption="image.caption"
      :text="image.text"
    ></b-carousel-slide>
  </b-carousel>
</template>

<script>
import { BCarousel, BCarouselSlide } from 'bootstrap-vue-next';

export default {
  name: 'ImageCarousel',
  components: {
    BCarousel,
    BCarouselSlide
  },
  data() {
    return {
      images: [
        {
          src: require('@/assets/image1.jpg'), // Path relatif ke gambar pertama
          caption: '',
          text: ''
        },
        {
          src: require('@/assets/image2.jpg'), // Path relatif ke gambar kedua
          caption: '',
          text: ''
        },
        {
          src: require('@/assets/image3.jpg'), // Path relatif ke gambar ketiga
          caption: '',
          text: ''
        }
      ]
    };
  }
};
</script>

<style scoped>
#carousel-fade .carousel-inner {
  display: flex;
  align-items: center;
  height: 400px; /* Tinggi gambar pada tampilan desktop */
}

/* Responsive CSS untuk tampilan mobile */
@media (max-width: 767px) {
  #carousel-fade .carousel-inner {
    height: 250px; /* Mengurangi tinggi gambar pada tampilan mobile */
  }
}
</style>
