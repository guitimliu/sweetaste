<script setup>
import { ref } from 'vue'

const currentCategory = ref('所有甜點');
</script>

<template>
  <ul class="categoryList">
    <li class="categoryList__item">甜點類別</li>
    <li class="categoryList__item">
      <a class="categoryList__item__link" :class="{'active': currentCategory === '所有甜點'}" href="#">所有甜點（48）</a>
    </li>
    <li class="categoryList__item">
      <a class="categoryList__item__link" href="#">本日精選（10）</a>
    </li>
    <li class="categoryList__item">
      <a class="categoryList__item__link" href="#">人氣推薦（26）</a>
    </li>
    <li class="categoryList__item">
      <a class="categoryList__item__link" href="#">新品上市（12）</a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
.categoryList {
  width: 300px;

  &__item {
    font-size: 24px;
    line-height: 40px;
    text-align: center;
    transition: background-color .3s;
    outline: 1px solid #EAF0ED;

    &__link {
      display: block;
      text-decoration: none;
      color: #3F5D45;
    }

    &:nth-child(1) {
      background-color: #3F5D45;
      color: #ffffff;
    }

    &__link, &:nth-child(1) {
      padding: 16px 0;
    }

    &:not(:nth-child(1)):hover, .active {
      background-color: #EAF0ED;
    }
  }
}
</style>
