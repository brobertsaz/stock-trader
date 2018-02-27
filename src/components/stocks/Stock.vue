<template>
  <div class="col-sm-6 col-md-4">
    <div class="card mt-4">
      <div class="card-header bg-info">
        <div class="card-title d-flex">
          <h5>{{ stock.name }}</h5>
          <div class="small pt-1 pl-2">(Price: {{ stock.price }})</div>
        </div>
      </div>
      <div class="card-body">
        <div class="card-text d-flex">
          <div class="mr-auto p-2">
            <input type="number"
                   class="form-control"
                   placeholder="Quantity"
                   v-model="quantity">
          </div>
          <div class="p-2">
            <button class="btn btn-success"
                    @click="buyStock"
                    >Buy</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['stock'],
  data() {
    return {
      quantity: 0
    }
  },
  methods: {
    buyStock() {
      const order = {
        stockId: this.stock.id,
        stockPrice: this.stock.price,
        quantity: this.quantity
      }
      console.log(order)
      this.quantity = 0
    }
  }
}
</script>


