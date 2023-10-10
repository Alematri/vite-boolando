<script>
  export default{
  name: 'Main'
}
</script>

<template>
  <main>

    <div class="container">

      <div class="row d-flex flex-wrap">

                <!-- CARD 1 -->
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/1.webp" alt="1">
                <img class="secondary-image" src="../assets/img/1b.webp" alt="1b">
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

                <!-- CARD 2 -->
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/2.webp" alt="2">
                <img class="secondary-image" src="../assets/img/2b.webp" alt="2b">
              </div>
          
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
              <span class="discount">-30%</span>
              </div>

            </div>

            <div class="card-text">
              <span class="brand">Guess</span>
              <h3 class="product-name">ROSES TEE</h3>
                <div class="price">
                  <span>20.99&euro;</span>
                <span>29.99&euro;</span>
                </div>
            </div>
          </div>
        </div>

              <!-- CARD 3 -->
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/3.webp" alt="3">
                <img class="secondary-image" src="../assets/img/3b.webp" alt="3b">
              </div>
          
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
              <span class="discount">-30%</span>
              </div>

            </div>

            <div class="card-text">
              <span class="brand">Come Zucchero Filato</span>
              <h3 class="product-name">VOGLIA DI COLORI PASTELLO</h3>
                <div class="price">
                  <span>129.99&euro;</span>
                <span>184.99&euro;</span>
                </div>
            </div>
          </div>
        </div>

              <!-- CARD 4 -->
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/4.webp" alt="4">
                <img class="secondary-image" src="../assets/img/4b.webp" alt="4b">
              </div>
          
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
              <span class="discount">-50%</span>
              <span class="tag">Sostenibiltà</span>
              </div>

            </div>

            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">TEE UNISEX</h3>
                <div class="price">
                  <span>14.99€</span>
                <span>29.99€</span>
                </div>
            </div>
          </div>
        </div>

              <!-- CARD 5 -->
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/5.webp" alt="5">
                <img class="secondary-image" src="../assets/img/5b.webp" alt="5b">
              </div>
          
              <div class="favourite">&hearts;</div>

            </div>

            <div class="card-text">
              <span class="brand">Maya Deluxe</span>
              <h3 class="product-name">STRIPE BODICE</h3>
                <div class="price">
                  <span>14.99€</span>
                </div>
            </div>
          </div>
        </div>

              <!-- CARD 6 -->        
        <div class="col">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/6.webp" alt="6">
                <img class="secondary-image" src="../assets/img/6b.webp" alt="6b">
              </div>
          
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
              <span class="tag">Sostenibiltà</span>
              </div>

            </div>

            <div class="card-text">
              <span class="brand">Espirit</span>
              <h3 class="product-name">MAGLIONE - BLACK</h3>
                <div class="price">
                  <span>14.99€</span>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>

</template>

<style lang="scss" scoped>

  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;
  @use '../scss/partials/utility' as *;
  @use '../scss/partials/variabiles' as *;

  main{
    padding-top: 130px;
    padding-bottom: 60px;
    .card-image{
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

  main .card-image:hover .secondary-image{
    display: block;
  }

</style>