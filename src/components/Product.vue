<template>
  <div class="product">
    <router-link class="product" v-bind:to="url">
      <img class="thumbnail" v-bind:src="product.image" v-bind:alt="product.name" height="200"/>
      <p>{{ product.name }}</p>
      <button class="add-item"
              v-bind:data-item-name="product.name"
              v-bind:data-item-id="product.id"
              v-bind:data-item-image="product.image"
              data-item-url="url"
              v-bind:data-item-price="product.price">Ver
      </button>
    </router-link>
  </div>
</template>
<script>
  export default {
    name: 'Product',
    props: ['product'],
    computed: {
      url () {
        return `/products/${this.product.id}`
      },
    },
  }
</script>

<style scoped>
  .product {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 35px;
  }

  .product:hover {
    background-color: #CFD8DC;
  }

</style>
