<template>
  <section id="profileSection" class="profile__wrap section center">
    <h3>프로필 소개</h3>
    <p>웹디자이너, 웹퍼블리셔, 프론트앤드 개발자를 희망합니다.</p>
    <div class="profile__inner container">
      <div class="profile">
        <figure class="profile__header">
          <img src="@/assets/img/porfile/profile01.svg" alt="프로필이미지" />
        </figure>
        <div class="profile__body">
          <h4 class="title">이훈규</h4>
          <a href="/" class="btn"> 포트폴리오 보기 </a>
        </div>
      </div>
      <div class="profile">
        <figure class="profile__header">
          <img src="@/assets/img/porfile/profile02.svg" alt="프로필이미지" />
        </figure>
        <div class="profile__body">
          <h4 class="title">이훈규</h4>
          <a href="/" class="btn"> 포트폴리오 보기 </a>
        </div>
      </div>
      <div class="profile">
        <figure class="profile__header">
          <img src="@/assets/img/porfile/profile03.svg" alt="프로필이미지" />
        </figure>
        <div class="profile__body">
          <h4 class="title">이훈규</h4>
          <a href="/" class="btn"> 포트폴리오 보기 </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
// profile__wrap
.profile__wrap {
}
.profile__inner {
  @include flex-between;

  .profile {
    width: 32%;
    border: 2px solid var(--color_body);

    .profile__header {
      padding: 20px;
      margin-top: -20px;

      img {
        width: 100%;
      }
    }
    .profile__body {
      padding: 15px 10px;
      margin-top: -90px;
      background-color: #000;
      color: #fff;
      z-index: 100;
      position: relative;

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
