<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="unsplash__text">
        <h3>이미지 다운로드 추천</h3>
        <p>
          더 다양한 강의는 유튜브를 통해 제공하고 있습니다. <br />구독과 좋아요!
          부탁드립니다.
        </p>
        <a href="#" class="button-blue">자세히 보기</a>
      </div>
      <div class="unsplash__item">
        <div>
          <img src="@/assets/images/unsplash/unsplash01.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/unsplash/unsplash02.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/unsplash/unsplash03.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/unsplash/unsplash04.jpg" alt="유투브" />
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
};
</script>
<style lang="scss">
// unsplash__section
.unsplash__wrap {
  overflow: hidden;
}
.unsplash__inner {
  height: 560px;

  .unsplash__text {
    h3 {
      font-size: 50px;
      margin-bottom: 40px;
    }
    p {
      font-size: 22px;
      font-weight: 300;
      margin-bottom: 30px;
    }
    a {
      @include border(50px);
    }
  }
  .unsplash__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 400px;
      margin-right: 20px;

      img {
        width: 100%;
        @include border(10px);
      }
    }
  }
}

// unsplash__page
.unsplash__slider {
  display: none;
}
.unsplash__search {
  text-align: center;
  margin-bottom: 50px;

  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
  }
  button {
    @include button(#ffa500, #fff);
    @include border(50px);
  }
}
.unsplash__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 50px;

    li {
      a {
        border: 1px solid #ffa500;
        padding: 10px 20px;
        margin: 0 10px;
        color: #ffa500;
      }
    }
  }
}
.unsplash__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.333%;
      margin-bottom: 4%;

      span {
        display: block;
        margin: 4px 0;
      }
    }
  }
}
</style>
