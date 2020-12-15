<template>
    <div>
      <h1 v-on:click="showRoute">{{ user.name }}</h1>
      <hr />
      <h4>{{ user.email }}</h4>
    </div>
</template>

<script>
    export default {
      async asyncData({$axios, params}) {
        const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id);
        return {user}
      },
      validate({params}) {
        console.log('validate');
        return /^\d+$/.test(params.id)
      },
      name: "id",
      data: () => ({
        user: {}
      }),
      methods: {
        showRoute() {
          console.log(this.$route);
        }
      }
    }
</script>

<style scoped>

</style>
