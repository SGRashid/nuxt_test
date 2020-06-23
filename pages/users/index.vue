<template>
  <section>
    <h1>Users</h1>
    <ul>
      <li v-for="user of users" :key="user.id">
        <a href="#" @click.prevent="openUser(user)">User {{user.name}}</a>
      </li>
    </ul>
  </section>
</template>

<script>
    export default {
      async asyncData({$axios}) {
        const users = await $axios.$get('https://jsonplaceholder.typicode.com/users');
        console.error(users);
        return { users };
      },
      data: () => ({
      users: []
    }),
      methods: {
        openUser(user) {
          console.log(user.id);
          this.$router.push('/users/' + user.id);
        }
      }
    }
</script>

<style scoped>

</style>
