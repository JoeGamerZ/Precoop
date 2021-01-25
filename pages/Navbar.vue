<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <nuxt-link class="navbar-item" to="/">
        Movie Application
      </nuxt-link>
      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div class="navbar-menu">
      <div class="navbar-start">
        <nuxt-link class="navbar-item" to="/">
          Home
        </nuxt-link>
       
      </div>
      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <nuxt-link to="/login" class="button is-primary">
              <strong>Login</strong>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
export default {}
</script>
