<template>
    <div>
      <h1>Login</h1>
      <div class="alert alert-danger" v-if="$route.query.message">
        {{ $route.query.message }}
      </div>
      <form @submit.prevent="onSubmit">
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
      layout: 'empty',
      methods: {
        onSubmit() {
          this.$store.dispatch('login');
          this.$router.push('/');
        }
      }
    }
</script>

<style scoped>
  form {
    width: 500px;
  }
</style>
