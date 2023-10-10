<script>
  export default{
  name: 'Footer'
}
</script>

<template>
    <footer>
    <div class="container d-flex justify-content-between h-100 align-center">
      
      <div class="footer-info">
        <h3>Boolando s.r.l</h3>
        <a href="#">Informazioni legali</a>
       <a href="#">Informativa sulla privacy</a>
       <a href="#">Diritto di recesso</a>
      </div>

      <div class="footer-social">
       <h4>Trovaci anche su</h4>
        <ul class="d-flex">
         <li><a href="#"><i class="fa-brands fa-square-twitter"></i></a></li>
         <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
         <li><a href="#"><i class="fa-brands fa-square-instagram"></i></a></li>
         <li><a href="#"><i class="fa-brands fa-square-pinterest"></i></a></li>
         <li><a href="#"><i class="fa-brands fa-square-youtube"></i></a></li>
        </ul>
      </div>
    </div>
  </footer>  
</template>

<style lang="scss" scoped>
  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;
  @use '../scss/partials/utility' as *;
  @use '../scss/partials/variabiles' as *;

  footer{
    background-color: $footer-gray;
    padding-top: 30px;
    padding-bottom: 30px;
    width: 100%;
    .footer-social{
      ul{
        justify-content: space-between;
      }
      h4{
        text-align: center;
        margin-bottom: 10px;
      }
    }
    .footer-info{
      h3{
        margin-bottom: 10px;
      }
    }
  }

</style>