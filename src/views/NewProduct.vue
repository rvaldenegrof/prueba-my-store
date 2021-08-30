<template>
  <form @submit.prevent="handleFormSubmit" class="form">


  <div class="form-group col-6">
    <label for="nombreProducto">Nombre Producto</label>
    <input type="text" class="form-control" v-model="form.name" id="nombreProducto" aria-describedby="nombreHelp" placeholder="Nombre del Producto" required>
    <!-- <small id="nombreHelp" class="form-text text-muted">Debe ingresar el nombre del producto.</small> -->
  </div>
  <div class="form-group col-6">
    <label for="precioProducto">Precio del Producto</label>
    <input type="text" class="form-control" v-model="form.price" id="precioProducto" aria-describedby="precioHelp" placeholder="Precio del Producto" required>
    <!-- <small id="precioHelp" class="form-text text-muted">Debe ingresar el precio del producto.</small> -->
  </div>

  <div class="form-group col-6">
    <label for="categoriaProducto">Categoria</label>
    <select class="form-control" v-model="form.category" id="categoriaProducto" required>
      <option value="Food">Comida</option>
      <option value="Pets">Mascotas</option>
      <option value="Other">Otro</option>
    </select>
  </div>

    <div class="form-group col-3">
    <label for="colorProducto">Color</label>
    <input type="color" class="form-control" v-model="form.color" id="colorProoducto" required />
  </div>

  <div class="form-check col-6 ml-3 mb-2">
    <input type="checkbox" class="form-check-input" id="exampleCheck1" v-model="form.offer">
    <label class="form-check-label" for="exampleCheck1">Oferta</label>

    <label for="" v-if="form.offer" class="ml-2">Descuento</label>
    <input
    class="col-3 ml-2"
      type="number"
      min="1"
      max="100"
      v-model="form.discount"
      v-if="form.offer"
      required
    />
  </div>
  <button type="submit" class="btn btn-primary">Guardar</button>

<!-- <hr />
      <label for="">Nombre Producto</label>
      <input type="text" v-model="form.name" required />
    
    <br />
      <label for="">Precio del producto</label>
      <input type="number" v-model.number="form.price" required />

    <br />
      <label for="">Categoria</label>
      <select v-model="form.category" required>
      <option value="Food">Comida</option>
      <option value="Pets">Mascotas</option>
      <option value="Other">Otro</option>
    </select>
  
    <br />
    <label>Color</label>
    <input type="color" v-model="form.color" required />
    <br />
    <label>Oferta</label>
    <input type="checkbox" v-model="form.offer" />
    <label for="" v-if="form.offer" class="ml-2">Descuento</label>
    <input
      type="number"
      min="1"
      max="100"
      v-model="form.discount"
      v-if="form.offer"
      required
    />

    <br />
    <button type="submit">Guardar</button> -->
  </form>
</template>

<script>
export default {
  name: 'NewProduct',
  data: () => ({
    form: {
      name: '',
      price: null,
      category: '',
      offer: false,
      discount: null,
      color: ''
    }
  }),
  methods: {
    async handleFormSubmit() {
      await this.$store.dispatch('agregarProducto', this.form)
      this.$router.push('/products')
    }
  }
}
</script>

<style scoped>
/* .form {
  border: 1px solid black;
  width: 80%;
}
td {
    border: 1px solid black;
} */
</style>
