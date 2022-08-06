<template>
  <div class="container-lg mt-5 pt-5 ">
    <div class="row">
        <div class="col-12 text-center">
            <span class="text-center title">
                {{txt_title}}
            </span>
        </div>
        <div class="col-1 divider mx-auto my-5"></div>
    </div>
  </div>
</template>

<script>
export default {
    props :{
       'txt_title' : String,
    }, 
}
</script>

<style scoped lang="scss">
.title{
    font-size: 1.8rem;
    font-family: 'Roboto Mono', monospace;
    font-style: italic;
    
}
</style>