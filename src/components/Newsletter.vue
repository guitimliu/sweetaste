<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="newsletter">
    <div class="newsletter__main">
      <div class="newsletter__desc">
        <img class="newsletter__desc__icon" src="../assets/img/logo-light.svg" alt="Icon">
        <p>訂閱你我的甜蜜郵件</p>
      </div>
      <form action="" class="newsletter__fields">
        <input class="newsletter__fields__input" type="email">
        <button class="newsletter__fields__button" type="submit">
          <img src="../assets/img/arrow_forward-24px.png" alt="訂閱">
        </button>
      </form>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.newsletter {
  background-color: #3F5D45;
  padding: 30px 0;
  
  &__main {
    max-width: 780px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: auto;
  }

  &__desc {
    display: flex;
    align-items: center;
    gap: 20px;
    color: #ffffff;
    font-size: 24px;

    &__icon {
      width: 40px;
      height: 40px;
    }
  }

  &__fields {
    display: flex;

    &__input, &__button {
      border: none;
    }

    &__input {
      width: 316px;
      height: 56px;
    }

    &__button {
      width: 64px;
      height: 58px;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #FFE180;
      color: #3F5D45;
      font-weight: bold;
      cursor: pointer;
      opacity: 1;
      transition: opacity .3s;

      &:hover {
        opacity: .9;
      }
    }
  }
}
</style>
