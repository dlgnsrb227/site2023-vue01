<template>
  <ContTitle title="movie" />
  <MovieSlider />
  <MovieSearch />
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
    };
  },
};
</script>
