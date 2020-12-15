<template>
    <div>
      <h1>Login</h1>
      <form>
        <div>
          <input type="text" class="form-control">
        </div>
        <p>
          <nuxt-link to="/">To home page</nuxt-link>
        </p>
        <button class="btn btn-primary" type="submit">Login</button>
      </form>
    </div>
</template>

<script>
    export default {
        name: 'login',
        layout: 'empty'
    }
</script>

<style scoped>
  form {
    width: 500px;
  }
</style>
