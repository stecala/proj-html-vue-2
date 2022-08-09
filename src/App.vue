<template>
  <div>
    <headerApp />
    <mainApp />
    <footerApp />
  </div>
</template>

<script>
import headerApp from './components/headerApp.vue'
import mainApp from './components/mainApp.vue'
import footerApp from './components/footerApp.vue'

export default {
  components: {
    headerApp,
    mainApp,
    footerApp,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
// font-family: 'Catamaran', sans-serif;
@import url('https://fonts.googleapis.com/css2?family=Catamaran:wght@100;200;300;400;500;600;700;800;900&display=swap');
// font-family: 'Ibarra Real Nova', serif;
@import url('https://fonts.googleapis.com/css2?family=Ibarra+Real+Nova:ital,wght@0,400;0,500;1,400&display=swap');
// import btn
@import './assets/style/btn.scss';
// font-family: 'Roboto Mono', monospace;
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap');
:root{
  --dark : black;
  --txt-white : white;
  --dark-grey : #434243;
  --silver : #bcbcbc;
}
a{
  text-decoration: none;
}
.my-margin{
  margin-top: 120px;
}
.divider{
  height: 1px;
  background-color: var(--silver);  
}
</style>
