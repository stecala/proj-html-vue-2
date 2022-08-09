<template>
  <div class="container-lg">
      <!-- Mobile -->
      <div class="row d-lg-none">
        <div class="col-12">
          <reviewCardSmallMain v-for="card in infoReviewForCards" :key="card.id" :class="{'d-none d-lg-block' : card.id != currentID }" :card="card" />
        </div>
      </div>
      <!-- LG -->
      <div class="row">
        <reviewCardMain />
      </div>
  </div>
</template>

<script>
import reviewCardMain from './reviewCardMain.vue'
import reviewCardSmallMain from './reviewCardSmallMain.vue'
export default {
  data : function (){
    return{
      infoReviewForCards : [
        {
          id : 0,
          name : 'meggy stewart',
          journal : 'new york times',
          img : '/img/blog72x-1200x1375.jpg',
          stars : 5,
          txt : {
            paragraph1 : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt, id sapien accumsai, sed at.' ,
            paragraph2 : 'Mmalesuada ullamcorper amet. Pretium pretium dignissim nisi.'
          },
          btn : {
            url : '#',
            txt_btn : 'read full article'
          }
        },
        {
          id : 1,
          reviewer : 'mary maxey',
          journal : 'the guardian',
          img : '/img/info52x.jpg',
          stars :  5,
          txt : {
            paragraph1 : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt id sapien accumsan sed.',
            paragraph2 : ''
            },
          btn : {
            url : '#',
            txt_btn : 'read full article'
          } 
        },
        {
          id : 2,
          reviewer : 'patrick monroe',
          journal : 'globe and mail',
          img : '/img/info12x.jpg',
          stars :  5,
          txt : {
            paragraph1 : 'Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Nulla porttitor accumsan tincidunt.',
            paragraph2 : ''
            },
          btn : {
            url : '#',
            txt_btn : 'read full article'
          } 
        },
      ], 
      currentID : 0,
    }
  },
  components : {
    reviewCardMain,
    reviewCardSmallMain,
  },
  methods : {

  },
}
</script>

<style>

</style>