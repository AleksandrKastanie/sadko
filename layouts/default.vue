<template>
    <Head>
        <Link rel="manifest"
         href="/site.webmanifest" />
    </Head>
    <Header />

    <slot />
    <Footer />
</template>


<style>
*,*::before,*::after{
    box-sizing: border-box;
    margin: 0px;
    padding: 0px;   
}

:root{
   --accent: #BF181C;
   --font: 'Montserrat' , sans-serif;
   --header-container: 1350px;
   --container: calc(960px + 1rem);
   --safe-zone:0px 40px;
   --bg: white;
   --header-height:80px;
   --text-gray:#757575;
   --block-background: #f1f2f3; 
}

@font-face {
    font-family: 'Montserrat';
    src: url("/fonts/Montserrat-Medium.ttf");
    font-weight: 500;
    font-style: normal;
}

@font-face {
    font-family: 'Montserrat';
    src: url("/fonts/Montserrat-Regular.ttf");
    font-weight: 400;
    font-style: normal;
}

@font-face {
    font-family: 'Montserrat';
    src: url("/fonts/Montserrat-SemiBold.ttf");
    font-weight: 600;
    font-style: normal;
}

@font-face {
    font-family: 'Montserrat';
    src: url("/fonts/Montserrat-Light.ttf");
    font-weight: 300;
    font-style: normal;
}

@font-face {
    font-family: 'Montserrat';
    src: url("/fonts/Montserrat-Bold.ttf");
    font-weight: 700;
    font-style: normal;
}

.standard-enter-active {
    animation: standard 0.2s;
}

.standard-leave-active {
    animation: standard 0.2s reverse;
}

@keyframes standard {
    0% {
        transform: translateY(-10px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

.fade-enter-active {
    animation: fade 0.2s;
}

.fade-leave-active {
    animation: fade 0.2s reverse;
}

@keyframes fade {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

body {
    font-family: var(--font);
    background-color: var(--bg);
}

.container{
    max-width: var(--container);
    width: 100%;
    margin: 0 auto;
}

.header-container {
    max-width: var(--header-container);
    width: 100%;    
    margin: 0 auto;
}

.flex{
    display: flex;
    align-items: center;
}

.center {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.column{
    display: flex;
    flex-direction: column;
}

a {
    text-decoration: none;
    color: black;
    display: flex;
    align-items: center;
    gap: 5px;
    font-weight: 600;
}

li { 
    list-style: none;
}
@media screen and (max-width: 768px) {
    :root{
        --safe-zone:0px 20px;
    }

}

@media screen and (max-width: 406px) {
    :root{
        --safe-zone:0px 10px
    }

}


</style>