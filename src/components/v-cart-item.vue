<template>
  <div class="v-cart-item">
    <img
      class="v-cart-item__image"
      :src="cart_item_data.image"
      alt="img"
    >
    <div class="cart-item__info">
      <p>{{ cart_item_data.name }}</p>
      <p>{{ cart_item_data.price }}</p>
      <p>{{ cart_item_data.article }}</p>
    </div>
    <div class="v-cart-item__quantity">
      <p>Quantity</p>
      <p> {{ cart_item_data.quantity}} </p>
    </div>
    <button @click="deleteFromCart">Delete</button>
  </div>
</template>
<script>
export default {
  name: "v-cart-item",
  props: {
    cart_item_data: {
      type: Object,
      default() {
        return {}
      }
    }
  },
  data() {
    return {
      
    }
  },
  methods: {
    deleteFromCart() {
      this.$emit('deleteFromCart')
    },
  },
  computed: {},
  mounted() {
    /* Так делать во VUE2 */
    // this.$set(this.cart_item_data, 'quantity', 1);
    const cartItemData = this.cart_item_data;
    cartItemData.quantity = 1;
  },
}
</script>

<style>
    
</style>