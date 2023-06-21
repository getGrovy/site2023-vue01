<template>
  <section id="memberSection" class="member__wrap gmarket5 section center">
    <h3>멥버 소개</h3>
    <p>웹디자이너, 웹 퍼블리셔, 프론트앤드 개발자 멤버를 소개합니다.</p>

    <div class="member__inner container">
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/memberPic01.jpg" alt="멤버1" />
        </figure>
        <div class="member__body">
          <h4>웹쓰 24기</h4>
          <a href="#" class="btn">포폴보기</a>
        </div>
      </div>
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/memberPic02.jpg" alt="멤버2" />
        </figure>
        <div class="member__body">
          <h4>웹쓰 24기</h4>
          <a href="#" class="btn">포폴보기</a>
        </div>
      </div>
      <div class="member">
        <figure class="member__header">
          <img src="@/assets/images/member/memberPic03.jpg" alt="멤버3" />
        </figure>
        <div class="member__body">
          <h4>웹쓰 24기</h4>
          <a href="#" class="btn">포폴보기</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
// member__wrap
.member__wrap {
}
.member__inner {
  @include flex-between;

  .member {
    width: 32%;
    position: relative;

    .member__header {
      img {
        width: 100%;
      }
    }
    .member__body {
      position: absolute;
      left: 0;
      bottom: 0;
      width: 100%;
      padding: 15px 10px;
      background: #000000b4;
      color: #fff;
      z-index: 100;
      text-align: center;

      h4 {
        font-size: 22px;
      }
      a {
        color: #fff;
        text-decoration: underline;
        text-underline-position: under;
      }
    }
  }
}
</style>
