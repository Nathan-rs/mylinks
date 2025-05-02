<script setup>
import HeaderContent from '@/components/HeaderContent.vue';
import LinkShare from '@/components/LinkShare.vue';
</script>

<template>
    <div class="container">
        <div class="content">
            <header class="header">
                <HeaderContent />
            </header>

            <main class="contentLinks">
                <LinkShare />
            </main>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
}

.content {
    display: flex;
    flex-direction: column;
    width: 680px;
    min-height: 100vh;
    border: 1px solid #000;
    padding: 1rem;
    gap: 1rem;
}

@media (max-width: 468px) {
    .content {
        width: 100%;
        padding: 0;
    }
}
</style>