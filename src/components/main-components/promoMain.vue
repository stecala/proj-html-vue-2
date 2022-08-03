<template>
  <div class="container-lg mt-5 pt-lg-5 px-5 px-lg-0">
    <div class="row">
        <div class="col-12 col-lg-6">
            <div class="row px-lg-5">
                <div class="col-12 pt-lg-5">
                  <span class="txt-container">
                    <strong class="text-uppercase">hac tellus, felis risus at </strong>mattis mattis. Eget euismod sempere eget tortor, donec amet, blandit. 
                    Tristique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis facilisis amet vulputate.
                  </span>
                </div>
            </div>
        </div>
        <div class="d-none d-lg-block col-lg-6">
            <div class="img-container position-relative">
                <img src="/img/info22x.jpg" alt="california roll">
                <div class="position-absolute txt-absolute">
                  <span class="text-uppercase">california roll $22</span>
                </div>
            </div>
        </div>
    </div>
  </div>   
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">

.img-container{
  height: 700px;
  transition: all 0.5s;
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
</style>