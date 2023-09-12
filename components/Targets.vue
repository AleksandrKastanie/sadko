<template>
    <section class="container targets-wrapper column">
        <h2 class="title">Social commitment<br>
        <span class="second-line">With SadkoNewLife</span></h2>
        <div class="targets center">
            <div class="target column">
                <img class="target-icon" src="/icons/lang.svg" alt="icon"/>
                <div class="text-group column">
                    <h3 class="target-title">Social commitment</h3>
                    <p class="target-info">Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah</p>
                </div>
            </div>
            <div class="target column">
                <img class="target-icon" src="/icons/lang.svg" alt="icon"/>
                <div class="text-group column">
                    <h3 class="target-title">Social commitment</h3>
                    <p class="target-info">Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah</p>
                </div>
            </div>
            <div class="target column">
                <img class="target-icon" src="/icons/lang.svg" alt="icon"/>
                <div class="text-group column">
                    <h3 class="target-title">Social commitment</h3>
                    <p class="target-info">Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah</p>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>

</script>
<style>

    .targets-wrapper{
        margin-top: 54px !important;
        padding: var(--safe-zone);
        gap: 24px;
    }

    .targets{
        background-color: var(--block-background);
        border-radius: 20px;
        padding: 20px;
        gap: 25px;
    }

    .target{
        gap: 15px;
    }
    
    .target-icon{
        height: 20px;
        width: 20px;
    }

    .text-group{
        gap:10px;
    }

    .text-group h3{
        font-size: 20px;
        line-height:24.38px;
    }

    .text-group p{
        color: var(--text-gray);
        font-size: 14px;
        line-height: 21px;
    }
    
    @media screen and (max-width:870px ) {

        .targets{
            flex-direction: column;
        }
        
    }

    @media screen and (max-width: 768px) {

        .text-group h3{
            font-size: 22px;
            line-height:29px;
        }

        .text-group p{
            font-size: 18px;
            line-height: 22px;
        }
    }

</style>