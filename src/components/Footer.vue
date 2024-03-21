<script>
  export default {
    
  }
</script>

<template>
  <footer>
    <div class="my_container">
      <div>
        <span class="agency">Boolando s.r.l.</span>
        <div>
          <a href="#">Informazioni legali</a>
          <a class="px-2" href="#">Informativa sulla privacy</a>
          <a href="#">Diritto di recesso</a>
        </div>
      </div>
      <div>
        <span class="social_direct">Trovaci anche su</span>
        <div class="d-flex justify-content-between">
          <i class="fa-brands fa-x-twitter"></i>
          <i class="fa-brands fa-square-facebook"></i>
          <i class="fa-brands fa-square-instagram"></i>
          <i class="fa-brands fa-square-pinterest"></i>
          <i class="fa-brands fa-square-youtube"></i>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

footer{
  background-color: $my_black;
  padding: 25px 0 25px 0;
  .my_container{
    color:white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .agency{
      font-weight: bold;
      font-size: 1.2rem;
    };
    a{
        text-decoration: none;
        color: white;
        font-size:.8rem;
      };
    .social_direct{
      font-weight: bold;
      font-size: 1.2rem;
    };
    i{
      font-size: 1.7rem;
    }
  }
}

</style>