<template >
    <section class="prod-intro">
        <div class="prod-panel">
            <button v-for="(product, index) in products" :key="index" @click="showProduct(index)"  :class="{'prod-btn': true, 'tab-active': index === productIndex }">
                {{ product.name }}
            </button>
        </div>
        <transition name="fade" mode="out-in">
            <ProductsIntroGrid :key="productIndex"
            :object="products[productIndex]"/>
        </transition>
    </section>
</template>
<script setup>
    let productIndex = ref(0);
    const products = [
        {
            id:1,
            name:"Bike",
            bigpic:"/pictures/products/bike.webp",
            smallpic:"/pictures/products/bike.webp",
            text:"bla-bal vldsald-  dsldasdlsf2 dsdadqd lorem!!!"
        },
        {
            id:2,
            name:"Pro 7",
            bigpic:"/pictures/products/pro7/2313-Black-pro7-2s.webp",
            smallpic:"/pictures/products/pro7/2313-Black-pro7-2s.webp",
            text:"bla-bal vldsald-  dsldasdlsf2 dsdadqd lorem!!!"
        },
        {
            id:3,
            name: "Pulse",
            bigpic:"/pictures/products/pulse/IMG_9677_4ad1acc3-b239-414f-a897-d7f0fb752524.webp",
            smallpic:"/pictures/products/pulse/IMG_9677_4ad1acc3-b239-414f-a897-d7f0fb752524.webp",
            text:"bla-bal vldsald-  dsldasdlsf2 dsdadqd lorem!!!"
        }
    ]

    function showProduct(index){
        productIndex.value = index
    }
</script>
<style>

    .prod-btn{
        border-style: none;
        cursor: pointer;
        border-radius: 20px;
        padding: 10px 15px;
        font-size: 20px;
        background-color: white;
        color:rgba(0, 0, 0, 0.472);
        transition: background-color 0.4s;
    } 
    
    .prod-btn:hover {
        background-color: rgba(143, 135, 135, 0.554);
        color: black;
    }

    .tab-active {
        background-color: var(--accent);
        color: white;
    }

    .prod-panel{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 30px;
        margin: 10px 0px;
    }

    .prod-intro{
        padding: var(--safe-zone);
    }

    
</style>