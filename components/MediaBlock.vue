<template>
    <div v-for="media in array" :key="media.id" class="media-item">
        <div class="background-pic" :style="{backgroundImage:`url(${media.pic})`}"></div>
        <div class="media-elements column">
            <div class="text-wrapper column">
                <h3 class="media-title">
                    <span class="first-line">{{ media.subtitle }}</span><br>
                    {{ media.title }}
                </h3>
                <p>{{ media.text }}</p>
            </div>
            <Button :text="media.btn_text"/>
        </div>
    </div>
</template>
<script setup>
    const props = defineProps ({
        array: {
            type: Array,
            required: true
        }
    })
</script>
<style>

    .media-item{
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 40px;
        margin-bottom: 20px;
    }

    .background-pic{
        min-width: 390px;
        height: 390px;
        border-radius: 20px;
        background-color: rgba(209, 209, 209, 0.44);
        background-repeat: no-repeat;
        background-size:60% auto;
        aspect-ratio: 1 / 1;
        background-position: center;
    }

    .media-elements {
        gap: 20px;
        align-items: start;
    }

    .text-wrapper{
        gap: 15px;
    }

    .media-title{
        font-size: 28px;
        line-height: 34px;
    }
    .first-line{
        color: var(--text-gray);
        font-size: 18px;
    }

    .media-item:nth-child(2n){
        flex-direction: row-reverse;
    }

    @media screen and (max-width: 706px) {

        .media-item{
            flex-direction: column;
            gap: 15px
        }

        .media-item:nth-child(2n){
            flex-direction: column;
        }

        .background-pic{
            width: 100% ;
            background-size:40% auto;
        }

    }

    @media screen and (max-width: 430px) {
        
        .text-wrapper p{
            font-size: 18px;
            line-height: 23px;
        }

        .background-pic{
            height: 275px;
            min-width: 0px;
            background-size:50% auto;
        }
    }
</style>