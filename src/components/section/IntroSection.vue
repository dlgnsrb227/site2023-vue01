<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">프론트엔드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>Frontend</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>
            {{ text.desc }}
          </p>
        </div>
        <!-- <div>
          <h4 class="icon-react">React.js</h4>
          <p>
            React는 사용자 인터페이스(UI)를 구축하기 위한 JavaScript
            라이브러리입니다. React는 웹 애플리케이션 개발에 주로 사용되며,
            모바일 앱과도 통합할 수 있습니다.
          </p>
        </div> -->
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: { attr: String },
  data: function () {
    return {
      title: "프론트앤드<br />전문과정",
      desc: "프론트앤드 개발자로 취업하기 위한<br />전문과정입니다.<br />여러분들도 도전해보세요!",
      texts: [
        {
          title: "React.js",
          desc: "React는 사용자 인터페이스(UI)를 구축하기 위한 JavaScript 라이브러리입니다. React는 웹 애플리케이션 개발에 주로 사용되며, 모바일 앱과도 통합할 수 있습니다.",
        },
        {
          title: "Vue.js",
          desc: "Vue는 사용자 인터페이스(UI)를 구축하기 위한 프로그레시브 자바스크립트 프레임워크입니다. React와 마찬가지로 웹 애플리케이션 개발에 주로 사용됩니다.",
        },
        {
          title: "Vite.js",
          desc: "Vite.js는 개발 서버와 빌드 도구를 포함하고 있어 개발 환경에서 매우 빠른 번들링 및 핫 리로딩 기능을 제공합니다. 이는 애플리케이션을 빠르게 개발하고 효율적으로 변경사항을 적용할 수 있게 해줍니다.",
        },
        {
          title: "Next.js",
          desc: "Next.js는 React 기반의 서버 사이드 렌더링 프레임워크입니다. 웹애플리케이션을 개발할 때 필요한 기본 구성 요소와 라우팅, 데이터 통합 등을 제공하여 개발자들이 보다 쉽고 빠르게 웹 애플리케이션을 구축할 수 있게 도와줍니다.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
// intro__wrap
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;

  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
      display: inline-block;
    }
    &:nth-child(3),
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
