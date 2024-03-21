<script>
  export default {
    data(){
      return{
        types:[
          {
            text: 'Donna',
            link: '#'
          },
          {
            text: 'Uomo',
            link: '#'
          },
          {
            text: 'bambini',
            link: '#'
          }
        ]
      }
    },

    methods:{
      padding(i){
        if(i > 0 && i < this.types.length - 1){
          return 'px-2'
        }
      }
    }
  }
</script>

<template>
  <header>
    <div class="my_container">
      <div class="my_section">
        <a
        v-for="(type, i) in types"
        :class="padding(i)"
        :href="type.link"
        >{{ type.text }}</a>
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
  box-shadow: 0 1px 3px gray;
  .my_container{
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
        cursor: pointer;
      }
    }
  }
}
</style>