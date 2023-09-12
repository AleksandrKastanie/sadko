<template>
    <button class="btn"
    ref="mainBtn">
        {{ props.text }} 
        <img v-if="props.pic" :src="props.pic" alt="btn-picture">
    </button>
</template>
<script setup>
    const mainBtn = ref(null);
    const props = defineProps({
        text: {
            type: String
        },
        pic: {
            type: String
        },
    })
</script>
<style>
    .btn{
        border-radius: 10px;
        border: none;
        background-color: var(--accent);
        padding: 10px 30px;
        color: white;
        display: flex;
        gap: 10px;
        font-size: 20px;
        font-weight: 700;
        text-align: center;
        align-items: center;
        cursor: pointer;
        font-family: 'Montserrat';
    }

    @media screen and (max-width: 565px) {
        
        .btn{
            width: 100%;
            justify-content: center;
            font-size: 18px;
            padding: 15px ;
        }
    
    }

    @media screen and (max-width: 406px) {

        .btn{
            font-size: 16px;
        }
    }

    @media screen and (max-width: 320px) {
        
        .btn{
            font-size: 14px;
        }
    }

</style>