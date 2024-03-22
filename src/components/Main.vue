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
        <card />
        <card />
        <card />
        <card />
        <card />
        <card />
    </div>
  </main>
</template>

<style lang="scss" scoped>
main{
  padding-top: 70px;
  .my_container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
}

</style>