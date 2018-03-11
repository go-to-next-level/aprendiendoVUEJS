<template>
  <div class="product-details">
    <img class="thumbnail"
         v-bind:src="product.image"
         v-bind:alt="product.name"
         height="200"/>
    <div class="product-description">
      <p>{{ product.name }}</p>
      <p>{{product.description}}</p>
      <button class="add-item"
              v-bind:data-item-name="product.name"
              v-bind:data-item-id="product.id"
              v-bind:data-item-image="product.image"
              data-item-url=""
              v-bind:data-item-price="product.price">Su precio aproximado es de {{product.price}}$
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ProductDetails',
    computed: {
      id () {
        return this.$store.state.route.params.id
      },
      product () {
        return this.$store.getters.getProductById(this.id)
      },
    },
  }
</script>
<style scoped>
  .product-description {
    width: 400px;
    padding: 25px;
    margin: 25px;
    background-color: #CFD8DC;
    font-size: 20px;
  }

  .product-details {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

</style>
