<script>
export default {
    data() {
        return {
            iconItems: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'SUBSCRIPTION'
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                },
            ],
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
};
</script>

<template>
    <main>
        <div class="container-main">
            <ul>
                <li v-for="icon in iconItems" :key="icon.text"><a href=""><img :src="getImagePath(icon.img)" alt="">{{ icon.text }}</a></li>
            </ul>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;

main {
    background-color: $primary;
    padding: 2rem 0;

    .container-main {
        width: 70%;
        margin: 0 auto;

        ul {
            @include flex();
            list-style: none;
            gap: 4rem;
            font-size: 0.8rem;

            a {
                @include flex();
                text-decoration: none;
                color: white;
                gap: 1rem;

                img {
                    width: 50px;
                }
            
            }
        }
    }
}
</style> 