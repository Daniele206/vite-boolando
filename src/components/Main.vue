<script>
  import card from './partials/card.vue';

  export default {
    components:{
      card
    }
  }
</script>

<template>
  <main>
    <div class="my_container">
      <div class="my_row">
        <card />
        <card />
        <card />
        <card />
        <card />
        <card />
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main{
  padding-top: 70px;
  .my_container{
    padding: 40px 0;
    display: flex;
    justify-content: center;
    .my_row{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
  }
}

</style>