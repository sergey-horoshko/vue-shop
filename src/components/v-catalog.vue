<template>
  <div class="v-catalog">
    <h2>Catalog</h2>
    <div class="v-catalog__list">
      <v-catalog-item
        v-for="product in PRODUCTS"
        :key="product.article"
        :product_data="product"
        @addToCart="addToCart"
      />
    </div>
  </div>
</template>

<script>
  import vCatalogItem from './v-catalog-item'
  import {mapActions, mapGetters} from 'vuex'

  export default {
    name: "v-catalog",
    components: {
      vCatalogItem,
    },
    data() {
      return {}
    },
    computed: { 
      ...mapGetters([
        'PRODUCTS'
      ]),
    },
    methods: {
      ...mapActions([
        'GET_PRODUCTS_FROM_API',
        'ADD_TO_CART'
      ]),
      addToCart(data) {
        this.ADD_TO_CART(data)
      },
    },
    mounted() {
      this.GET_PRODUCTS_FROM_API()
        .then((response) => {
          if (response.data) {
            console.log('Data arrived !');
          }
        })
    },
  }
</script>

<style>

</style>