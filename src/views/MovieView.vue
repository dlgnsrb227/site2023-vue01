<template>
  <ContTitle title="movie" />
  <MovieSlider :movies="movies" />
  <MovieSearch :onSearch="searchMovies" />
  <MovieTag />
  <MovieCont :movies="movies" />
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";

import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },

  setup() {
    const movies = ref([]);
    const searchs = ref([]);
    const search = ref("avengers");

    const searchMovies = async (query) => {
      await fetch(
        `https://api.themoviedb.org/3/search/movie?api_key=9be29262d25a4b248a7a8c73a358aa0d&query=${query}`
      )
        .then((response) => response.json())
        .then((result) => {
          movies.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };

    const TopMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=9be29262d25a4b248a7a8c73a358aa0d&query=${search.value}`
      )
        .then((response) => response.json())
        .then((result) => {
          movies.value = result.results;
          searchs.value = result.results;
          console.log(searchs);
        })
        .catch((error) => console.log("error", error));
    };
    TopMovies();

    return {
      movies,
      searchs,
      TopMovies,
      searchMovies,
    };
  },
};
</script>
