<template>
  <div class="v-catalog-item">
    <img 
      :src="product_data.image"
      :title="product_data.name"
      class="v-catalog-item__img" 
      alt="img"
    >
    <p class="v-catalog-item__name">{{ product_data.name }}</p>
    <p class="v-catalog-item__price">Price: {{ product_data.price }} ₽</p>
    <button 
      class="v-catalog-item__add_to_cart_btn btn" 
      @click="sendDataToParrent"
    >
      Add to cart
    </button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
    },
  },
  data() {
    return {}
  },
  methods: {
    sendDataToParrent() {
      this.$emit('sendArticle', this.product_data.article)
    },
  },
}
</script>

<style>
  .v-catalog-item__img {
    width: 100%;
  }
</style>