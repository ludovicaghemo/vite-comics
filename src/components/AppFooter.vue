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
                ]
            }
        }   
    }
</script>

<!-- <ul>
    <li class="d-flex flex-column" v-for="(link,index) in linksComics" :key="index">
        <a class="pt-1 link-color" :href="link.href">{{ link.title }}</a>
    </li>
</ul> -->

<template>
    <footer class="large-container">
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
        <div class="footer-bottom container">
            <h2>Footer Bottom</h2>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.footer-top {
    background-image: url(../assets/img/footer-bg.jpg);
    min-height: 400px;

    .container {
        position: relative;
    }

    img {
        width: 400px;
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
    z-index: 999;
}
</style>