<script>
export default {
    data() {
        return {
            bannerList: [
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
                    text: 'SUBSCRIPTION'
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <div class="small-container">
            <ul>
                <li v-for="item in bannerList" :key="item.text">
                    <a href="">
                        <img :src="getImagePath(item.img)" alt="">{{ item.text }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.banner {
    min-height: 100px;
    background-color: $banner-bg-color;

    ul {
        @include flex();
        padding: 2rem 0;
        gap: 1rem;
 
        a {
            @include flex();
            gap: .7rem;
            color: $white;
            font-size: .7rem;

            img {
                width: 30px;
            }
        }
    }
}
</style>