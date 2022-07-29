<template>
<div class="carousel-header">
  <a class="new">"Самое новое"</a>
  <a class="look-all">Смотреть все</a>
</div>

<swiper

:space-between="-70" 
:slides-per-view="auto" 
:slidesOffsetBefore="25"
:slidesOffsetAfter="-80"
:slideToClickedSlide="true"

>
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



.carousel-header {
  display: flex;
  justify-content: space-between;
  padding-left: 25px;
  padding-bottom: 18px;
  padding-top: 19px;
  padding-right: 24px ;
}
.look-all {
  color: #FFFFFF;
  font-size: 16px;
  cursor: pointer;
}
.new {
  cursor: pointer;
  font-size: 16px;
}
.slide {
  margin-bottom: 10px;
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