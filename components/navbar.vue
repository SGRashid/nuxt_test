<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">My site</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>

    <div id="navbarSupportedContent" class="collapse navbar-collapse">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item">
          <nuxt-link class="nav-link"
                     to="/"
                     exact
                     active-class="active"
          >Home</nuxt-link>
        </li>
        <li class="nav-item ml-2">
          <nuxt-link class="nav-link"
                     to="/users"
                     active-class="active"
          >Users</nuxt-link>
        </li>
        <li class="nav-item ml-2">
          <nuxt-link class="nav-link"
                     to="/about"
                     active-class="active"
          >About</nuxt-link>
        </li>
        <li class="nav-item ml-2">
          <nuxt-link class="nav-link"
                     to="/login"
                     active-class="active"
          >Login</nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style scoped>

</style>
