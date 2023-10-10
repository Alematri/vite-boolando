<script>
  export default{
  name: 'Header'
}
</script>

<template>

<header>
    <div class="container d-flex justify-content-between h-100 align-center">

      <nav class="main-menu">
        <ul class="d-flex">
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Donna</a></li>
          <li><a href="#">Bambimo</a></li>
        </ul>
      </nav>
      
      <div class="box-logo">
        <div class="logo">
         <img src="../assets/img/boolean-logo.png" alt="logoboolean">
        </div>
      </div>

      <nav class="social-menu">
        <ul class="d-flex">
          <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
          <li><a href="#"><i class="fa-regular fa-heart"></i></a></li>
          <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
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