<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Nuxt SSR</a>

    <div class="collapse navbar-collapse">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item">
          <nuxt-link exact class="nav-link" active-class="active" to="/">Home</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" active-class="active" to="/about">About</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" active-class="active" to="/users">Users</nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
    export default {
        name: "Navbar"
    }
</script>

<style scoped>

</style>
