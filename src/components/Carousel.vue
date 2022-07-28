<template>
<div class="carousel-header">
  <a class="new">"Самое новое"</a>
  <a class="look-all">Смотреть все</a>
</div>

<swiper :space-between="-100" :slides-per-view="auto">
    <swiper-slide class="slide" ><Card/></swiper-slide>
    <swiper-slide class="slide"><Card/></swiper-slide>
    <swiper-slide class="slide"><Card/></swiper-slide>
  </swiper>
</template>
<script>
import Card from './Card.vue';
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'

  // import swiper module styles
  import 'swiper/css'
  import 'swiper/css/pagination'
  // more module style...

  export default {
    components: {
      Card,
      Swiper,
      SwiperSlide
    },
    setup() {
      return {
      }
    }
  }
</script>
<style scoped>

.swiper-wrapper {
  max-height: 309px;
}

.carousel-header {
  display: flex;
  justify-content: space-between;
  padding-left: 25px;
  padding-bottom: 18px;
}
.look-all {
  color: #FFFFFF;
  font-size: 16px;
}
.new {
  font-size: 16px;
}
.slide {
  margin-left: 25px;
  margin-bottom: 31px;
}
.card {
    width: 309px;
    height: 309px;
    background-color: white;
    background: #FFFFFF;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 36px;
}
</style>