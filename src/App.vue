<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Yugioh Store</a>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active"><router-link class="nav-link" to="/">Home</router-link></li>
          <li class="nav-item active"><router-link class="nav-link" to="/admin">Cart</router-link></li>
          <li class="nav-item active"><router-link class="nav-link" to="/cart">Admin</router-link></li>        
        </ul>
      </div>
    </nav>
  <router-view></router-view>  
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
