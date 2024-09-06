<template>
  <div class="container">
    <section class="callToAction">
      <div class="callToAction__background">
        <h2 class="callToAction__title">Send your data</h2>
        <NuxtLink to="/form-page" class="callToAction__btn">
          <span class="callToAction__btn-text">Go to form</span>
        </NuxtLink>
      </div>
    </section>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.callToAction {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-block: 81px 100px;

  &__background {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-inline: 105px;
    background-image: url(../assets/Subtract.svg);
    background-size: cover;
    width: 100%;
    height: 262px;
  }

  &__title {
    font-size: 50px;
    font-weight: 700;
    line-height: 60.95px;
    text-align: center;
    margin: 0px;
    color: rgba(255, 255, 255, 1);
  }

  &__btn {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    width: 392px;
    height: 58px;
    background: rgba(103, 80, 164, 1);
    border-radius: 100px;
    cursor: pointer;
    border: none;
    transition: background-color 0.3s ease, transform 0.3s ease;

    &-text {
      font-size: 18px;
      font-weight: 500;
      line-height: 28px;
      text-align: center;
      color: rgba(255, 255, 255, 1);
    }
  }

  &__btn:hover {
    background-color: #0056b3;
    transform: scale(1.05);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  }
}

.container {
  padding-inline: 135px;
}
</style>
