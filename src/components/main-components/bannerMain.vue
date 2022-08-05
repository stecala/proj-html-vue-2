<template>
  <div class="mt-5 pt-lg-5 container-fluid">
    <div class="row">
        <div class="col-12 col-lg-7 img-banner">
        </div>
        <div class="col-5 d-none d-lg-block bg-black">
            <div class="row ">
                <div class="col-6 mx-auto mb-5 my-margin">
                    <bannerCard :infoForCard="infoForCard" />
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import bannerCard from '../common/bannerCard.vue'
export default {
    components : {
        bannerCard,
    },
    data : function(){
        return{
            infoForCard : {
                subtitle : 'fine dining experience',
                title : 'the best table in town',
                text : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga adipisci aut consequatur nam! Eius quas labore aperiam non.',
                btn : {
                    url : '#',
                    txt_btn : 'explore the menu' 
                }
            },
        }
    },
}
</script>

<style scoped lang="scss">
    .container-fluid{
        .img-banner{
            padding: 0;
            min-height: 350px;
            background-image: url('../../../public/img/slider32x.jpg');
            background-size: cover;
            background-position-y: 60%;
        }
    }
</style>