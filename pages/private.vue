<template>
  <div>
    <h1>please login</h1>
    <nuxt-link to="/">Go to Home</nuxt-link>
  </div>
</template>
<script>
export default {
  middleware: 'auth'
};
</script>