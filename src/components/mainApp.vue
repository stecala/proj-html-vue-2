<template>
  <main>
    <promoMain />
    <bannerMain />
    <titleSection :txt_title="txt_title[0]" />
    <reviewMain />
  </main>
</template>

<script>
import promoMain from './main-components/promoMain.vue'
import bannerMain from './main-components/bannerMain.vue'
import titleSection from './common/titleSection.vue'
import reviewMain from './main-components/reviewMain.vue'

export default {
  components : {
    promoMain,
    bannerMain,
    titleSection,
    reviewMain,
  },
  data : function(){
    return{
      txt_title : ['What critics are saying about us' , 'Latest news & promotion']
    }
  },
}
</script>

<style scoped lang="scss">

</style>
