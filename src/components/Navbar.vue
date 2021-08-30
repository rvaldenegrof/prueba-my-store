<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">

  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavDropdown">
    <ul class="navbar-nav">
      <li class="nav-item active">
          <router-link to="/"><a class="nav-link" href="#">Inicio <span class="sr-only">(current)</span></a></router-link>
        
      </li>
      <li class="nav-item">
          <router-link to="/products"><a class="nav-link" href="#">Productos</a></router-link>
        
      </li>
      <li class="nav-item">
          <router-link to="/newproduct"><a class="nav-link" href="#">Nuevo Producto</a></router-link>
        
      </li>
      <li class="nav-item">
          <router-link to="/carrito"><a class="nav-link" href="#">Carrito</a></router-link>
      </li>
    </ul>
  </div>
</nav>
</template>

<script>
export default {

}
</script>

<style>

</style>