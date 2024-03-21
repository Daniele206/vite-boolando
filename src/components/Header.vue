<script>
  export default {
    data(){
      return{
        
      }
    }
    
  }
</script>

<template>
  <header>
    <div class="container">
      <div class="my_section">
        <a href="#">Donna</a>
        <a href="#" class="px-3">Uomo</a>
        <a href="#">Bambini</a>
      </div>
      <div class="my_section d-flex justify-content-center">
        <img class="w-75" src="/public/boolean-logo.png" alt="Boolean">
      </div>
      <div class="my_section d-flex justify-content-end">
        <i class="fa-regular fa-user"></i>
        <i class="px-2 fa-regular fa-heart"></i>
        <i class="fa-solid fa-bag-shopping"></i>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

header{
  background-color: $my_orange;
  height: 70px;
  position: fixed;
  width: 100%;
  .container{
    height: 100%;
    color:white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .my_section{
      width: 220px;
      a{
        text-decoration: none;
        color: white;
        font-weight: bold;
      }
      i{
        color: white;
        font-size: 1.2rem;
      }
    }
  }
}
</style>