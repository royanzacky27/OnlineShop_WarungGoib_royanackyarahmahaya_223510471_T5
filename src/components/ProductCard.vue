<template>
    <div class="card">
      <img class="card-img-top" :src="product.image" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title">{{ product.name }}</h5>
        <p class="card-text">{{ product.description }}</p>
        <a href="#" class="btn btn-primary">Buy Now</a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ProductCard',
    props: {
      product: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  /* styling for card */
  </style>
  