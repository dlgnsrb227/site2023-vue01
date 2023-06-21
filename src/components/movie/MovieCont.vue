<template>
  <div class="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/w500${movie.poster_path}`"
            :alt="movie.title"
          />
          <em>
            <span class="title">{{ movie.title }}</span>
            <span class="star">{{ movie.vote_average }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.movie__cont {
  ul {
    // column-count: 4;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    li {
      width: 24%;
      margin-bottom: 30px;
      position: relative;

      .title {
        font-size: 20px;

        &hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }
      .star {
        position: absolute;
        right: 20px;
        top: 20px;
        width: 30px;
        height: 30px;
        background-color: #fff;
        text-align: center;
        border-radius: 50%;
        line-height: 30px;
        font-size: 12px;
        font-weight: 800;
        color: #4d0000;
      }
    }
  }
}
// movie__search
.movie__search {
  margin-bottom: 50px;
  text-align: center;
  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
  }
  button {
    @include button(#56d8c2, #fff);
    @include border(50px);
  }
}
</style>
