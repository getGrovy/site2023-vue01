<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>frontend</span>
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
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      title: "프론트앤드<br />전문과정",
      desc: "프론트앤드 개발자로 취업하기 위한<br />전문 과정입니다.<br />여러분들도 도전해보세요!",
      texts: [
        {
          title: "React.js",
          desc: "리액트는 Facebook에서 개발한 오픈 소스 자바스크립트 라이브러리입니다. 리액트를 사용하면 컴포넌트 기반의 UI 개발을 간편하게 할 수 있습니다. 리액트의 주요 특징은 가상 DOM(Virtual DOM)을 사용하여 성능을 최적화하고, 컴포넌트의 재사용성을 높이는 것입니다",
        },
        {
          title: "Vue.js",
          desc: "뷰는 Evan You에 의해 개발된 오픈 소스 자바스크립트 프론트엔드 프레임워크입니다. 리액트와 마찬가지로 컴포넌트 기반의 UI 개발을 지원하며, 가상 DOM을 사용하여 성능을 향상시킵니다",
        },
        {
          title: "Next.js",
          desc: "넥스트.js는 리액트 기반의 서버 사이드 렌더링(SSR) 및 정적 사이트 생성(Static Site Generation)을 지원하는 프레임워크입니다. 넥스트.js를 사용하면 서버 측에서 초기 렌더링을 수행하여 초기 로딩 속도를 개선하고, 검색 엔진 최적화(SEO)를 향상시킬 수 있습니다",
        },
        {
          title: "Webstandard",
          desc: "웹 표준 코딩은 웹 개발에서 일관된 기술 표준을 준수하여 웹 페이지를 개발하는 것을 말합니다. 이는 웹 페이지의 구조, 디자인 및 기능을 구현하는 데 사용되는 HTML, CSS, JavaScript 등의 웹 기술에 적용됩니다",
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
    }
    p {
      font-weight: 300;
      line-height: 1.6;
    }
    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
