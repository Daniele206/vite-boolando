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
          {
            class: 'fa-brands fa-x-twitter',
            link: '#'
          },
          {
            class: 'fa-brands fa-square-facebook',
            link: '#'
          },
          {
            class: 'fa-brands fa-square-instagram',
            link: '#'
          },
          {
            class: 'fa-brands fa-square-pinterest',
            link: '#'
          },
          {
            class: 'fa-brands fa-square-youtube',
            link: '#'
          },
        ]
      }
    },
    
    methods:{
      padding(i){
        if(i > 0 && i < this.info.length - 1){
          return 'mx-2'
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
          <ul class="my_menu">
            <li v-for="(infor, i) in info"
            :key="`i-${i}`">
              <a
              :class="padding(i)"
              :href="infor.link"
              >{{ infor.text }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div>
        <span class="social_direct">Trovaci anche su</span>
        <div>
          <ul class="my_menu justify-content-between">
            <li v-for="(social, i) in socials"
            :key="`s-${i}`">
              <a :href="social.link">
                <i :class="social.class"></i>
              </a>
            </li>
          </ul>
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