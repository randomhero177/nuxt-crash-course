<template>
    <div>
      <h1 v-on:click="showRoute">User {{ $route.params.id }}</h1>
    </div>
</template>

<script>
    export default {
        validate({params}) {
          console.log('validate')
          return /^\d+$/.test(params.id)
        },
        name: "id",
        methods: {
          showRoute() {
            console.log(this.$route);
          }
        }
    }
</script>

<style scoped>

</style>
