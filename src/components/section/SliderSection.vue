<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <h2 class="blind">배너 슬라이드</h2>
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="50"
        :autoplay="{
          delay: 5000,
          disableOnInteraction: false,
        }"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button-green">자세히보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.image1" :alt="slider.title" />
                <img :src="slider.image2" :alt="slider.title" />
                <img :src="slider.image3" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
      <div class="slider__btn">
        <a href="#" class="left"><span class="ir">이전이미지</span></a>
        <a href="#" class="right"><span class="ir">다음이미지</span></a>
      </div>
      <div class="slider__dot">
        <a href="#" class="dot"><span class="ir">1번 이미지</span></a>
        <a href="#" class="dot"><span class="ir">2번 이미지</span></a>
        <a href="#" class="dot active"><span class="ir">3번 이미지</span></a>
      </div>
    </div>
  </section>
</template>

<script>
// import Swiper core and required modules
import {
  Navigation,
  Pagination,
  Scrollbar,
  EffectFade,
  Autoplay,
  Parallax,
} from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

export default {
  props: { attr: String },
  components: {
    Swiper,
    SwiperSlide,
  },

  data: function () {
    return {
      sliders: [
        {
          title: "New<br />portfolio1",
          desc: "재능은 노력끝에서 발견된다.<br />어떤 일이라도 노력하고 즐기면 그 결과는 빛을 바란다고 생각합니다.",
          image1: "./img/slider/slidericon04.png",
          image2: "./img/slider/slidericon08.png",
          image3: "./img/slider/slidericon10.png",
        },
        {
          title: "New<br />portfolio2",
          desc: "재능은 노력끝에서 발견된다.<br />어떤 일이라도 노력하고 즐기면 그 결과는 빛을 바란다고 생각합니다.",
          image1: "./img/slider/slidericon03.png",
          image2: "./img/slider/slidericon07.png",
          image3: "./img/slider/slidericon09.png",
        },
        {
          title: "New<br />portfolio3",
          desc: "재능은 노력끝에서 발견된다.<br />어떤 일이라도 노력하고 즐기면 그 결과는 빛을 바란다고 생각합니다.",
          image1: "./img/slider/slidericon01.png",
          image2: "./img/slider/slidericon02.png",
          image3: "./img/slider/slidericon05.png",
        },
      ],
    };
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [
        Navigation,
        Pagination,
        Scrollbar,
        EffectFade,
        Autoplay,
        Parallax,
      ],
    };
  },
};
</script>

<style lang="scss">
.swiper {
  overflow: visible;
}
.swiper-pagination {
  bottom: -80px !important;
}
// slider__wrap
.slider__wrap {
  background-color: #eee;
  overflow: hidden;
}

// slider__inner
.slider__inner {
  position: relative;

  // slider__img
  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 900;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 40px;
        }
        p {
          font-size: 22px;
          line-height: 1.2;
          margin-bottom: 50px;
        }
        .more {
          font-size: 18px;
        }
      }
      .img {
        position: absolute;
        right: 0;
        top: -120px;
        width: 600px;
        height: 600px;
        background-image: url(@/assets/img/slider/slidergradient.png);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center center;

        img {
          &:nth-child(1) {
            width: 300px;
            height: 300px;
            position: absolute;
            bottom: 20px;
            left: 70px;
          }
          &:nth-child(2) {
            width: 300px;
            height: 300px;
            position: absolute;
            right: 30px;
            top: 30px;
          }
          &:nth-child(3) {
            width: 300px;
            height: 300px;
            position: absolute;
            left: -10px;
            top: -30px;
          }
        }
      }
      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }

        span:nth-child(1) {
          background-color: var(--button_red);
          left: 55%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_green);
          top: 20%;
          left: -10%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_green);
          left: 90%;
        }
        span:nth-child(4) {
          background-color: var(--button_green);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_blue);
          top: 80%;
          width: 30px;
          height: 30px;
        }
      }
    }
  }
  // slider__btn
  .slider__btn {
    > a {
      position: absolute;
      top: 50%;
      width: 23px;
      height: 40px;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
      transition: all 0.1s;

      &:hover {
        opacity: 0.7;
      }
    }

    .left {
      left: 20px;
      background-image: url(@/assets/img/slider/sliderleft.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/img/slider/sliderright.png);
    }
  }
  // slider__dot
  .slider__dot {
    position: absolute;
    left: 50%;
    bottom: -80px;
    transform: translateX(-50%);

    a {
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      margin: 0 5px;
      border: 4px solid #ff3344;
      background-color: #ff3344;
      box-shadow: 0 0 0 3px transparent;

      &.active {
        box-shadow: 0 0 0 3px #ff3344;
        border-width: 4px;
        background-color: #fff;
      }
    }
  }
}
</style>
