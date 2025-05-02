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
    // {
    //     id: 6,
    //     name: 'Twitch',
    //     url: 'link://link.com.br/twitch'
    // },
    // {
    //     id: 7,
    //     name: 'Discord',
    //     url: 'link://link.com.br/discord'
    // },
    // {
    //     id: 8,
    //     name: 'Telegram',
    //     url: 'link://link.com.br/telegram'
    // },
    // {
    //     id: 9,
    //     name: 'WhatsApp',
    //     url: 'link://link.com.br/whatsapp'
    // },
    // {
    //     id: 10,
    //     name: 'Email',
    //     url: 'link://link.com.br/email'
    // },
    // {
    //     id: 11,
    //     name: 'Youtube',
    //     url: 'link://link.com.br/youtube'
    // },
    // {
    //     id: 12,
    //     name: 'TikTok',
    //     url: 'link://link.com.br/tiktok'
    // },
    // {
    //     id: 13,
    //     name: 'Snapchat',
    //     url: 'link://link.com.br/snapchat'
    // },
    // {
    //     id: 14,
    //     name: 'Pinterest',
    //     url: 'link://link.com.br/pinterest'
    // },
    // {
    //     id: 15,
    //     name: 'Reddit',
    //     url: 'link://link.com.br/reddit'
    // },
    // {
    //     id: 16,
    //     name: 'Tumblr',
    //     url: 'link://link.com'
    // }
]

</script>

<template>
    <div class="link-share">
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
/* .link-share {
    height: 100%;
    margin-top: 1rem;
}

.list-links {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.item-link {
    flex: 1;
}

.link {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    color: #eee;
    font-size: 1.2rem;
    background-color: #213448;
    font-weight: bold;
    padding: .625rem;
    cursor: pointer;
    border-radius: 10px;
    transition: background-color 0.3s ease;

}

.link:hover {
    background-color: #2b3c5a;
} */

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
    gap: 1rem;
}

.itemLink {
}

.contentLink {
    /* display: flex; */
}

.linkClick {
    display: flex;
    align-items: center;
    /* justify-content: center; */
    gap: 1rem;
    padding: 1rem;
    text-align: center;
    background-color: #213448;
    border-radius: 8px;
}

.label {
    flex: 1;
}
</style>