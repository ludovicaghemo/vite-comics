<script>
    export default {
        data() {
            return {
                footerItems: [
                    {
                        footerTitle: "DC COMICS",
                    },
                    {
                        footerTitle: "DS",
                    },
                    {
                        footerTitle: "SITES",
                    },
                    {
                        footerTitle: "SHOP",
                    },
                ],
                comicsLinks: [
                    {
                        linkTitle: 'Characters',
                    },
                    {
                        linkTitle: 'Comics',
                    },
                    {
                        linkTitle: 'Movies',
                    },
                    {
                        linkTitle: 'TV',
                    },
                    {
                        linkTitle: 'Games',
                    },
                    {
                        linkTitle: 'News',
                    },
                ],
                dcLinks: [
                    {
                        linkTitle: 'Terms Of Use',
                    },
                    {
                        linkTitle: 'Privacy Policy (New)',
                    },
                    {
                        linkTitle: 'Ad Choices',
                    },
                    {
                        linkTitle: 'Advertising',
                    },
                    {
                        linkTitle: 'Jobs',
                    },
                    {
                        linkTitle: 'Subscriptions',
                    },
                    {
                        linkTitle: 'Talent Workshops',
                    },
                    {
                        linkTitle: 'CPSC Certificates',
                    },
                    {
                        linkTitle: 'Ratings',
                    },
                    {
                        linkTitle: 'Shop Help',
                    },
                    {
                        linkTitle: 'Contact Us',
                    },
                ],
                sitesLinks: [
                    {
                        linkTitle: 'DC',
                    },
                    {
                        linkTitle: 'MAD Magazine',
                    },
                    {
                        linkTitle: 'DC Kids',
                    },
                    {
                        linkTitle: 'DC Universe',
                    },
                    {
                        linkTitle: 'DC Power Visa',
                    },
                ],
                linksShop:[
                    {
                        linkTitle: 'Shop DC',
                    },
                    {
                        linkTitle: 'Shop DC Collectibles',
                    },
                ],
                footerImg: [
                    {
                        img: 'footer-facebook.png',
                    },
                    {
                        img: 'footer-twitter.png',
                    },
                    {
                        img: 'footer-twitter.png',
                    },
                    {
                        img: 'footer-youtube.png',
                    },
                    {
                        img: 'footer-pinterest.png',
                    },
                    {
                        img: 'footer-periscope.png',
                    },
                ],
            }
        },
        methods: {
            getImagePath: function(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            }
        },
    }
</script>

<template>
    <footer class="large-container">
        <!-- Footer Top -->
        <div class="footer-top">
            <div class="container">
                <img src="../assets/img/dc-logo-bg.png" alt="">
                <div class="footer-links">
                    <div class="footer-col">
                        <h5><strong>DC COMICS</strong></h5>
                        <ul>
                            <li v-for="item in comicsLinks" :key="item.linkTitle">
                                <a href="">{{ item.linkTitle }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h5><strong>DC</strong></h5>
                        <ul>
                            <li v-for="item in dcLinks" :key="item.linkTitle">
                                <a href="">{{ item.linkTitle }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h5><strong>SITES</strong></h5>
                        <ul>
                            <li v-for="item in sitesLinks" :key="item.linkTitle">
                                <a href="">{{ item.linkTitle }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h5><strong>SHOP</strong></h5>
                        <ul>
                            <li v-for="item in linksShop" :key="item.linkTitle">
                                <a href="">{{ item.linkTitle }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- /Footer Links -->
            </div>
            <!-- /Container -->
        </div>
        <!-- /Footer Top -->
        <!-- Footer Bottom -->
        <div class="footer-bottom large-container">
            <div class="container">
                <button>
                    <a href="">SIGN-UP NOW!</a>
                </button>
                <div class="follow">
                    <h4>Follow us</h4>
                    <div v-for="item in footerImg">
                        <a href="">
                            <img :src="getImagePath(item.img)" alt="">
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    min-height: 420px;

    .container {
        position: relative;
    }

    img {
        width: 440px;
        position: absolute;
        top: 0;
        right: 0px;
    }

    .footer-links {
        width: 80%;
        display: flex;
        gap: 1rem;
        padding: 2rem 0;
    }

    .footer-col {
        width: calc((50% / 3) - 1rem);
    }

    li {
        display: flex;
        padding: .2rem 0;
        font-size: .7rem;
        color: lightgray;
    }
}

.footer-bottom {
    @include flex();
    background-color: #303030;
    min-height: 100px;

    .container {
        @include flex();
    }
    
    .follow {
        @include flex();
        gap: 1rem;
    }
}
</style>