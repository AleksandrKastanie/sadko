<template>
    <section class="cards-section container">
        <h2 class="cards-title">Ready for life<br>
        <span class="second-line">With SadkoNewLife</span></h2>
        <CardsGrid :array="cards" />
    </section>
    <section class="cards-section container">
        <h2 class="title">Social commitment<br>
        <span class="second-line">With SadkoNewLife</span></h2>
        <CardsGrid :array="cards" />
    </section>
</template>
<script setup>
    const cards = [
        {
            id:1,
            pic: "/pictures/intro-img.png",
            title: "Help your family",
            text: "Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah"
        }, 

        {
            id:2,
            pic: "/pictures/intro-img.png",
            title: "Help your family",
            text: "Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah"
        },

        {
            id:3,
            pic: "/pictures/intro-img.png",
            title: "Help your family",
            text: "Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah. Lorem ipsum dolor sim amet blah blah blah"
        },
    ]
</script>
<style>
    .cards-section{
        margin-top: 54px !important;
        display: flex;
        flex-direction: column;
        gap: 24px;
        padding: var(--safe-zone);
    }

    .title{
        font-weight: 700;
        font-size: 24px;
        line-height: 28px;
    }
    .second-line{
        color: var(--text-gray)
    }

    @media screen and(max-width: 1055px) {

        .title{
            font-size: 30px;
            line-height: 34px;
        }
        
    }


    @media screen and(max-width: 750px) {

        .title{
            font-size: 38px;
            line-height: 42px;
        }
    }


</style>