<template>
  <section class="whatToDo">
    <div class="container">
      <div class="whatToDo__titleWrapper">
        <h2 class="whatToDo__title">Before, during and after pregnancy</h2>
        <p class="whatToDo__describe">
          The app is divided into three different stages to help you choose
          appropriate exercises. Each exercise is carefully selected to ensure
          safe and appropriate adjustments to follow the pregnancy’s progress.
        </p>
        <div class="whatToDo__stroke"></div>
      </div>

      <div class="whatToDo__before">
        <div class="whatToDo__before-wrapper">
          <h3 class="whatToDo__subtitle">Before pregnancy</h3>
          <div class="whatToDo__stroke"></div>
          <p class="whatToDo__text">
            Start preparing for pregnancy with safe exercises that build up a
            strong body.
          </p>
          <p class="whatToDo__subtitleSecond">Trimesters</p>
          <p class="whatToDo__text">
            The pregnancy is divided into first trimester, second trimester part
            1 and 2, and third trimester part 1 and 2 to provide exercises that
            are safe for each stage of the pregnancy. Each exercise comes with a
            video and a description so you can safely perform each exercise.
            Simple put in your due date and you will be taken to the proper
            stage.
          </p>
        </div>
        <img
          src="../assets/before_img.png"
          alt="Before Pregnance"
          class="whatToDo__before-photo"
        />
      </div>
      <div class="whatToDo__during">
        <img
          src="../assets/img_during.png"
          alt="During Pregnance"
          class="whatToDo__during-photo"
        />
        <div class="whatToDo__during-wrapper">
          <h3 class="whatToDo__subtitle">During pregnancy</h3>
          <div class="whatToDo__stroke"></div>
          <p class="whatToDo__text">
            Working out during pregnancy has many benefits for both the mom and
            the baby. It can reduce back pain, help prevent gestational
            diabetes, promote good posture, strength and endurance, and also
            improve the ability to cope with labor.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.whatToDo {
  &__titleWrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 24px;
  }

  &__stroke {
    box-sizing: border-box;
    border: 3px solid rgba(255, 45, 85, 1);
    width: 46px;
    margin-block: 13px 24px;
  }

  &__title {
    font-size: 50px;
    font-weight: 700;
    line-height: 60.95px;
    text-align: center;
  }

  &__describe {
    font-size: 32px;
    font-weight: 500;
    line-height: 39.01px;
    text-align: center;
  }

  &__before {
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 36px;
    padding-bottom: 68px;
    gap: 90px;

    &-photo {
      transition: transform 0.3s ease;
      width: 546px;
      height: 683px;
    }

    &-photo:hover {
      transform: scale(1.04);
    }

    &-wrapper {
      display: flex;
      flex-direction: column;
    }
  }

  &__during {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 90px;
  }

  &__subtitle {
    font-size: 40px;
    font-weight: 700;
    line-height: 48.76px;
    text-align: left;
  }

  &__text {
    font-size: 18px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
  }

  &__subtitleSecond {
    font-size: 32px;
    font-weight: 500;
    line-height: 39.01px;
    text-align: left;
    padding-block: 16px 5px;
  }

  &__subtitle,
  &__subtitleSecond,
  &__text,
  &__title,
  &__describe {
    margin: 0px;
  }

  &__during {
    &-photo {
      transition: transform 0.3s ease;
      width: 546px;
      height: 652px;
    }

    &-photo:hover {
      transform: scale(1.04);
    }
  }

  .container {
    padding-inline: 135px;
  }
}
</style>
