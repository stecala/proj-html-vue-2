<template>
  <div class="col-12 col-lg-4">
    {{card.id}}
  </div>
</template>

<script>
export default {
    props :{
        card : Object,
    }
}
</script>

<style scoped>
    .col-12{
        height: 200px;
    }
</style>
