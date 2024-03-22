<script>
  import { headerMenues } from '../data/menues';
  
  export default {
    computed:{
      types(){
        return headerMenues.types
      },
      icoMenu(){
        return headerMenues.icoMenu
      }
    },

    methods:{
      padding(i){
        if(i > 0 && i < this.types.length - 1){
          return 'mx-2'
        }
      }
    }
}
</script>

<template>
  <header>
    <div class="my_container">
      <div class="my_section">
        <ul class="my_menu">
          <li v-for="(type, i) in types"
          :key="`t-${i}`">
            <a
            :class="padding(i)"
            :href="type.link"
            >{{ type.text }}</a>
          </li>
        </ul>
      </div>
      <div class="my_section d-flex justify-content-center">
        <img class="w-75" src="/public/img/boolean-logo.png" alt="Boolean">
      </div>
      <div class="my_section d-flex justify-content-end">
        <ul class="my_menu">
          <li v-for="(ico, i) in icoMenu"
          :key="`ico-${i}`">
            <a :href="ico.link">
              <i :class="ico.class"></i>
            </a>
          </li>
        </ul>
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
      display: flex;
      align-items: center;
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