<script>
  import card from './partials/card.vue';
  import { products } from '../data/db.json';

  export default {
    data(){
      return{
        products
      }
    },

    components:{
      card  
    }
  }
</script>

<template>
  <main>
    <div class="my_container">
      <card
      v-for="product in products"
      :key="product.id"
      :firstrImg="product.frontImage"
      :secondImg="product.backImage"
      :productBrand="product.brand"
      :productName="product.name"
      :productPrice="product.price"
      :isLike="product.isInFavorites"
      :productBages="product.badges"
      />
    </div>
  </main>
</template>

<style lang="scss" scoped>
main{
  padding-top: 70px;
  .my_container{
    padding: 40px 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
}

</style>