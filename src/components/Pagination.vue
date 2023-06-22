<script setup>
import { ref } from 'vue'

const page = ref(1);
</script>

<template>
  <ul class="pagination">
    <li class="pagination__item">
      <button type="button" class="pagination__item__button">
        <img src="../assets/img/arrow_left.png" alt="上一頁">
      </button>
    </li>
    <li v-for="i in 3" :key="i" class="pagination__item">
      <button type="button" class="pagination__item__button" :class="{active: page === i}">{{ i }}</button>
    </li>
    <li class="pagination__item">
      <button type="button" class="pagination__item__button">
        <img src="../assets/img/arrow_right.png" alt="下一頁">
      </button>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
  .pagination {
    display: flex;
    justify-content: end;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 60px;

    &__item {
      &__button {
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #ffffff;
        color: #3F5D45;
        border: none;
        outline: 1px solid #EAF0ED;
        transition: all .3s;
        cursor: pointer;

        &:hover, &.active {
          background-color: #3F5D45;
          color: #ffffff;
        }
      }
    }
  }
</style>
