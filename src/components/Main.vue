<script>

  import ProductCard from './partials/ProductCard.vue';
  import products from '../data/products';

  export default{
  name: 'Main',
  components:{
    ProductCard
  },
  data(){
    return{
      products
    }
  }
}
</script>

<template>
  <main>

    <div class="container">

      <div class="row d-flex flex-wrap">

        <ProductCard
        v-for="product in products"
        :key="product.id"
        :productObj="product"
        />

      </div>

    </div>
  </main>

</template>

<style lang="scss">

  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;
  @use '../scss/partials/utility' as *;
  @use '../scss/partials/variabiles' as *;

  main{
    padding-top: 130px;
    padding-bottom: 60px;
    .card-image{
      &:hover{
        .secondary-image{
          display: block;
        }
      }
      .secondary-image{
        position: absolute;
        top: 0px;
        left: 0px;
        display: none;
      }
    }
    .row{
      .col{
        width: calc(100% /3);
        min-width: 250px;
        padding: 0 10px;
        margin-bottom: 20px;
        .favourite{
          background-color: $white;
          cursor: pointer;
          top: 10px;
          right: 0px;
          padding: 10px 18px;
          font-size: 2.2rem;
          &:hover{
            color: $red;
          }
        }
        .favourite, .card-badge{
          position: absolute;
        }
        .card{
          .card-image{
            position: relative;
            .card-badge{
              left: 0;
              bottom: 10px;
              color: $white;
              font-weight: bold;
              padding: 50px 0;
              span{
                padding: 5px;
              }
              .discount{
                background-color: $red;
              }
              .tag{
                background-color: $green;
              }
            }
          }
        }
      }
    }
  }

</style>