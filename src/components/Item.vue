<template>
  <div class="wrap">
    <swiper
    :direction="'vertical'"
    :simulateTouch="false"
    :slidesPerView="1"
    :speed="800"
    :mousewheel="true">
      <swiper-slide class="test1">Slide 1</swiper-slide>
      <swiper-slide class="test2">Slide 2</swiper-slide>
      <swiper-slide class="test3">Slide 3</swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';

import SwiperCore, {
  Mousewheel,Pagination
} from 'swiper/core';

SwiperCore.use([Mousewheel,Pagination]);

export default {
  name: 'Item',
  components: {
    Swiper,
    SwiperSlide,
  },
  methods: {
  }
}
</script>

<style scoped>
.wrap {
  height: 100%;
}
.swiper-container {
  width: 100%;
  height: calc(100% - 120px);
  margin-left: auto;
  margin-right: auto;
  position: relative;
  overflow: hidden;
  list-style: none;
  padding: 0;
  z-index: 1;
}

.swiper-container > :nth-child(n) {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  width: 100% !important;
  height: 100% !important;
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}
.test1 {
  background: #ccc;
}
.test2 {
  background: #f7f7f7
}
.test3 {
  background: #ccc;
}
</style>
