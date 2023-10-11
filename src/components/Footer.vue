<script>

  import { main_menu, social_menu } from '../data/menu';

  export default{
  name: 'Footer',
  data(){
    return{
      main_menu,
      social_menu
    }
  }
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
        <li v-for="(item, index) in social_menu.footer"
         :key="index">
         <a :href="item.href"><i :class="item.icon_class"></i></a>
        </li>
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