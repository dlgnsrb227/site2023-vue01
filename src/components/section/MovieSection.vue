<template>
  <section id="movieSection" :class="attr">
    <div class="movie__inner container">
      <div class="movie__text">
        <h3>추천 movie</h3>
        <p>추천 영화를 구경하고 감상해보세요 !</p>
        <router-link to="#" class="button-green"> 자세히보기 </router-link>
      </div>
      <div class="movie__item">
        <div>
          <img src="@/assets/img/movie/movie01.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie02.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie03.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie04.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie05.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie06.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie07.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie08.png" alt="영화썸네일이미지" />
        </div>
        <div>
          <img src="@/assets/img/movie/movie09.png" alt="영화썸네일이미지" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: { attr: String },
};
</script>

<style lang="scss">
// unsplash__wrap
.movie__wrap {
  overflow: hidden;
}
.movie__inner {
  height: 700px;
  // overflow: hidden;

  .movie__text {
    > h3 {
      font-size: 50px;
      font-weight: 600;
      margin-bottom: 30px;
    }
    > p {
      font-size: 24px;
      margin-bottom: 30px;
    }
    > a {
      border-radius: 30px;
      font-size: 18px;
      margin-bottom: 100px;
    }
  }
  .movie__item {
    // width: 200%;
    position: absolute;
    display: flex;

    > div {
      margin-right: 20px;
      width: 200px;

      img {
        width: 100%;
        border-radius: 20px;
      }
    }
  }
}

// movie__cont
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
