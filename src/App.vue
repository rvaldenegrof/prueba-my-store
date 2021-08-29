<template>
  <div id="app" class="ml-3 mt-2">
    <div id="nav">
      <router-link to="/products">Productos</router-link>
      |
      <router-link to="/newproduct">Nuevo Producto</router-link>
    </div>
    <br />
    <router-view />

    <hr />
    <ShoppingCart />
  </div>
</template>

<script>
import ShoppingCart from './components/ShoppingCart.vue'

export default {
  name: 'App',
  components: { ShoppingCart }
}
</script>
