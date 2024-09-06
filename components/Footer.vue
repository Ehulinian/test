<template>
  <footer class="footer">
    <div class="container">
      <NuxtLink to="/">
        <img src="../assets/LOGO-footer.svg" alt="Logo" class="footer__logo" />
      </NuxtLink>
      <div class="footer__textWrapper">
        <p class="footer__text">
          About Us <br />Blog <br />
          Support
        </p>
        <p class="footer__text">
          Terms & Conditions <br />
          Privacy Policy <br />
          Cookies
        </p>
      </div>
      <div class="footer__iconWrapper">
        <NuxtLink to="https://www.facebook.com/" class="icon"
          ><img
            src="../assets/facebook-icon.svg"
            alt="Facebook"
            class="icon__facebook"
        /></NuxtLink>
        <NuxtLink to="https://www.instagram.com/" class="icon"
          ><img
            src="../assets/instagram-icon.svg"
            alt="Instagram"
            class="icon__instagram"
        /></NuxtLink>
        <NuxtLink to="https://www.youtube.com/" class="icon"
          ><img
            src="../assets/youtube-icon.svg"
            alt="Youtube"
            class="icon__youtube"
        /></NuxtLink>
        <NuxtLink to="https://ru.pinterest.com/" class="icon"
          ><img
            src="../assets/pinterest-icon.svg"
            alt="Pinterest"
            class="icon__pinterest"
        /></NuxtLink>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  padding-top: 80px;
  background: rgba(66, 60, 78, 1);
  height: 302px;

  &__text {
    font-size: 24px;
    font-weight: 400;
    line-height: 50px;
    text-align: left;
    width: 150px;
    color: rgba(255, 255, 255, 1);
    margin: 0px;
  }

  &__logo {
    padding-top: 10px;
    transition: transform 0.3s ease;
  }

  &__logo:hover {
    transform: scale(1.2);
  }

  &__iconWrapper {
    display: flex;
    gap: 20px;
    padding-top: 10px;
  }

  &__textWrapper {
    display: flex;
    gap: 36px;
    padding-inline: 92px 36px;
  }
}

.icon {
  transition: transform 0.3s ease;
}

.icon:hover {
  transform: scale(1.1);
}

.container {
  display: flex;
  padding-inline: 135px;
}
</style>
