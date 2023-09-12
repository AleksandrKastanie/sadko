<template>
    <section class="media-group container column">
        <h2 class="title">Уникальные преимущества<br>
        <span class="second-line">Максимальная эффективность</span></h2>
        <MediaBlock :array="mediaitems" />
    </section>
</template>
<script setup>
    const mediaitems = [
        {
            id:1,
            pic:"/pictures/family.png",
            subtitle:"ВИБРАЦИЯ ВСЕГО ТЕЛА",
            title:"Power Plate",
            text:"Уникальные микро вибрации активируют больше мышц, сжигайте больше калорий, улучшите циркуляцию и помогайте мышцам восстановиться.",
            btn_text:"Something"
        },
        
        {
            id:2,
            pic:"/pictures/family.png",
            subtitle:"ВИБРАЦИЯ ВСЕГО ТЕЛА",
            title:"Power Plate",
            text:"Уникальные микро вибрации активируют больше мышц, сжигайте больше калорий, улучшите циркуляцию и помогайте мышцам восстановиться.",
            btn_text:"Something"
        }

    ]
</script>
<style>
    .media-group{
        margin-top: 54px !important;
        padding: var(--safe-zone);
        gap: 24px;
    }
</style>