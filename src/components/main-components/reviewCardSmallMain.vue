<template>
  <div class="row ">
    <div class="col-12 img-container position-relative">
        <img :src="card.img" alt="background image">
        <div class="gradient mx-auto"></div>
    </div>
  </div>
</template>

<script>
export default {
    props : {
        card : Object,
    }
}
</script>

<style scoped lang="scss">
.img-container{
    width: 100%;
    img{
        width: 100%;
    }
}
.gradient{
    position: absolute;
    top: 0;
    left: 12px;
    width: calc(100% - 24px);
    height: 100%;
    background-image: linear-gradient(rgba(0, 0, 0, 0.83), rgba(0, 0, 0, 0.342));
}
</style>