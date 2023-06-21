<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="youtube__text">
        <h3>추천 유튜브</h3>
        <p>
          더 다양한 강의는 유튜브를 통해 제공하고 있습니다.
          <br />
          구독과 좋아요! 부탁드립니다.
        </p>
        <router-link to="#" class="button-red"> 자세히보기 </router-link>
      </div>
      <div class="youtube__item">
        <div>
          <img
            src="@/assets/img/youtube/youtube01.png"
            alt="유튜브썸네일이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/youtube/youtube02.png"
            alt="유튜브썸네일이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/youtube/youtube03.png"
            alt="유튜브썸네일이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/youtube/youtube04.png"
            alt="유튜브썸네일이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/youtube/youtube05.png"
            alt="유튜브썸네일이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/youtube/youtube06.png"
            alt="유튜브썸네일이미지"
          />
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
// port__wrap
.youtube__wrap {
  overflow: hidden;
}
.youtube__inner {
  // overflow: hidden;
  height: 600px;

  .youtube__text {
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

  .youtube__item {
    display: flex;
    position: absolute;

    > div {
      margin-right: 20px;
      width: 400px;

      img {
        width: 100%;
        border-radius: 20px;
      }
    }
  }
}

// youtube__page
.youtube__slider {
  display: none;
}
.youtube__search {
  text-align: center;
  margin-bottom: 50px;

  input {
    border: 1px solid #ebecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
  }
  button {
    @include button(#f7100d, #ffffff);
    @include border(50px);
  }
}
.youtube__tag {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 50px;

    li {
      a {
        border: 1px solid #bfc0c5;
        @include border(10px);
        padding: 10px 20px;
        margin: 0 10px;
      }
    }
  }
}
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.3333%;
      margin-bottom: 4%;

      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
        -webkit-box-orient: vertical;
        word-wrap: break-word;
      }
      img {
        @include border(5px);
        width: 100%;
        max-height: 280px;
      }
    }
  }
}
</style>
