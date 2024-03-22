<script>
  export default {
    props:{
      firstrImg: String,
      secondImg: String,
      productBrand: String,
      productName: String,
      productPrice: Number,
      isLike: Boolean,
      productBages: Array
    },
    
    methods:{
      discSos(type){
        if(type === 'discount'){
          return 'discount'
        }else if(type === 'tag'){
          return 'sostenibility'
        }
      },
      
      reverseArray(array){
        if(array.length > 1){
          if(array.at(0).type === 'tag'){
            array.unshift(array[array.length -1])
            array.splice(array.length-1, 1)
            return array
          }
          return array
        }else{
            return array
        }
      }
      
    }
  }
</script>

<template>
  <div class="my_card">
    <div class="my_card_img">
      <img class="my_img_first" :src="`public/img/${firstrImg}`" alt="non si vede l'immagine">
      <img class="my_img_second" :src="`public/img/${secondImg}`" alt="">
      <div class="like">
        <i :class="{'red' : isLike}" class="fa-solid fa-heart"></i>
      </div>
      <div class="product_info">
        <span v-for="(bage, i) in reverseArray(productBages)" :key="i" :class="discSos(bage.type)">{{ bage.value }}</span>
      </div>
    </div>
    <div class="description">
      <span>{{ productBrand }}</span>
      <span class="product-name">{{ productName }}</span>
      <span>{{ productPrice }}&euro;</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.red{
  color: $my_red;
};

.my_card{
  width: 460px;
  max-width: 100%;
  margin: 25px auto;
  .my_card_img{
    cursor: pointer;
    position: relative;
    &:hover .my_img_second{
      display: block;
    };
    .my_img_second{
      display: none;
      position: absolute;
      top: 0;
      left: 0;
    };
    .like{
      background: white;
      width: 50px;
      aspect-ratio: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      position: absolute;
      top: 20px;
      right: 0;
    };
    .product_info{
      position: absolute;
      bottom: 40px;
      left: 0;
      color: white;
      font-weight: bold;
      .discount{
        background-color: $my_red;
        padding: 5px 10px;
        margin-right: 5px;
      };
      .sostenibility{
        background-color: $my_green;
        padding: 5px 10px;
      };
    };
  };
  .description{
    span{
      display: block;
      line-height: 1.15rem
    };
    .product-name{
      text-transform: uppercase;
      font-weight: bold;
      font-size: 1.3rem;
    }
  }
}

</style>