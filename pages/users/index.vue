<template>
    <section>
      <h1>Users</h1>
      <ul>
        <li v-for="user of usersList" :key="user.id">
          <a href="#" @click.prevent="openUser(user.id)">{{ user.name }}</a>
        </li>
      </ul>
    </section>
</template>

<script>
    export default {
      async asyncData({$axios}) {
        const usersList = await $axios.$get('https://jsonplaceholder.typicode.com/users');
        return {usersList}
      },
      name: "index",
      data: () => ({
        usersList: [],
        url: 'https://jsonplaceholder.typicode.com/users'
      }),
      methods: {
        openUser(user) {
          this.$router.push('/users/' + user)
        }
      }
    }
</script>

<style scoped>

</style>
