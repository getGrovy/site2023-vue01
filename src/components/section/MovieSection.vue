<template>
  <section id="movieSection" :class="attr">
    <div class="movie__inner container">
      <div class="movie__text">
        <h3>코딩 영화 추천</h3>
        <p>
          더 다양한 강의는 유튜브를 통해 제공하고 있습니다. <br />구독과 좋아요!
          부탁드립니다.
        </p>
        <a href="#" class="button-green">자세히 보기</a>
      </div>
      <div class="movie__item">
        <div>
          <img src="@/assets/images/movie/movie01.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/movie/movie02.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/movie/movie03.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/movie/movie04.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/movie/movie05.jpg" alt="유투브" />
        </div>
        <div>
          <img src="@/assets/images/movie/movie06.jpg" alt="유투브" />
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
// movie__section
.movie__wrap {
  overflow: hidden;
}
.movie__inner {
  height: 780px;

  .movie__text {
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
  .movie__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;

    > div {
      width: 300px;
      margin-right: 20px;

      img {
        width: 100%;
        @include border(10px);
      }
    }
  }
}

// movie__page
.movie__slider {
  display: none;
}
.movie__search {
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
    @include button(#4857ec, #fff);
    @include border(50px);
  }
}
.movie__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 50px;

    li {
      a {
        border: 1px solid #4857ec;
        padding: 10px 20px;
        margin: 0 10px;
        color: #4857ec;
      }
    }
  }
}
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 19%;
      margin-bottom: 4%;

      img {
        border-radius: 10px;
      }
      span {
        display: block;
        margin: 4px 0;
      }
    }
  }
}
</style>
