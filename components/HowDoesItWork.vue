<template>
  <section class="howDoesItWork">
    <div class="container">
      <h2 class="howDoesItWork__title">How Does It Work?</h2>
      <p class="howDoesItWork__describe">
        Easy, fun & essential training for moms
      </p>
      <div class="howDoesItWork__stroke"></div>
      <div class="howDoesItWork__wrapper">
        <div class="howDoesItWork__exercises">
          <div class="howDoesItWork__icon">
            <img
              src="../assets/ic_search.svg"
              alt="Search"
              class="icon__image"
            />
          </div>
          <div class="howDoesItWork__textWrapper">
            <p class="howDoesItWork__text">Browse exercises</p>
            <p class="howDoesItWork__description">
              Browse over 100 exercises with a video or picture and a
              description.
            </p>
          </div>
        </div>
        <div class="howDoesItWork__timeline">
          <div class="howDoesItWork__icon">
            <img
              src="../assets/ic_timeline.svg"
              alt="Timeline"
              class="icon__image"
            />
          </div>
          <div class="howDoesItWork__textWrapper">
            <p class="howDoesItWork__text">Create timeline</p>
            <p class="howDoesItWork__description">
              Take pictures along the way during and after the pregnancy to see
              the transformation.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.howDoesItWork {
  padding-bottom: 160px;

  &__title {
    font-size: 50px;
    font-weight: 700;
    line-height: 60.95px;
    text-align: center;
    margin: 0px;
    color: rgba(35, 21, 62, 1);
  }

  &__describe {
    font-size: 32px;
    font-weight: 500;
    line-height: 39.01px;
    text-align: center;
    padding-block: 24px 21px;
    margin: 0px;
  }

  &__stroke {
    box-sizing: border-box;
    border: 3px solid rgba(255, 45, 85, 1);
    width: 46px;
    margin-bottom: 60px;
  }

  &__wrapper {
    display: flex;
    gap: 40px;
  }

  &__exercises {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    gap: 42px;
  }

  &__timeline {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    gap: 42px;
  }

  &__icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 56px;
    height: 56px;
    box-shadow: 0px 4px 15px 0px rgba(0, 0, 0, 0.15);
    border-radius: 50px;
    transition: transform 0.3s ease;
  }

  &__icon:hover {
    transform: scale(1.2);
  }

  &__textWrapper {
    display: flex;
    flex-direction: column;
    gap: 5px;
  }

  &__text {
    font-size: 32px;
    font-weight: 500;
    line-height: 39.01px;
    text-align: left;
    margin: 0px;
  }

  &__description {
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
    margin: 0px;
  }
}

.container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding-inline: 135px;
}
</style>
