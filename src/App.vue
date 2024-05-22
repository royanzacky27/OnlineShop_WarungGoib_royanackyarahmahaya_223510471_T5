<template>
  <div id="app">
    <MainNavbar />
    <ImageCarousel />
    <div class="container mt-4">
      <div class="row">
        <div class="col-md-4" v-for="product in products" :key="product.id">
          <ProductCard :product="product" />
        </div>
      </div>
    </div>
    <AppFooter />
  </div>
</template>

<script>
import MainNavbar from './components/MainNavbar.vue';
import ImageCarousel from './components/ImageCarousel.vue';
import ProductCard from './components/ProductCard.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    MainNavbar,
    ImageCarousel,
    ProductCard,
    AppFooter
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Product 1', description: 'Description for product 1', image: 'https://image.uniqlo.com/UQ/ST3/id/imagesgoods/466732/item/idgoods_09_466732.jpg?width=750' },
        { id: 2, name: 'Product 2', description: 'Description for product 2', image: 'https://image.uniqlo.com/UQ/ST3/AsianCommon/imagesgoods/459621/item/goods_09_459621.jpg?width=750' },
        { id: 3, name: 'Product 3', description: 'Description for product 3', image: 'https://image.uniqlo.com/UQ/ST3/id/imagesgoods/467247/item/idgoods_09_467247.jpg?width=750' }
      ]
    };
  }
};
</script>

<style>
@import 'bootstrap/dist/css/bootstrap.css';
@import 'bootstrap-vue-next/dist/bootstrap-vue-next.css';
</style>
