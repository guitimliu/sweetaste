<script setup>
// import HelloWorld from './components/HelloWorld.zvue'
import Header from './components/Header.vue'
import CategoryList from './components/CategoryList.vue'
import ProductList from './components/ProductList.vue'
import Pagination from './components/Pagination.vue'
import Newsletter from './components/Newsletter.vue'
</script>

<template>
  <div class="products">
    <Header />
    <div class="container">
      <img class="products__banner" src="./assets/img/banner.png" alt="Banner" />
      <div class="products__main">
        <CategoryList />
        <ProductList />
      </div>
      <Pagination />
    </div>
    <Newsletter />
  </div>
</template>

<style lang="scss" scoped>
.products {
  
  &__banner {
    margin-bottom: 60px;
  }

  &__main {
    display: flex;
    justify-content: space-between;
    align-items: start;
  }
}
</style>
