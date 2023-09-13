<template>
  <header class="header">
    <NuxtLink class="header__logo" to="/">
      <img alt="logo" src="/images/logo.svg">
    </NuxtLink>
    <div class="header__content">
      <div><img alt="burger" src="/images/logo_main.svg"></div>
      <div class="header__description">
        <div class="header__text">
          <span style="color: var(--white)">Только самые</span>
          <br>
          <span style="color: var(--orange)">сочные бургеры!</span>
        </div>
        <div class="header__delivery">Бесплатная доставка от 599₽</div>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
@import "assets/styles/devices";

.header {
  height: 400px;
  background-color: var(--yello);
  box-sizing: border-box;
  border-radius: 0 0;
  @media (max-width: $mobile) {
    height: fit-content;
  }

  &__logo {
    margin: 0 auto;
    padding: 16px 0;
    width: fit-content;
    display: block;
  }

  &__content {
    display: flex;
    align-items: center;
    gap: 24px;
    margin: 0 auto;
    width: fit-content;
    @media (max-width: $mobile) {
      flex-direction: column-reverse;
    }
  }

  &__description {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 70px;
    @media (max-width: $mobile) {
      gap: 10px;
    }
  }

  &__text {
    font-weight: 800;
    font-size: 50px;
    @media (max-width: $mobile) {
      font-size: 30px;
      text-align: center;
    }
  }

  &__delivery {
    color: var(--white);
    font-weight: 600;
    font-size: 16px;
    @media (max-width: $mobile) {
      text-align: center;
    }
  }
}

</style>
