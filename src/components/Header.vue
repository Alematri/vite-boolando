<script>

  import { main_menu, social_menu } from '../data/menu';

  export default{
  name: 'Header',
  data(){
    return{
      main_menu,
      social_menu
    }
  }
}
</script>

<template>

<header>
    <div class="container d-flex justify-content-between h-100 align-center">

      <nav class="main-menu">
        <ul class="d-flex">
          <li
          v-for="(item, index) in main_menu"
          :key="index"
          ><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </nav>
      
      <div class="box-logo">
        <div class="logo">
         <img src="../assets/img/boolean-logo.png" alt="logoboolean">
        </div>
      </div>

      <nav class="social-menu">
        <ul class="d-flex">
          <li
          v-for="(item, index) in social_menu.header"
          :key="index"
          ><a :href="item.href"><i :class="item.icon_class"></i></a>
          </li>
        </ul>
      </nav>

    </div>
  </header>


</template>

<style lang="scss" scoped>
  @use '../scss/partials/general' as *;
  @use '../scss/partials/typography' as *;
  @use '../scss/partials/utility' as *;
  @use '../scss/partials/variabiles' as *;

  header{
  position: fixed;
  top: 0;
  left: 0;
  right: 0; /* al posto di dire width 100% */
  background-color: #FA6903;
  height: 80px;
  color: white;
  box-shadow: 0 1px 3px gray;
  z-index: 1;
}

header{
  .conteiner{
  padding: 0 10px;
  }
  .logo{
  width: 180px;
  }
  nav{
    width: 30%;
  }
}


header nav.social-menu ul{
  justify-content: flex-end;
}

header nav.main-menu a{
  padding-right: 20px;
}

header nav.social-menu a{
  padding-left: 5px;
}
</style>