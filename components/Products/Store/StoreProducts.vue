<template>
    <section class="container store-section">
        <ProductsStoreGrid />
    </section>
</template>
<script setup >
    const storeProducts = [
        {
            id: 1,
            nameOfProduct:"Dual Sphere",
            storePic:"/pictures/products/dualsphere/DualSphere-isolated_black_2400px_1.webp",
            storeText:"Short store discription about product",
            fullDiscription:"Full Discription for this product",
            arrayOfPic:[
                {
                    id:1,
                    img:""
                }
            ]
        }
    ]
</script>
<style>
    .store-section{
        margin-top: 20px !important; 
    }
</style>