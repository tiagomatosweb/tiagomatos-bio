<template>
    <div>
        <Heading tag="h2">
            <span>Meus links</span>
            <span>🔗</span>
        </Heading>

        <div class="grid grid-cols-3 gap-2">
            <Card
                v-for="link in links"
                :key="link.label"
                tag="a"
                :href="link.href"
                target="_blank"
                class="flex flex-col md:flex-row items-center md:space-x-3 space-y-3 md:space-y-0 rounded-lg px-3 py-3"
            >
                <div class="flex-none flex items-center justify-center w-8 h-8">
                    <img
                        :src="link.img"
                        :alt="link.img_alt"
                    >
                </div>

                <div class="text-xs md:text-sm truncate">
                    {{ link.label }}
                </div>
            </Card>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'LinksBox',

        data() {
            return {
                links: [
                    { label: 'Instagram', img: require('@/assets/img/instagram.svg'), img_alt: 'Instagram @tiagomatosweb', href: 'https://www.instagram.com/tiagomatosweb/' },
                    { label: 'YouTube', img: require('@/assets/img/youtube.svg'), img_alt: 'Youtube /tiagomatosweb', href: 'https://www.youtube.com/tiagomatosweb?sub_confirmation=1' },
                    // { label: 'Face', img: require('@/assets/img/facebook-f.svg'), img_alt: 'Facebook /tiagomatosweb', href: 'https://www.facebook.com/tiagomatosweb' },
                    // { label: 'Blog', img: require('@/assets/img/laptop.svg'), img_alt: 'Blog blog.tiagomatos.com', href: 'https://blog.tiagomatos.com/' },
                    // { label: 'Site', img: require('@/assets/img/globe.svg'), img_alt: 'Site tiagomatos.com', href: 'https://tiagomatos.com/' },
                    { label: 'Discord', img: require('@/assets/img/discord.svg'), img_alt: 'Discord discord.tiagomatos.com', href: 'https://discord.gg/HXGwssB8S4' },
                ],
            };
        },

        methods: {},
    };
</script>
