<script setup>
import { ref } from 'vue'

</script>

<template>
  <ul class="productList">
    <li v-for="i in 6" :key="i" class="productList__item">
      <img class="productList__item__img" src="../assets/img/p-1.png" alt="焦糖馬卡龍">
      <div class="productList__item__info">
        <h2 class="productList__item__title">焦糖馬卡龍</h2>
        <p class="productList__item__price">NT$ 450</p>
      </div>
      <button class="productList__item__button" type="button">加入購物車</button>
      <div class="productList__item__feature">
        本日精選
      </div>
      <a class="productList__item__collect" href="#" @click.prevent>
        <img src="../assets/img/favorite_border.png" alt="收藏">
      </a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
  .productList {
    width: 620px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;

    &__item {
      position: relative;
      width: 300px;
      margin-bottom: 20px;

      &__img {
        width: 100%;
        display: block;
      }

      &__info {
        display: flex;
        align-items: center;
        text-align: center;
        font-size: 20px;
        color: #3F5D45;
      }

      &__title, &__price {
        outline: 1px solid #EAF0ED;
        padding: 14px 0;
      }

      &__title {
        width: 173px;
      }

      &__price {
        width: 127px;
        font-weight: bold;
      }

      &__button {
        color: #3F5D45;
        background-color: #EAF0ED;
        border: none;
        outline: 1px solid #EAF0ED;
        width: 100%;
        font-size: 24px;
        font-weight: bold;
        cursor: pointer;
        padding: 16px 0;
      }

      &__feature {
        position: absolute;
        top: 0;
        left: 20px;
        background-color: #3F5D45;
        color: #ffffff;
        writing-mode: vertical-rl;
        text-orientation: upright;
        letter-spacing: 1.5px;
        padding: 10px;
      }

      &__collect {
        position: absolute;
        top: 19px;
        right: 22px;
      }
    }
  }
</style>
