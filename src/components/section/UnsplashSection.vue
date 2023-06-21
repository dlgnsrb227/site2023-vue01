<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>추천 unsplash 이미지</h3>
        <p>
          unsplash에서 다양한 이미지를 다운로드 받으세요.
          <br />
          추천 이미지를 구경하고 가세요.
        </p>
        <router-link to="#" class="button-blue"> 자세히보기 </router-link>
      </div>
      <div class="unsplash__item">
        <div>
          <img
            src="@/assets/img/unsplash/unsplash01.png"
            alt="언스플래쉬이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/unsplash/unsplash02.png"
            alt="언스플래쉬이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/unsplash/unsplash03.png"
            alt="언스플래쉬이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/unsplash/unsplash04.png"
            alt="언스플래쉬이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/unsplash/unsplash05.png"
            alt="언스플래쉬이미지"
          />
        </div>
        <div>
          <img
            src="@/assets/img/unsplash/unsplash06.png"
            alt="언스플래쉬이미지"
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
// unsplash__wrap
.unsplash__wrap {
  overflow: hidden;
}
.unsplash__inner {
  // overflow: hidden;
  height: 600px;

  .unsplash__text {
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
  .unsplash__item {
    width: 200%;
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

// unsplash__cont
.unsplash__cont {
  ul {
    column-count: 4;

    li {
      margin-bottom: 20px;
    }
  }
}
// unsplash__search
.unsplash__search {
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
