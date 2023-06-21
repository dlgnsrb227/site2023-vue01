<template>
  <section id="portSection" :class="attr">
    <h3>포트폴리오 소개</h3>
    <p>웹디자이너, 웹퍼블리셔, 프론트앤드 개발자를 희망합니다.</p>
    <div class="port__inner container">
      <div class="port__btn">
        <a href="/" class="active"> 21기 </a>
        <a href="/">22기</a>
        <a href="/">23기</a>
        <a href="/">24기</a>
      </div>
      <div class="port__cont">
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <img :src="text.img" alt="프로필이미지" />
          </figure>
          <div class="port__body">
            <span>
              <img :src="text.icon" alt="포폴프로필" />
              <div>
                <h4>{{ text.title }}</h4>
                <p>{{ text.desc }}</p>
              </div>
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: { attr: String },
  data: function () {
    return {
      texts: [
        {
          img: "./img/port/port01.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile01.png",
        },
        {
          img: "./img/port/port02.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile02.png",
        },
        {
          img: "./img/port/port03.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile03.png",
        },
        {
          img: "./img/port/port04.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile04.png",
        },
        {
          img: "./img/port/port05.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile05.png",
        },
        {
          img: "./img/port/port06.png",
          title: "이훈규 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./img/port/portprofile06.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
// port__wrap
.port__inner {
  .port__btn {
    width: 50%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    margin-bottom: 30px;

    > a {
      font-size: 20px;
      display: inline-block;
      padding: 7px 50px;
      border: 1px solid #d9e4ff;
      background-color: #eaf0ff;
      color: #666;
      border-radius: 50px;

      &.active {
        background-color: #d9e4ff;
        border: 1px solid #a2bcff;
        color: #232323;
      }
    }
  }
  .port__cont {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    .port {
      width: 32%;
      margin-bottom: 30px;

      figure > img {
        width: 100%;
        border-radius: 10px;
      }
      .port__body {
        span {
          display: flex;
          text-align-last: left;
          padding: 15px 0;

          > img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 15px;
          }
          > div > h4 {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 5px;
          }
          > div > p {
            color: #666;
            font-weight: 600;
          }
        }
      }
    }
  }
}
</style>
