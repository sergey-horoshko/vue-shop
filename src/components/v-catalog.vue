<template>
  <div class="v-catalog">
    <h2>Catalog</h2>
    <div class="v-catalog__list">
      <v-catalog-item
        v-for="product in products"
        :key="product.article"
        :product_data="product"
        @sendArticle="showChildArticleInConsole"
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
        "products": [
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/8cf/500_500_1/8cf3cfc21dd67fd5261fa3fbb88af1c2.jpg",
            "name": "T-shirt 1",
            "price": 100,
            "article": "T1",
            "available": true
          },
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/e0e/500_500_1/e0edacb921db51594672e2b6fcc29a6e.jpg",
            "name": "T-shirt 2",
            "price": 150,
            "article": "T2",
            "available": true
          },
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/794/500_500_1/794cf1e626a13479be47e00b71eb133c.jpg",
            "name": "T-shirt 3",
            "price": 200,
            "article": "T3",
            "available": false
          },
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/196/500_500_1/1967eb8087e6df41b976ac3f436a7667.jpg",
            "name": "T-shirt 4",
            "price": 350,
            "article": "T4",
            "available": true
          },
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/ffa/500_500_1/ffab0f07868750f653f9ec007292e4c5.jpg",
            "name": "T-shirt 5",
            "price": 400,
            "article": "T5",
            "available": true
          },
          {
            "image": "https://static.street-beat.ru/upload/resize_cache/iblock/fb0/500_500_1/fb0c74aaa7653e9ae5a3b575f95a24a0.jpg",
            "name": "T-shirt 6",
            "price": 450,
            "article": "T6",
            "available": false
          }
        ],
      }
    },
    methods: {
      showChildArticleInConsole(data) {
        console.log(data)
      },
    },
    created() {
    },
  }
</script>

<style>

</style>