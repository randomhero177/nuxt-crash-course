<template>
    <section>
      <h1>Users</h1>
      <ul>
        <li v-for="user of 5" :key="user">
          <a href="#" @click.prevent="openUser(user)">USER {{ user }}</a>
        </li>
      </ul>
    </section>
</template>

<script>
    export default {
        name: "index",
        methods: {
          openUser(user) {
            this.$router.push('/users/' + user)
          }
        }
    }
</script>

<style scoped>

</style>
