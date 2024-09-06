<template>
  <div class="container">
    <section class="banner">
      <img src="../assets/bg.svg" alt="Waves" class="banner__background" />
      <div class="banner__wrapper">
        <h1 class="banner__title">Strong for life with us</h1>

        <div class="banner__stroke"></div>

        <p class="banner__text">
          The best Pre/postnatal fitness app! 100 exercises divided in before,
          during and after pregnancy. Stay strong and healthy through all stages
          of pregnancy.
        </p>

        <div class="banner__buttons">
          <div class="banner__btn">
            <img src="../assets/Mobile app store badge.svg" alt="AppleStore" />
            <a
              href="https://apps.apple.com/ua/app/apple-store/id375380948?l=ru"
            ></a>
          </div>
          <div class="banner__btn">
            <img
              src="../assets/Mobile app store badge (1).svg"
              alt="GooglePlay"
            />
            <a href="https://play.google.com/store/games?hl=ru&pli=1"></a>
          </div>
        </div>
      </div>
      <img src="../assets/Img.svg" alt="Iphone" class="banner__phone" />
    </section>
  </div>
</template>

<style lang="scss" scoped>
.banner {
  position: relative;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: flex-start;
  box-sizing: border-box;

  &__background {
    position: absolute;
    top: 0;
    left: 0;
    object-fit: cover;
    z-index: -1;
  }

  &__buttons {
    display: flex;
    gap: 40px;
  }

  &__wrapper {
    padding-top: 107px;
    padding-left: 102px;
    width: 501px;
  }

  &__title,
  &__text {
    color: rgba(35, 21, 62, 1);
    margin: 0px;
    text-align: left;
  }

  &__btn {
    transition: transform 0.3s ease;
    cursor: pointer;
  }

  &__btn:hover {
    transform: scale(1.1);
  }

  &__stroke {
    box-sizing: border-box;
    border: 3px solid rgba(255, 45, 85, 1);
    width: 46px;
    margin-block: 21px 37px;
  }

  &__title {
    font-size: 56px;
    font-weight: 700;
    line-height: 68.26px;
  }

  &__phone {
    transition: transform 0.3s ease;

    position: relative;
    object-fit: cover;
  }

  &__phone:hover {
    transform: scale(1.02);
  }

  &__text {
    font-size: 24px;
    font-weight: 400;
    line-height: 38.4px;
    padding-bottom: 37px;
  }
}

.container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-inline: auto;
  padding-top: 60px;
}
</style>
