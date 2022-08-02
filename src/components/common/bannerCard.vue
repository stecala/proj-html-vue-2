<template>
    <div>
        <div class="row">
            <div class="col-12">
                <span class="subtitle text-uppercase position-relative">
                    {{infoForCard.subtitle}}
                </span>
            </div>
            <div class="col-12 mt-4">
                <span class="title text-uppercase">
                    {{infoForCard.title}}
                </span>
            </div>
            <div class="col-12 mt-4">
                <span class="description">
                    {{infoForCard.text}}
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
    .title{
        font-size: 3.7rem;
        line-height: 1.5;
        font-weight: 700;
    }
    .description{
        font-size: 1.2rem;
        line-height: 1.7;
        font-family: 'Ibarra Real Nova', serif;
    }
</style>