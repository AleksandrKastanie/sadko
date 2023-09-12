<template>
    <div class="store-grid">
        <div class="column product-cell">
            <img src="/pictures/products/pro7/2313-Black-pro7-2s.webp" alt="prod_photo" class="store-grid-pic">
            <div class="text-wrapper column">
                <p class="store-grid-text">something bla blab lalorem lorem lsaldasof</p>
                <Button text="Read more" />
            </div>
        </div>
    </div>
</template>
<script setup>

</script>
<style>

    .store-grid{
        display: grid; 
        grid-template-columns: repeat(3, 1fr); 
        grid-template-rows: 1fr; 
        grid-column-gap: 14.5px;
        grid-row-gap: 10px;
    }

    .store-grid-pic{
        height: 100%;
        width: 100%;
        border-radius: 20px;
    }

    .product-cell{
        gap: 15px;
    }
    
    .text-wrapper{
        gap: 5px;
    }


    

</style>