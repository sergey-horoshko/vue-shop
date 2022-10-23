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
      @click="addToCart"
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
    addToCart() {
      this.$emit('addToCart', this.product_data);
    },
  },
}
</script>

<style>
</style>