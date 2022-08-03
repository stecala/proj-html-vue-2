<template>
  <div class="container-lg mt-5">
        <div class="col-12 col-lg-6">

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
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.img-container{
  height: 700px;
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
}
</style>