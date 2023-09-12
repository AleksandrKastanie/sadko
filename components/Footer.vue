<template>
    <footer>
        <section class="footer-grid container">
            <div class="first-column column">
                <h3 class="footer-title">Contacts</h3>
                <a href="#" class="footer-link">SomeLink</a>
                <a href="#" class="footer-link">SomeLink</a>
            </div>
            <div class="second-column column">
                <h3 class="footer-title">Help</h3>
                <a href="#" class="footer-link">SomeLink</a>
                <a href="#" class="footer-link">SomeLink</a>
            </div>
            <div class="third-column column">
                <h3 class="footer-title">Social media</h3>
                <a href="#" class="footer-link">SomeLink</a>
                <a href="#" class="footer-link">SomeLink</a>
            </div>
        </section>
    </footer>
</template>
<script setup>

</script>
<style>

    footer{
        margin-top: 54px;
    }
    
    .footer-grid{
        padding: var(--safe-zone);
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: 1fr;
        grid-column-gap: 15px;
        grid-row-gap: 15px;

        
    }
    .footer-grid a{
        font-weight: 300;
    }

    .first-column{
        grid-area: 1 / 1 / 2 / 2;
        gap: 30px;
        justify-content: space-around;
        padding-bottom: 30px;
    }

    .second-column{
        grid-area: 1 / 2 / 2 / 3;
        gap: 30px;
        justify-content: space-around;
        padding-bottom: 30px;
    }

    .third-column{
        grid-area: 1 / 3 / 2 / 4;
        gap: 30px;
        justify-content: space-around;
        padding-bottom: 30px;
    }

    .footer-link{
        font-size: 15px;
    }
</style>