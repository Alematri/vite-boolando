<script>

  export default{
  name: 'ProductCard',
  props:{
    productObj: Object
  }
}
</script>

<template>
  <div class="col">
    <div class="card">
      <div class="card-image">
        <div class="images">
          <img :src="`/img/${productObj.primaryImage}`">
          <img class="secondary-image" :src="`/img/${productObj.secondaryImage}`">
        </div>
            
        <div class="favourite">&hearts;</div>
        <div class="card-badge">
          <span v-if="productObj.discount" class="discount">{{productObj.discount}}</span>
          <span v-if="productObj.sostenibilita" class="tag">Sostenibiltà</span>
        </div>
      </div>

      <div class="card-text">
        <span class="brand">{{productObj.marca}}</span>
        <h3 class="product-name">{{productObj.modello}}</h3>
        <div class="price">
          <span>{{productObj.lastPrice}}&euro;</span>
          <span v-if="productObj.fullPrice">{{productObj.fullPrice}}&euro;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
</style>