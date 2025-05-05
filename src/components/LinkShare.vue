<script setup>

import 'primeicons/primeicons.css'

const links = [
    {
        id: 1,
        name: 'Github',
        url: 'link://link.com.br/github',
        iconClass: 'pi pi-github'
    },
    {
        id: 2,
        name: 'Linkedin',
        url: 'link://link.com.br/linkedin',
        iconClass: 'pi pi-linkedin'
    },
    {
        id: 3,
        name: 'Instagram',
        url: 'link://link.com.br/instagram',
        iconClass: 'pi pi-instagram'
    },
    {
        id: 4,
        name: 'Facebook',
        url: 'link://link.com.br/facebook',
        iconClass: 'pi pi-facebook'
    },
    {
        id: 5,
        name: 'Twitter',
        url: 'link://link.com.br/twitter',
        iconClass: 'pi pi-twitter'
    },
]

</script>

<template>
    <div class="linkShare">
        <ul class="listLinks">
            <li v-for="link in links" :key="link.id" class="itemLink">
                <div class="contentLink">
                    <a class="linkClick" :href="link.url" target="_blank" rel="noopener noreferrer">
                        <div class="icon">
                            <i :class="`${link.iconClass}`"></i>
                        </div>

                        <div class="label">{{ link.name }}</div>
                    </a>
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
a,
ul,
li {
    text-decoration: none;
    list-style: none;
    padding: 0;
    margin: 0;
    color: #eee;
}

.listLinks {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 1rem;
    padding-left: 1rem;
    padding-right: 1rem;
}

.linkShare {
    width: 100%;
}

.linkClick {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem;
    text-align: center;
    background-color: #474E93;
    border-radius: 48px;
}

.label {
    flex: 1;
}
</style>