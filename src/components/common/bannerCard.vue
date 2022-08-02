<template>
    <div>
        <div class="row">
            <div class="col-12">
                <span class="subtitle text-uppercase position-relative">
                    {{infoForCard.subtitle}}
                </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props : {
        infoForCard : Object,
    }
}
</script>

<style scoped lang="scss">
    .subtitle{
        font-family: 'Catamaran', sans-serif;
        &::before{
            content: '';
            position: absolute;
            top: 50%;
            left: - 90px;
            background-color: var(--txt-white);
            height: 1px;
            width: 50px;
        }
    }
</style>