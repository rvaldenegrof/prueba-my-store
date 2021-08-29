<template>
  <ul>
    <li v-for="(product, $index) in $store.state.productList" :key="$index" class="listado">
      {{ product.name }} | {{ product.category }} | ${{ product.price }} |
      {{ product.offer ? `${product.discount}%` : '' }} |
      <button
        @click="$store.dispatch('agregarProductoAlCarritoDeCompras', product)"
       class="boton ml-3">
        Agregar al carrito
      </button>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Products'
}
</script>

<style scoped>

</style>
