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
                  <span class="title-lg d-none d-lg-block pe-lg-5 ">
                      food is our common ground, a universal experience.
                  </span>
                  <span class="d-lg-none title-smartphone ">
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
        <div class="d-none d-md-block col-md-6"  @click="startEasterEgg()">
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
  data : function(){
    return{
      counterEasterEgg : 0
    }
  },
  methods : {
    startEasterEgg(){
      this.counterEasterEgg++
    }
  }
}
</script>

<style scoped lang="scss">

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
}
.title-smartphone{
  font-size: 1.4rem;
}
.col-6 > img{
  width: 100%;
}

.animation-to-right{
  bottom: 30%;
  left: -10%;
  animation: movingRight linear infinite;
  animation-duration: 10s;
  z-index: -1;
  width: 100px;
  img{
    width: 100%;
    filter: grayscale(1);
  }

}
@keyframes movingRight{
  0% {bottom: 40%; left: -10%;}
  10%{bottom: 45%; left: 20%;}
  20%{bottom: 50%; left: 40%;}
  30%{bottom: 55%; left: 60%;}
  40%{bottom: 60%; left: 80%;}
  50%{bottom: 65%; left: 100%;}
  70%{bottom: 60%; left: 70%;}
  80%{bottom: 55%; left: 40%;}
  90%{bottom: 50%; left: 10%;}
  100%{bottom: 40%; left: -10%;}
}
.animation-to-left{
  top: 30%;
  right: 0;
  animation: movingLeft linear infinite;
  animation-duration: 15s;
  z-index: -1;
  width: 100px;
  img{
    width: 100%;
    filter: grayscale(1);
  }
}
@keyframes movingLeft{
  0% {top: 30%; right: 0;}
  10%{top: 25%; right: 20%;}
  20%{top: 20%; right: 40%;}
  30%{top: 15%; right: 60%;}
  40%{top: 10%; right: 80%;}
  50%{top: 15%; right: 100%;}
  70%{top: 20%; right: 70%;}
  80%{top: 25%; right: 40%;}
  90%{top: 30%; right: 10%;}
  100%{top: 30%; right: 0;}
}
</style>