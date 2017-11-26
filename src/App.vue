<template>
  <div id="app">
    <h1>Shopping Cart Example</h1>
    <hr>
    <h2>products</h2>
    <product-list></product-list>
    <hr>
    <cart></cart>
  </div>
</template>

<script>
import ProductList from '@/components/ProductList'
import Cart from '@/components/Cart'

export default {
  name: 'app',
  components: {
    ProductList,
    Cart
  }
}
</script>
