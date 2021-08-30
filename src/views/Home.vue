<template>
  <div class="home">
    Bienvenido

    <hr />
    <p>Busqueda de producto</p>
    <input type="text" v-model="search" />
    <ul>
      <li v-for="(producto, $index) in $store.state.search" :key="$index">
        <label for="" v-text="producto.name"></label>
      </li>
    </ul>
  </div>
</template>

<script>
//import { mapState, mapGetters } from 'vuex'
export default {
  name: 'Home',
  data() {
    return {
      products: [],
      search: '',

    }
  },
  searchProduct() {
    return this.$store.getters.filteredProductList(this.search)
  }
}
</script>
