<template>
<section class="intro-section">
    <div class="intro-img header-container">
        <div class="intro-elem-wrapper">
            <div class="intro-text-wrapper">
                <h1>SadkoNewLife</h1>
                <p>Advanced health tech systems. Hardware and sofltware solutions to power your employes’ health.</p>
            </div>
            <Button  text="Contact us"/>
        </div>
    </div>
</section>
</template>
<script setup>
</script>
<style>
    
    .intro-section{
        padding: var(--safe-zone);
    }

    .intro-img{
        display: flex;
        align-items: center;
        filter: drop-shadow(1px 4px 15px rgba(48, 48, 48, 0.25));
        background-image:   linear-gradient(90deg, rgba(27, 27, 27, 0.56) 0%, rgba(27, 27, 27, 0) 35%), url("/pictures/intro-img.png");
        height: calc(95svh - 80px);
        min-height: 600px;
        border-radius: 20px;
        color: white;
        background-size:cover;
    }

    .intro-elem-wrapper{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding-left: 73px;
        gap: 16px; 
        width: 483px;
    }

    .intro-elem-wrapper h1{
        font-size: 64px;
        line-height: 78px;
        font-weight: 700;
    }

    .intro-elem-wrapper p{
        font-weight: 500;
        font-size: 20px;
        line-height: 28px;
    }

    @media screen and (max-width: 1210px){

        .intro-img{
            background-position: center;
        }

    }

    @media screen and (max-width: 768px) {
        
        .intro-section{
            padding: 0px;
        }

        .intro-elem-wrapper h1{
            font-size: 55px;
            line-height: 67px;
            font-weight: 700;
        }

        .intro-img{
            background-image:   linear-gradient(90deg, rgba(27, 27, 27, 0.56) 0%, rgba(27, 27, 27, 0) 70%), url("/pictures/intro-img.png");
            background-position: 90% 50%;
            border-radius: 0px;
            min-height: 0px;
            height: calc(100svh - 80px);
        }

        .intro-elem-wrapper{
            width: 400px;
        }

        .intro-elem-wrapper p{
            font-size: 18px;
        }

    }

    @media screen and (max-width: 565px) {
        
        .intro-elem-wrapper{
            width: 100%;
            padding: 20px;
            gap: 20px;
            justify-content: flex-end;
            height: 100%;
        }

        .intro-elem-wrapper h1{
            font-size: 40px;
            line-height: 47px;
        }

        .intro-text-wrapper{
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .intro-elem-wrapper p{
            font-size: 18px;
            line-height: 23px;
        }

        .intro-img{
            background-position: 80% 50%;
        }

    }

    @media screen and (max-width: 406px) {
        
        .intro-elem-wrapper h1{
            font-size: 30px;
            line-height: 39px;
        }

        .intro-elem-wrapper p{
            font-size: 16px;
            line-height: 21px;
        }

        .intro-img{
            background-position: 70% 50%;
            background-image:   linear-gradient(0deg, rgba(27, 27, 27, 0.56) 0%, rgba(27, 27, 27, 0) 70%), url("/pictures/intro-img.png");
        }

    }

    @media screen and (max-width: 320px) {
        
        .intro-elem-wrapper p{
            font-size: 14px;
            line-height: 19px;
        }
    }
    

</style>