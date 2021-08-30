<template>
  <ul class="list-group col-8">
    <li class="list-group-item" v-for="(product, $index) in $store.state.productList" :key="$index">
      {{ product.name }} | {{ product.category }} | ${{ product.price }} |
      {{ product.offer ? `${product.discount}%` : '' }} |
      <button
        @click="$store.dispatch('agregarProductoAlCarritoDeCompras', product)"
       class="btn btn-success justify-content-end">
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
