<template>
  <div class="col-12 col-lg-4 p-4">
    <div class="row">
        <div class="col-6 mx-auto d-flex justify-content-center">
            <img :src="card.img" alt="sushi">
        </div>
        <div class="col-12 mt-5 justify-content-center title d-flex align-items-center">
            <span class="text-uppercase text-center">
                {{card.title}}
            </span>
        </div>
        <div class="col-2 mx-auto divider mt-5"></div>
        <div class="col-12 mt-5 text-center">
            <span>
                {{card.txt}}
            </span>
        </div>
        <div class="col-12">
            <btnCommon :isWhite="isWhite" :infoForBtn="card.btn" />
        </div>
    </div>
  </div>
</template>

<script>
import btnCommon from '../common/btnCommon.vue'
export default {
    props :{
        card : Object,
        isWhite : Boolean,
    },
    components : {
        btnCommon,
    }
}
</script>

<style scoped>
.col-6>img{
    width: 100%;
    max-width: 146px;
}
.title{
    font-weight: 700;
    font-size: 1.4rem;
    min-height: 68px;
}

</style>
