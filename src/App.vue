<template>
  <div id="app" class="ml-3 mt-2">
    <Navbar />
     <router-view />
<!--     <div id="nav"> -->
<!--       <router-link to="/">Inicio</router-link>
      |
      <router-link to="/products">Productos</router-link>
      |
      <router-link to="/newproduct">Nuevo Producto</router-link>
      |
      <router-link to="/carrito">Carrito</router-link>
    </div>
    <br />
   

    <hr /> -->
<!--     <ShoppingCart /> -->


  </div>
</template>

<script>
//import ShoppingCart from './components/ShoppingCart.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: { 
    //ShoppingCart,
    Navbar
  }
}
</script>
