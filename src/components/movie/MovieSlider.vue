<template>
  <div class="movie__slider">
    <Swiper
      effect="coverflow"
      :grabCursor="true"
      :centeredSlides="true"
      :slidesPerView="4"
      :spaceBetween="30"
      :loop="true"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: false,
      }"
      :modules="[Autoplay, Navigation, Pagination, EffectCoverflow]"
    >
      <SwiperSlide v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/w500${movie.poster_path}`"
            :alt="movie.title"
          />
        </a>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<script>
import { Navigation, Pagination, Autoplay, EffectCoverflow } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/scss/navigation";
import "swiper/scss/pagination";
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/bundle";

export default {
  props: {
    movies: {
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
      EffectCoverflow,
    };
  },
};
</script>

<style lang="scss">
.movie__slider {
  height: 70vh;

  img {
  }
}
</style>
