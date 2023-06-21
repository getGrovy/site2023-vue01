<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <swiper
        :modules="modules"
        :autoplay="true"
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide>
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3>New<br />portfolio</h3>
                <p>
                  재능은! 노력 끝에서 발견된다.<br />어떤 일이라도 노력하고
                  즐기면 그 결과는 빛을 바란다고 생각합니다.
                </p>
                <a href="#" class="more button-red">더 알아보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img
                  src="@/assets/images/slider/sliderIcon1.png"
                  alt="이미지1"
                />
                <img
                  src="@/assets/images/slider/sliderIcon2.png"
                  alt="이미지2"
                />
                <img
                  src="@/assets/images/slider/sliderIcon3.png"
                  alt="이미지3"
                />
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
        <swiper-slide>
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3>New<br />portfolio</h3>
                <p>
                  재능은! 노력 끝에서 발견된다.<br />어떤 일이라도 노력하고
                  즐기면 그 결과는 빛을 바란다고 생각합니다.
                </p>
                <a href="#" class="more button-red">더 알아보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img
                  src="@/assets/images/slider/sliderIcon1.png"
                  alt="이미지1"
                />
                <img
                  src="@/assets/images/slider/sliderIcon2.png"
                  alt="이미지2"
                />
                <img
                  src="@/assets/images/slider/sliderIcon3.png"
                  alt="이미지3"
                />
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
        <swiper-slide>
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3>New<br />portfolio</h3>
                <p>
                  재능은! 노력 끝에서 발견된다.<br />어떤 일이라도 노력하고
                  즐기면 그 결과는 빛을 바란다고 생각합니다.
                </p>
                <a href="#" class="more button-red">더 알아보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img
                  src="@/assets/images/slider/sliderIcon1.png"
                  alt="이미지1"
                />
                <img
                  src="@/assets/images/slider/sliderIcon2.png"
                  alt="이미지2"
                />
                <img
                  src="@/assets/images/slider/sliderIcon3.png"
                  alt="이미지3"
                />
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
    </div>
  </section>
</template>
<script>
import { Autoplay } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/autoplay";
export default {
  props: {
    attr: String,
  },
  components: {
    Swiper,
    SwiperSlide,
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
      modules: [Autoplay],
    };
  },
};
</script>
<style lang="scss">
.slider__inner {
  position: relative;
  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 800;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 40px;
        }
        p {
          font-size: 24px;
          line-height: 1.3;
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
        background-image: url(@/assets/images/slider/sliderIBg.png);
        background-size: cover;
        img {
          &:nth-child(1) {
            position: absolute;
            width: 300px;
          }
          &:nth-child(2) {
            position: absolute;
            width: 300px;
            right: 0;
            bottom: 140px;
          }
          &:nth-child(3) {
            position: absolute;
            width: 300px;
            bottom: 0;
            left: 30px;
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
          background-color: var(--button_blue);
          left: 50%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_red);
          top: 20%;
          left: -10%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_green);
          left: 100%;
          top: 10%;
        }
        span:nth-child(4) {
          background-color: var(--button_red);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_blue);
          left: 90%;
          top: 80%;
          width: 30px;
          height: 30px;
        }
      }
    }
  }
  .slider__btn {
    > a {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 22px;
      height: 40px;
      transition: opacity 0.3s;
      &:hover {
        opacity: 0.5;
      }
    }
    .left {
      left: 20px;
      background-image: url(@/assets/images/slider/slider_left.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/images/slider/slider_right.png);
    }
  }
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

반응 댓글 김현빈에 메시지 보내기
