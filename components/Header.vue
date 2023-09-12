<template>
    <header>
        <div class="header-container center">
            <img src="/pictures/logo.png" alt="logo" class="logo">
            <img :src=icon class="menu-btn" alt="menu" @click="toggleMenu"/>
            <transition name="standard">
                <nav v-if="isOpened && isMobile" class="menu">
                    <p class="section-name">Menu</p>
                    <nuxt-link to="/products" class="nav-link-mob">Products</nuxt-link>
                    <a href="#" class="nav-link-mob">About us</a>
                    <a href="#" class="nav-link-mob">Contacts</a>
                    <p v-if="true"
                    class="section-name">Language</p>
                    <div v-if="true" class="select-wrapper">
                        <p>English</p>
                        <img src="/icons/Ellipse.svg" />
                        <p style="color: gray;">Eesti</p>
                    </div>
                </nav> 
            </transition>
            <div class="right-header-wrapper ">
                <div class="nav-links center">
                    <nuxt-link to="/products" class="nav-link">Products</nuxt-link>
                    <a href="/" class="nav-link">About us</a>
                    <a href="/" class="nav-link">Contacts</a>
                </div>
                <div class="lng-wrapper">
                    <img src="/icons/lang.svg" alt="language" class="lng-btn" />
                    <ul class="lng-list">
                        <a href="/" class="lng-line"><li class="lng">ET</li></a>
                        <a href="/" class="lng-line"><li class="lng">ET</li></a>
                        <a href="/" class="lng-line"><li class="lng">ET</li></a>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<script setup>
    let isOpened = useState('menuOpened', () => false)
    let isMobile = useState('menuMobile', () => false)
    let icon = useState('iconChanged', () => "/icons/menu.svg")

    function resizeBrowser() {
        isMobile.value = window.innerWidth <= 768;
        if (!isMobile.value && isOpened.value) {
            isOpened.value = false;
            document.body.style.overflow = 'auto';
            symbolChange();
        }
    }

    function toggleMenu() {
        isOpened.value = !isOpened.value;
        isOpened.value ? document.body.style.overflow = 'hidden' : document.body.style.overflow = 'auto';
        symbolChange();
    }

    function symbolChange() {
        if (isOpened.value) {
            icon.value = "/icons/cross.svg";
        }
        else {
            icon.value = "/icons/menu.svg";
        }
    }

    onMounted(() => {
        resizeBrowser()
        window.addEventListener('resize', resizeBrowser);
    })

    onUnmounted(() => {
         window.removeEventListener('resize', resizeBrowser);
    })
</script>
<style>
    .logo{
        height: 40px;
        width: 124px;
    }

    header{
        height: var(--header-height);
        display: flex;
        width:100%;
        align-items: center;
        justify-content: space-between;
        padding: var(--safe-zone);
    }
    
    .right-header-wrapper{
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    .nav-links{
        gap: 40px;
    }

    .nav-link{
    position: relative;
    justify-content: center;
    border-radius: 5px;
    background: linear-gradient(to left, var(--bg) 50%, var(--accent) 50%) right;
    background-size: 200%;
    height: calc(100% + 10px);
    width: 90px;
    text-align: center;
    transition: background-position 0.35s;
    }

    .nav-link:hover {
        background-position: left;
        color: white;
    }

    .lng-btn{
        padding-left: 20px;
        border-left: 2px solid grey;
        cursor: pointer;
    }

    .menu {
        background-color: rgba(246, 246, 246, 0.679);
        backdrop-filter: blur(17.5px);
        left: 0;
        position: absolute;
        z-index: 999;
        bottom: 0;
        display: flex;
        flex-direction: column;
        gap: 25px;
        padding: 30px 40px;
        width: 100%;
        height: calc(100vh - 80px);
        overflow-y: scroll;
        top: 80px;
    }

    .lng-list{
        display: none 
    }

    .lng{
        list-style: none;
        align-self: center;
    }

    .lng-line{
        position: relative;
        padding-top: 5px;
        padding-bottom: 5px;
        width: 100%;
    }

    .lng-wrapper:hover  .lng-list{
        display: flex !important;
        flex-direction: column;
        position: absolute;
        background-color: white;
        width: 80px;
        height: 100px;
        align-items: center;
        right: 10px;
        bottom: 190px;
        top: 55px;
        border-radius: 15px;
        z-index: 998;
    }

    .lng-line:hover{
        background-color: grey;
        display: flex;
    }
    
    .nav-link-mob{
        font-weight: 800;
        font-size: 30px;
        line-height: 36.5px;
        display: flex;
        gap: 5px;
        z-index: 998;
    }

    .section-name {
        color: var(--accent);
        font-size: 16px;
        line-height: 19.5px;
        font-weight: 700;
    }

    .select-wrapper p {
        font-size: 20px;
        line-height: 24px;
    }

    .select-wrapper {
        display: flex;
        gap: 17px;
        font-weight: 700;
    }

    .menu-btn {
        cursor: pointer;
        left: 90%;
        display: none;
    }

    @media screen and (max-width: 768px) {

        .right-header-wrapper{
            display: none;
        }

        .menu-btn{
            display: flex !important;
        }

    }

</style>