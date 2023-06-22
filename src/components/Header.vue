<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="header container">
    <a href="#">
      <img class="header__logo" src="../assets/img/logo-all-dark.svg" alt="">
    </a>
    <nav class="header__nav">
      <ul class="header__menu">
        <li>
          <a class="header__menu__link" href="#">首頁</a>
        </li>
        <li>
          <a class="header__menu__link" href="#">甜點</a>
        </li>
        <li>
          <a class="header__menu__link" href="#">登入</a>
        </li>
      </ul>
      <a class="header__cart" href="#">
        <img class="header__cart__img" src="../assets/img/shopping_cart.png" alt="購物車">
      </a>
    </nav>
  </div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 0;

  &__logo {
    width: 220px;
    height: 40px;
  }

  &__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 80px;
  }

  &__menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 60px;
    font-weight: bold;

    &__link {
      text-decoration: none;
      color: #3F5D45;
      opacity: 1;
      transition: opacity .3s;

      &:hover {
        opacity: .5;
      }
    }
  }

  &__cart {
    &__img {
      opacity: 1;
      transition: opacity .3s;

      &:hover {
        opacity: .5;
      }
    }
  }
}
</style>
