<template>
  <div class="container-lg mt-5 pt-lg-5 px-5 px-lg-0 position-relative">
    <div class="row">
        <!-- text part -->
        <div class="col-12 col-md-6">
            <div class="row px-lg-5">
                <div class="col-12 pt-md-5">
                  <span class="txt-container">
                    <strong class="text-uppercase">hac tellus, felis risus at </strong>mattis mattis. Eget euismod sempere eget tortor, donec amet, blandit. 
                    Tristique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis facilisis amet vulputate.
                  </span>
                </div>
                <div class="col-12 mt-4  text-uppercase ">
                  <span class="title-lg d-none d-lg-block pe-lg-5 " @click="startEasterEgg()">
                      food is our common ground, a universal experience.
                  </span>
                  <span class="d-lg-none title-smartphone " @click="startEasterEgg()">
                      <strong>food is our common ground, a universal experience.</strong>
                  </span>
                </div>
                <div class="col-12 mt-4">
                  <span class="txt-container">
                    Tristique tempus condimentum diam donec. Condimentum ullamcorper sit elementum hendrerit mi nulla in consequat, ut.
                    Metus, nullam scelerisque netus viverra dui.
                  </span>
                </div>
                <div class="col-6 mt-3 mt-lg-5">
                    <img src="/img/signature.jpg" alt="signature">
                </div>
            </div>
        </div>

        <!-- img part -->
        <div class="d-none d-md-block col-md-6"  >
            <div class="img-container position-relative">
                <img src="/img/info22x.jpg" alt="california roll">
                <div class="position-absolute txt-absolute">
                  <span class="text-uppercase">california roll $22</span>
                </div>
            </div>
        </div>
    </div>
    <!-- easteregg part -->
    <div class="position-absolute" :class="counterEasterEgg >= 5 ? 'animation-to-right' : 'd-none'">
        <img src="/img/bg-sushi.png" alt="">
    </div>
    <div class="position-absolute" :class="counterEasterEgg >= 5 ? 'animation-to-left' : 'd-none'">
        <img src="/img/bg-sushi2.png" alt="">
    </div>
  </div>   
</template>

<script>
export default {
  methods : {
    startEasterEgg(){
      this.counterEasterEgg++
    }
  },
  data : function(){
    return{
      counterEasterEgg : 0,
      cardsInfoPromo : [
        {
          id : 0,
          img : '/img/sushi-1.png',
          title : 'the best table in town',
          txt : 'sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn' : 'explore the menu',
            }
        },
        {
          id : 1,
          img : '/img/sushi-2.png',
          title : 'perfect for groups',
          txt : 'sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn' : 'make a reservation',
            }
        },
        {
          id : 2,
          img : '/img/sushi-3.png',
          title : 'fresh product everyday',
          txt : 'sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn' : 'learn more about us',
            }
        },
      ],
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/animationEasterEgg.scss';
.img-container{
  min-height: 700px;
  height: 100%;
  transition: all 0.5s;
  z-index: 2;
  img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
  .txt-absolute{
    bottom: 12px;
    left: 40%;
    color: var(--txt-white);
    font-weight: 700;
    font-size: 0.8rem;
  }
  &:hover{
    transform: scale(1.05);
  }
}
.txt-container{
  line-height: 1.8;
  font-size: 1.2rem;
}
.title-lg{
  font-size: 2.6rem;
  font-weight: 700;
  line-height: 1.5;
  cursor: pointer;
}
.title-smartphone{
  font-size: 1.4rem;
  cursor: pointer;
}
.col-6 > img{
  width: 100%;
}


</style>