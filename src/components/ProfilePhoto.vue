<script setup>
import photo from '@/assets/images/profile.jpg'
</script>

<template>
    <div class="card-photo">
        <span class="photo">
            <img :src="photo" alt="">
        </span>
    </div>
</template>

<style scoped>

.card-photo {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    border-radius: 12px;
    border: 1px solid #fff;
}

.photo {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    border: 1px solid #fff;
    /* padding: 1rem; */
}

.photo img {
    width: 7rem;
    height: 7rem;
    border-radius: 50%;
    object-fit: cover;
    object-position: center
}

@media (max-width: 468px) {
    .photo-profile img {
        width: 8rem;
        height: 8rem;
    }

    /* .photo {} */
}
</style>