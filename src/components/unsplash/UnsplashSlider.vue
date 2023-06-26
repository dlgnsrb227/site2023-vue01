<template>
  <div class="unsplash__slider">
    <Swiper
      effect="cube"
      :cubeEffect="{
        shadow: true,
        slideShadows: true,
        shadowOffset: 20,
        shadowScale: 0.89,
      }"
      :grabCursor="true"
      :centeredSlides="true"
      :slidesPerView="1"
      :spaceBetween="30"
      :loop="true"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: false,
      }"
      :modules="[Autoplay, Navigation, Pagination, EffectCube]"
    >
      <SwiperSlide v-for="(image, index) in images" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`">
          <img :src="image.urls.regular" :alt="image.alt_description" />
        </a>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<script>
import { Navigation, Pagination, Autoplay, EffectCube } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/scss/navigation";
import "swiper/scss/pagination";
import "swiper/css";
import "swiper/css/effect-cube";
import "swiper/css/bundle";

export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      Swiper,
      SwiperSlide,
      Navigation,
      Pagination,
      Autoplay,
      EffectCube,
    };
  },
};
</script>

<style lang="scss">
.unsplash__slider {
  margin-bottom: 100px;
  .swiper {
    width: 300px;
    height: 300px;

    img {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
