<script>

  export default{
  name: 'ProductCard'
}
</script>

<template>
  <div class="col">
    <div class="card">
      <div class="card-image">
        <div class="images">
          <img src="../../assets/img/1.webp" alt="1">
          <img class="secondary-image" src="../../assets/img/1b.webp" alt="1b">
        </div>
            
        <div class="favourite">&hearts;</div>
        <div class="card-badge">
          <span class="discount">-50%</span>
          <span class="tag">Sostenibiltà</span>
        </div>
      </div>

      <div class="card-text">
        <span class="brand">Levi's</span>
        <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
        <div class="price">
          <span>14.99&euro;</span>
          <span>29.99&euro;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
</style>