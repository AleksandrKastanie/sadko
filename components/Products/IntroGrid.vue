<template>
        <div class="grid-prod-intro">
            <div class="grid-bigpic"><img :src=object.bigpic class="big-pic" alt="pic1"></div>
            <div class="grid-smallpic"><img :src=object.smallpic class="small-pic" alt="pic2"></div>
            <div class="grid-text">
                <div class="grid-text-inner column">
                    <p>{{ object.text }}</p>
                    <Button 
                    text="Read more"/>
                </div>
            </div>
        </div>
</template>
<script setup>
    const props = defineProps ({
        object: {
            type: Object,
            required: true
        }
    })
</script>
<style>
    .grid-prod-intro{
        height: calc(95svh - 120px);
        width: 100%;
        display: grid;
        grid-template-columns: 3fr 2fr;
        grid-template-rows: repeat(2, 1fr);
        grid-column-gap: 20px;
        grid-row-gap: 20px;
    }

    .grid-text-inner{
        align-items: start;
        gap: 20px;
    }

    .grid-bigpic{
        grid-area: 1 / 1 / 3 / 2;
    }

    .grid-smallpic{
        
        grid-area: 1 / 2 / 2 / 3;
    }

    .grid-text{
        grid-area: 2 / 2 / 3 / 3;
    }

    .big-pic{
        width: 100%;
        height: 100%;
        border-radius: 20px;
    }

    .small-pic{
        height: 100%;
        width: 100%;
        border-radius: 20px;
    }
</style>