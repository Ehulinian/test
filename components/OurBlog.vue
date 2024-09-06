<template>
  <section class="ourBlog">
    <div class="container">
      <div class="ourBlog__intro">
        <h2 class="ourBlog__title">Our blog posts</h2>
        <div class="ourBlog__stroke"></div>
      </div>

      <div class="ourBlog__wrapper">
        <div class="ourBlog__backgroundPhoto ourBlog__backgroundPhoto--big">
          <h4 class="ourBlog__title--big">
            Return to running after pregnancy – Is your body strong enough for
            running?
          </h4>
          <div class="ourBlog__informationWrapper">
            <img
              src="../assets/image 9.png"
              alt="Tilda"
              class="ourBlog__icon"
            />
            <div class="ourBlog__aboutPerson">
              <p class="ourBlog__name">BY TILDA LOFTIN</p>
              <p class="ourBlog__date1">JUNE 25, 2021</p>
            </div>
          </div>
        </div>
        <div class="ourBlog__smallPhotos">
          <div
            class="ourBlog__backgroundPhoto ourBlog__backgroundPhoto--small1 photo"
          >
            <h5 class="ourBlog__title--small">Stroller walks</h5>
            <p class="ourBlog__date">APRIL 21, 2021</p>
          </div>
          <div
            class="ourBlog__backgroundPhoto ourBlog__backgroundPhoto--small2 photo"
          >
            <h5 class="ourBlog__title--small">Playground workout</h5>
            <p class="ourBlog__date">MARCH 17, 2020</p>
          </div>
          <div
            class="ourBlog__backgroundPhoto ourBlog__backgroundPhoto--small3 photo"
          >
            <h5 class="ourBlog__title--small">
              Your Essential Fitness Gear for Each Trimester
            </h5>
            <p class="ourBlog__date">FEBRUARY 21, 2021</p>
          </div>
          <div
            class="ourBlog__backgroundPhoto ourBlog__backgroundPhoto--small4 photo"
          >
            <h5 class="ourBlog__title--small">
              What YOU could gain by working with a Woman’s Health Physical
              Therapist
            </h5>
            <p class="ourBlog__date">JANUARY 23, 2020</p>
          </div>
        </div>
      </div>
      <div class="ourBlog__follow">
        <p class="ourBlog__view">Like what you see? View more</p>
        <div class="ourBlog__iconArrow">
          <img
            src="../assets/arrow-right.svg"
            alt="Arrow right"
            class="icon__image"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.ourBlog {
  &__title {
    font-size: 50px;
    font-weight: 700;
    line-height: 60.95px;
    margin: 0px;
    padding-top: 160px;
    text-align: center;

    &--big {
      font-size: 32px;
      font-weight: 700;
      line-height: 39.01px;
      text-align: left;
      color: rgba(255, 255, 255, 1);
      margin: 0px;
      padding-inline: 32px 28px;
    }

    &--small {
      font-size: 24px;
      font-weight: 700;
      line-height: 29.26px;
      text-align: left;
      padding: 0px 0px 6px 16px;
      margin: 0px;
      color: rgba(255, 255, 255, 1);
    }
  }

  &__follow {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 32px;
    gap: 9px;
  }

  &__icon {
    display: block;
    padding-inline: 32px 8px;
    width: 30px;
    height: 30px;
    transition: transform 0.3s ease;
  }

  &__icon:hover {
    transform: scale(1.1);
  }

  &__iconArrow {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 32px;
    height: 32px;
    background: rgba(103, 80, 164, 1);
    border-radius: 50%;
    transition: transform 0.3s ease;
    cursor: pointer;
  }

  &__iconArrow:hover {
    transform: scale(1.2);
  }

  &__aboutPerson {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 35px;
  }

  &__date1 {
    font-size: 16px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
    margin: 0px;
    color: rgba(255, 255, 255, 1);
  }

  &__name,
  &__date {
    font-size: 16px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
    margin: 0px;
    color: rgba(255, 255, 255, 1);
  }

  &__view {
    font-size: 24px;
    font-weight: 400;
    line-height: 38.4px;
    margin: 0px;
    text-align: center;
  }

  &__date {
    padding: 0px 0px 16px 16px;
  }

  &__informationWrapper {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    padding-block: 12px 34px;
    width: 100%;
  }

  &__intro {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }

  &__wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 32px;
  }

  &__smallPhotos {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, auto);
    gap: 32px;
  }

  &__backgroundPhoto {
    transition: transform 0.3s ease;
    cursor: pointer;
    &--big {
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: center;
      background-image: url(../assets/img_1.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 604px;
      height: 604px;
    }

    &--small1 {
      background-image: url(../assets/img_2.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 286px;
      height: 286px;
    }

    &--small2 {
      background-image: url(../assets/img_3.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 286px;
      height: 286px;
    }

    &--small3 {
      background-image: url(../assets/img_4.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 286px;
      height: 286px;
    }

    &--small4 {
      background-image: url(../assets/img_5.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 286px;
      height: 286px;
    }
  }

  &__backgroundPhoto:hover {
    transform: scale(1.05);
  }

  &__stroke {
    box-sizing: border-box;
    border: 3px solid rgba(255, 45, 85, 1);
    width: 46px;
    margin-block: 21px 60px;
  }
}

.photo {
  display: flex;
  justify-content: flex-end;
  flex-direction: column;
  align-items: flex-start;
}

.icon__image {
  display: block;
  width: 20.21px;
  height: 20.21px;
  cursor: pointer;
}

.container {
  padding-inline: 135px;
  display: flex;
  align-items: center;
  flex-direction: column;
}
</style>
