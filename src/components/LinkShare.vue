<script setup>

import logo from '@/assets/icons/logo.svg'

import 'primeicons/primeicons.css'

const links = [
    {
        id: 0,
        name: 'Portfolio',
        url: 'https://nathan-rs.github.io/portfolio/',
        iconSVG: logo,
        iconClass: ''
    },
    {
        id: 1,
        name: 'Github',
        url: 'https://github.com/Nathan-rs',
        iconSVG: '',
        iconClass: 'pi pi-github'
    },
    {
        id: 2,
        name: 'Linkedin',
        url: 'https://www.linkedin.com/in/nataramos/',
        iconSVG: '',
        iconClass: 'pi pi-linkedin'
    },
    {
        id: 3,
        name: 'Instagram',
        url: 'https://www.instagram.com/natthan_rs/',
        iconSVG: '',
        iconClass: 'pi pi-instagram'
    },
    {
        id: 4,
        name: 'Threads',
        url: 'https://www.threads.com/@natthan_rs',
        iconSVG: '',
        iconClass: 'pi pi-hashtag'
    }
]

</script>

<template>
    <div class="linkShare">
        <ul class="listLinks">
            <li v-for="link in links" :key="link.id" class="itemLink">
                <div class="contentLink">
                    <a class="linkClick" :href="link.url" target="_blank" rel="noopener noreferrer">
                        <div class="icon">
                            <img v-if="link.iconSVG" :src="link.iconSVG" width="16" height="16" alt="icon" />
                            <i v-else :class="`${link.iconClass}`"></i>
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