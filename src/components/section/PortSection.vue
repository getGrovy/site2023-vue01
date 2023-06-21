<template>
  <section id="portSection" :class="attr">
    <h3>포트폴리오 소개</h3>
    <p>웹디자이너, 웹 퍼블리셔, 프론트앤드 포트폴리오입니다</p>
    <div class="port__inner container">
      <div class="port__btn">
        <ul>
          <li class="active"><a href="#">21기</a></li>
          <li><a href="#">22기</a></li>
          <li><a href="#">23기</a></li>
          <li><a href="#">24기</a></li>
        </ul>
      </div>
      <div class="port__cont">
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <img :src="text.img" :alt="text.title" />
          </figure>
          <div class="port__body">
            <div class="pic">
              <img :src="text.icon" :alt="text.title" />
            </div>
            <div class="title">
              <h4>{{ text.title }}</h4>
              <span>{{ text.desc }}</span>
            </div>
          </div>
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
      texts: [
        {
          img: "./images/portfolio/portfolio01.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon01.png",
        },
        {
          img: "./images/portfolio/portfolio02.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon02.png",
        },
        {
          img: "./images/portfolio/portfolio03.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon03.png",
        },
        {
          img: "./images/portfolio/portfolio04.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon04.png",
        },
        {
          img: "./images/portfolio/portfolio05.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon05.png",
        },
        {
          img: "./images/portfolio/portfolio06.jpg",
          title: "김현정 포트폴리오",
          desc: "프론트앤드 개발자 포트폴리오",
          icon: "./images/portfolio/portfolioIcon06.png",
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
    margin-bottom: 30px;

    ul {
      display: flex;
      justify-content: center;

      li {
        a {
          border: 1px solid #44506f;
          color: #44506f;
          display: inline-block;
          padding: 5px 20px;
          margin: 0 5px;
          border-radius: 40px;
        }

        &.active a {
          background-color: #9babd3;
          border-color: #9babd3;
          color: #fff;
        }
      }
    }
  }

  .port__cont {
    @include flex-between;
    flex-wrap: wrap;

    .port {
      width: 32.2222%;
      margin-bottom: 30px;

      .port__body {
        display: flex;
        align-items: center;
        margin-top: 10px;

        .pic {
          margin-right: 10px;
        }
        .title {
          h4 {
            font-size: 20px;
            color: var(--color_body);
          }
          span {
            font-size: 16px;
            color: #2c3a4b;
          }
        }
      }

      img {
        border-radius: 10px;
        width: 100%;
      }

      &:nth-child(4) {
        margin-bottom: 0;
      }
      &:nth-child(5) {
        margin-bottom: 0;
      }
      &:nth-child(6) {
        margin-bottom: 0;
      }
    }
  }
}
</style>
