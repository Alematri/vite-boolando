<script>

  export default{
  name: 'ProductCard',
  props:{
    productObj: Object
  },
  methods:{
    getImagePath(img){
      return new URL(`../../assets/img${img}`, import.meta.url).href;
    }
  }
}
</script>

<template>
  <div class="col">
    <div class="card">
      <div class="card-image">
        <div class="images">
          <img :src="getImagePath(productObj.primaryImage)">
          <img class="secondary-image" :src="getImagePath(productObj.secondaryImage)">
        </div>
            
        <div class="favourite">&hearts;</div>
        <div class="card-badge">
          <span v-if="productObj.discount" class="discount">{{productObj.discount}}</span>
          <span v-if="productObj.sostenibilita" class="tag">sostenibiltà</span>
        </div>
      </div>

      <div class="card-text">
        <span class="brand">{{productObj.marca}}</span>
        <h3 class="product-name">{{productObj.mdello}}</h3>
        <div class="price">
          <span>{{productObj.fullPrice}}&euro;</span>
          <span v-if="productObj.fullPrice">{{productObj.lastPrice}}&euro;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
</style>