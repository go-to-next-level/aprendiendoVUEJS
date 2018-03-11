<template>
  <div>
    <div class="topcontext">
      <router-link class="home__title" to="/">
        Vue.js Demo Store
      </router-link>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TopContext',
  }
</script>

<style>
  .topcontext {
    padding-top: 20px;
    width: 100%;
    height: 100px;
    background-color: #212121;
    color: #FAFAFA;
    text-align: center;
    font-weight: bold;
    font-size: 25pt;
  }

  .home__title {
    text-decoration: none;
    color: white;
  }

</style>
