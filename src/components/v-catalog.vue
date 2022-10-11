<template>
  <div class="v-catalog">
    <h2>Catalog</h2>
    <div class="v-catalog__list">
      <v-catalog-item
        v-for="product in products"
        :key="product.article"
        :product_data="product"
      />
    </div>
  </div>
</template>

<script>
  import vCatalogItem from './v-catalog-item'

  export default {
    name: "v-catalog",
    components: {
      vCatalogItem,
    },
    data() {
      return {
        products: [
          {
            image: "1.jpg",
            name: "T-shirt 1",
            price: 100,
            article: "T1",
            available: true
          },
          {
            image: "2.jpg",
            name: "T-shirt 2",
            price: 150,
            article: "T2",
            available: true
          },
          {
            image: "3.jpg",
            name: "T-shirt 3",
            price: 200,
            article: "T3",
            available: false
          },
          {
            image: "4.jpg",
            name: "T-shirt 4",
            price: 350,
            article: "T4",
            available: true
          },
          {
            image: "5.jpg",
            name: "T-shirt 5",
            price: 400,
            article: "T5",
            available: true
          },
          {
            image: "6.jpg",
            name: "T-shirt 6",
            price: 450,
            article: "T6",
            available: false
          }
        ]
      }
    },
  }
</script>

<style>

</style>