<template>
    <section>
      <h1>{{user.name}}</h1>
      <hr/>
      <h3>{{user.email}}</h3>
      <h3>{{user.phone}}</h3>
    </section>
</template>

<script>
    export default {
        validate({params}) {
          console.log('validate');
          // return /^\d+$/.test(params.id);
          return true;
        },
      async asyncData({$axios, params}) {
          const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id);
          return { user };
      }
    }
</script>

<style scoped>

</style>
