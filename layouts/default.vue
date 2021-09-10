<template>
<div>
<div class="navbar">
<nuxt-link to="/">Home</nuxt-link>
<nuxt-link to="/videos">Videos</nuxt-link>
</div>
  <Nuxt />
</div>

</template>
<style  scoped>

.navbar{
  background: lightseagreen;
  width: 100%;
  height: 40px;
 
}
.navbar a{
  color: white;
  text-decoration: none;
  margin-right: 10px;
}
</style>