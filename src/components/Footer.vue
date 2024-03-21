<script>
  export default {
    data(){
      return{
        info:[
          {
            text: 'Informazioni legali',
            link: '#'
          },
          {
            text: 'Informativa sulla privacy',
            link: '#'
          },
          {
            text: 'Diritto di recesso',
            link: '#'
          }
        ],
        socials:[
          'fa-brands fa-x-twitter',
          'fa-brands fa-square-facebook',
          'fa-brands fa-square-instagram',
          'fa-brands fa-square-pinterest',
          'fa-brands fa-square-youtube',
        ]
      }
    },
    
    methods:{
      padding(i){
        if(i > 0 && i < this.info.length - 1){
          return 'px-2'
        }
      }
    }
  }
</script>

<template>
  <footer>
    <div class="my_container">
      <div>
        <span class="agency">Boolando s.r.l.</span>
        <div>
          <a
          v-for="(infor, i) in info"
          :class="padding(i)"
          :href="infor.link"
          >{{ infor.text }}</a>
        </div>
      </div>
      <div>
        <span class="social_direct">Trovaci anche su</span>
        <div class="d-flex justify-content-between">
          <i v-for="social in socials" :class="social"></i>
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