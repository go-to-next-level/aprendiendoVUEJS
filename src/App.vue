<template>
  <div id="app">
    <TopContext/>
    <router-view/>
  </div>
</template>
<script>
  import TopContext from './components/TopContext.vue'

  export default {
    name: 'app',
    components: {TopContext},
  }
</script>

<style>
  .add-item {
    background-color: #3F51B5;
    font-size: 18px;
    color: white;
    border: 0px;
    border-radius: 3%;
  }

  .add-item:hover {
    box-shadow: 0px 3px 5px #888888;
  }

  .add-item:active {
    box-shadow: 0 0 0 0;
  }

</style>
