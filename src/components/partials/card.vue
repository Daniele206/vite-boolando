<script>
  export default {
    props:{

    }
  }
</script>

<template>
  <div class="my_card">
    <div class="my_card_img">
      <img class="my_img_first" src="../../assets/img/1.webp" alt="">
      <img class="my_img_second" src="../../assets/img/1b.webp" alt="">
      <div class="like">
        <i class="fa-solid fa-heart"></i>
      </div>
      <div class="product_info">
        <span class="discount">-50%</span> <span class="sostenibility">Sostenibilitá</span>
      </div>
    </div>
    <div class="description">
      <span>text</span>
      <span>text</span>
      <span>price</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.my_card{
  width: 33%;
  min-width: 460px;
  margin: 25px 0;
  background-color: red;
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
      &:hover i{
        color: $my_red;
      }
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
    }
  }
}

</style>