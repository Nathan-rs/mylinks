<script setup>
import imageProfile from '@/assets/images/profile.jpg'
// import backgroundProfile from '@/assets/images/Capa_Linkedin.png'
import backgroundProfile from '@/assets/images/profile.jpg'
import LinkShare from '@/components/LinkShare.vue'

const data = {
    name: 'Natã Ramos | dev',
    description: 'Desenvolvedor FullStack',
    imageBackgroundProfile: `${backgroundProfile}`,
    imageProfile: `${imageProfile}`
}

</script>

<template>
    <div class="headerContainer">
        <div class="backgroundImageProfile">
            <img :src="`${data.imageBackgroundProfile}`" alt="">
        </div>
        <div class="t1">
            <div class="informationProfile">
                <div class="imageProfile">
                    <img :src="`${data.imageProfile}`" alt="">
                </div>

                <div class="nameProfile">
                    <p class="title">{{ data.name }}</p>
                </div>

                <div class="apresentationProfile">
                    <p class="text">{{ data.description }}</p>
                </div>

                <div class="linksSocial">

                </div>
            </div>

            <div class="t2">
                <LinkShare />
            </div>
        </div>
    </div>
</template>

<style scoped>
.headerContainer {
    display: flex;
    min-height: 100%;
    flex-direction: column;
    position: relative;
}

.t1 {
    z-index: 50;
}

.t2 {
    padding-top: 2rem;
    padding-bottom: 2rem;
}

.title {
    color: #eee;
    font-size: 1.25rem;
    line-height: 1.75rem;
    font-weight: 700;
}

.text {
    color: #eee;
    font-size: .75rem;
    line-height: 150%;
    font-weight: 400;
    text-align: center;
}

.backgroundImageProfile {
    width: 100%;
    position: absolute;
    z-index: 10;
}

.backgroundImageProfile img {
    height: 100%;
    width: 100%;
    max-height: 320px;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
    opacity: .8;
    object-fit: cover;

    /* efeito fade-out */
    -webkit-mask-image: linear-gradient(to bottom, #303030 80%, transparent 100%);
    mask-image: linear-gradient(to bottom, #303030 70%, transparent 100%);
}

.imageProfile img {
    width: 6rem;
    height: 6rem;
    border-radius: 50%;
}

.informationProfile {
    display: flex;
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: .2rem;
    padding-left: 1rem;
    padding-right: 1rem;
    margin-top: 4rem;
    /* coloca a div na frente da div com a imagem */
    z-index: 50; 
}

.apresentationProfile {
    width: 90%;
}

@media (max-width: 600px) {
    .imageProfile img {
        width: 6rem;
        height: 6rem;
    }

    .informationProfile {
        margin-top: 7rem;
    }
}

</style>