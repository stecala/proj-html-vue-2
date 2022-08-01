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
:root{
  --dark : black;
  --txt-white : white;
  --dark-grey : #434243;
  --silver : #bcbcbc;
}
a{
  text-decoration: none;
}
</style>
