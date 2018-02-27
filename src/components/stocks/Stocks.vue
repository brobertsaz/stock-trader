<template>
  <div class="row">
    <app-stock
        v-for="stock in stocks"
        :stock="stock"
        v-bind:key="stock.id"></app-stock>
  </div>
</template>

<script>
  import Stock from './Stock.vue'

  export default {
    data() {
      return {
        stocks: [
          { id: 1, name: "BMW", price: 110 },
          { id: 2, name: "AUDI", price: 90 },
          { id: 3, name: "DBENZ", price: 85 },
          { id: 4, name: "PORSH", price: 130 },
        ]
      }
    },
    components: {
      appStock: Stock
    }
  }
</script>
