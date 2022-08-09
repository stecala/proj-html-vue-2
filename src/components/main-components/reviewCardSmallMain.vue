<template>
  <div class="row ">
    <div class="col-12 img-container position-relative">
        <img :src="card.img" alt="background image">
        <div class="gradient mx-auto"></div>
        <div class="row info-container position-absolute">
            <div class="col-12 name text-uppercase">
                <span>
                    {{card.name}}
                </span>
            </div>
            <div class="col-12 mt-4 mb-2">
                <span class="title text-uppercase">
                    {{card.journal}}
                </span>
            </div>
            <div class="col-12 mt-4">
                <div v-for=" number in card.stars" :key="number" class="d-inline-block me-2">
                    <i class="fa-solid fa-star"></i>
                </div>
            </div>
            <div class="col-2 divider mt-4 ms-3"></div>
            <div class="col-12 mt-2 text">
                <span>
                    {{card.txt.paragraph1}}<br>
                </span>
                <div class="spacer"></div>
                <span>
                    {{card.txt.paragraph2}}
                </span>
            </div>
            <div class="col-12">
                <btnCommon :isWhite="isWhite" :infoForBtn="card.btn" />
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import btnCommon from '../common/btnCommon.vue'
export default {
    props : {
        card : Object,
    },
    components : {
        btnCommon,
    },
    data : function() {
        return{
            isWhite : true,
        }
    }
}
</script>

<style scoped lang="scss">
.img-container{
    width: 100%;
    height: 700px;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
.gradient{
    position: absolute;
    top: 0;
    left: 12px;
    width: calc(100% - 24px);
    height: 100%;
    background-image: linear-gradient(rgb(0, 0, 0), rgba(0, 0, 0, 0.342));
    z-index: 0;
}
.info-container{
    padding: 70px;
    top: 0;
    left: 0;
    z-index: 1;
    color: var(--txt-white);
    .name{
        font-family: 'Catamaran', sans-serif;
        font-weight: 700;
    }
    .title{
        font-size: 2rem;
        line-height: 1.5;
        font-weight: 700;
        min-height: 123px;
    }
    .text{
        font-size: 1.2rem;
        min-height: 250px;
        .spacer{
            width: 100%;
            height: 20px;
        }
    }
}
</style>