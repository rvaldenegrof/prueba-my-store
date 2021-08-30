<template>
  <div class="home">
    Bienvenido
    <hr />
    <form class="form-inline">
      <div class="form-group">
        <label for="busqueda">Busqueda de producto</label>
        <input
          type="text"
          class="form-control ml-2"
          id="busqueda"
          placeholder="Busquedor que no funciona"
          v-model="search"
        />
      </div>
      <button type="submit" class="btn btn-primary ml-2">Buscar</button>
    </form>
    <ul>
      <li v-for="(producto, $index) in products" :key="$index">
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
      search: ''
    }
  },
  searchProduct() {
    return this.$store.getters.filteredProductList(this.search)
  }
}
</script>
