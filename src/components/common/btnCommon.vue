<template>
    <div :class="isWhite ? 'my-btn-white' : 'my-btn-dark'" class="mt-5">
        <a :href="infoForBtn.url">
            {{infoForBtn.txt_btn}}
        </a>
    </div>
</template>

<script>
export default {
    props :{
        infoForBtn : Object,
        isWhite : Boolean,
    },
   
}
</script>

<style>

</style>