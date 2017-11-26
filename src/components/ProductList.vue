<template lang="html">
  <ul>
    <li v-for="p in products">
      {{ p.title }} - {{ p.price | currecy }}
      <br />
      <el-button
        :disabled="!p.inventory"
        @click="addToCart(p)">
        Add to cart
      </el-button>
    </li>
  </ul>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
  computed: mapGetters({
    products: 'allProducts'
  }),
  methods: mapActions([
    'addToCart'
  ]),
  created () {
    this.$store.dispatch('getAllProducts')
  }
}
</script>

<style lang="css">
</style>
