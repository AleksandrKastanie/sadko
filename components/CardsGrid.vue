<template>
    <div class="grid-section"> 
        <div v-for="card in array" :key="card.id" class="card" :style="{backgroundImage: 'linear-gradient(0deg, rgba(27, 27, 27, 0.56) 0%, rgba(27, 27, 27, 0) 100%), ' + `url(${card.pic})`}">
            <h3>{{ card.title }}</h3>
            <div class="text-wrap"><p class="card-text">{{ card.text }}</p></div>
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
    .grid-section{
        display: grid; 
        grid-template-columns: repeat(3, 1fr); 
        grid-template-rows: 1fr; 
        grid-column-gap: 14.5px;
        grid-row-gap: 0px;

    }

    .card{
        display: flex;
        justify-content: flex-end;
        flex-direction: column;
        padding: 20px;
        gap: 0px;
        height: 275px;
        border-radius: 20px;
        background-size: cover;
        background-repeat: no-repeat;
    }

    .card h3{
        font-size: 20px;
        line-height:24.38px;
        color: white;
    }

    .card-text{
        font-size: 14px;
        line-height: 21px;
        color: white;
        min-height: 0px;
    }

    .text-wrap{
        display: grid;
        grid-template-rows: 0fr;
        overflow: hidden;
        transition: grid-template-rows 200ms;
    }

    .card:hover .text-wrap{
        grid-template-rows: 1fr;
    }

    .card:hover{
        gap: 8px;
    }

    @media screen and (max-width: 1055px) {
        
        .grid-section{
            grid-template-columns: repeat(2, 1fr);
            grid-row-gap: 15px;
        }

    }

    @media  screen and (max-width: 768px) {

        .card-text{
            font-size: 20px;
            line-height: 24px;
        }

        .card h3{
            font-size: 32px;
            line-height:38px;
        }
        
    }

    @media screen and (max-width: 750px) {

        .grid-section{
            grid-template-columns: repeat(1, 1fr);
        }
        
    }

    @media  screen and (max-width: 332px) {

        .card-text{
            font-size: 18px;
            line-height: 22px;
        }

        .card h3{
            font-size: 28px;
            line-height:33px;
        }

    }
</style>