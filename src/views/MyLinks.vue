<script setup>
import HeaderContent from '@/components/HeaderContent.vue'
import LinkShare from '../components/LinkShare.vue';
</script>

<template>
    <div class="container">
        <div class="content">
            <main class="contentLinks">
                <div class="contentLinksComponents">
                    <HeaderContent />
                    <!-- <LinkShare /> -->
                </div>
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
}

.content {
    /* display: flex; */
    /* flex-direction: column; */
    width: 580px;
    min-height: 100vh;
    padding-top: .5rem;
    padding-bottom: .5rem;
    /* border: 1px solid blue; */
    /* position: relative; */
    /* min-height: 100vh; */
}

.contentLinks {
    /* display: flex; */
    /* width: 580px; */
    /* position: absolute; */
    /* margin-top: 4rem; */
}

@media (max-width: 468px) {
    .content {
        width: 100%;
        padding: 0;
    }
}
</style>