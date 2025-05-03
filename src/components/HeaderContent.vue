<script setup>
import ProfilePhoto from '@/components/ProfilePhoto.vue'
import DescriptionProfile from '@/components/DescriptionProfile.vue'
import backgroundProfile from '@/assets/images/profile.jpg'
import imageProfile from '@/assets/images/profile.jpg'

const data = {
    name: 'Nathan Ramus',
    description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. ' +
        'Earum eligendi quasi inventore ipsa dolor repudiandae, nesciunt eius ducimus ipsum recusandae pariatur distinctio explicabo? ' +
        'Odio non error sint beatae qui expedita?',
    imageBackgroundProfile: `${backgroundProfile}`,
    imageProfile: `${imageProfile}`
}

console.log(data)

</script>

<template>

    <div class="headerContainer">
        <div class="backgroundImageProfile">
            <img :src="`${data.imageBackgroundProfile}`" alt="">
        </div>

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

    </div>

</template>

<style scoped>
.headerContainer {
    position: relative;
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
    /* border: 1px solid #fff; */
    position: absolute;
    bottom: 0;
}

.backgroundImageProfile img {
    display: block;
    max-width: 100%;
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

.apresentationProfile {
    width: 90%;
}

@media (max-width: 468px) {
    .imageProfile img {
        width: 8rem;
        height: 8rem;
    }
}
</style>