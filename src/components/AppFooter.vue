<script>
export default {
    data() {
        return {
            footerTop: [
                {
                    title: "DC COMICS",
                    list: ["Charaters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "SHOP",
                    list: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    list: ["Terms Of Use", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Rating", "Shop Help", "Contact Us"]
                },
                {
                    title: "SITES",
                    list: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                },
            ],
            footerBottom: [
                {
                    icon: "facebook"
                },
                {
                    icon: "twitter"
                },
                {
                    icon: "youtube"
                },
                {
                    icon: "pinterest"
                },
                {
                    icon: "periscope"
                },
            ],
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/footer-${img}.png`, import.meta.url).href;
        },
    },
};
</script>

<template>
    <div class="footer-top">
        <div class="container">
            <div class="footer-container">
                <div class="left" v-for="item in footerTop">
                    <h4>{{ item.title }}</h4>
                    <ul>
                        <li v-for="list in item.list"><a href="">{{ list }}</a></li>
                    </ul>
                </div>
                <div class="right"></div>
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">
            <div class="space-between">
                <div class="btn">
                    <button>SING-UP NOW!</button>
                </div>
                <div class="social">
                    <div class="title">
                        <h4>FOLLOW US</h4>
                    </div>
                    <ul>
                        <li v-for="list in footerBottom">
                            <a href=""><img :src=getImagePath(list.icon) :alt="`Icon of ${list.icon}`"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    color: white;
    @include flex(row, space-between, null);

    .footer-container {
        display: flex;
        gap: 2rem;

        .left {
            margin-top: 2rem;

            h4 {
                margin-bottom: 1rem;
            }

            ul {
                list-style: none;

                a {
                    color: gray;
                    font-size: 0.7rem;
                    text-decoration: none;
                }
            }
        }

        .right {
            background-position: center;
            background-repeat: no-repeat;
            background-image: url(../assets/img/dc-logo-bg.png);
            width: 60%;
            height: 360px;
            margin-left: 5rem;
        }
    }

}

.footer-bottom {
    background-color: $footer-color;
    padding: 2rem 0;
    .space-between {
        @include flex(null, space-between, center);

        button {
            border: 2px solid $primary;
            padding: 0.7rem 1rem;
            background-color: $footer-color;
            color: white;

            &:hover {
                background-color: lighten($footer-color, 20%);
                cursor: pointer;
            }
        }

        .social {
            @include flex(null, space-between, center);

            h4 {
                color: $primary;
            }

            ul {
                @include flex(row, space-between, center);
                gap: 1rem;
                margin-left: 1rem;
                list-style: none;

                img {
                    width: 30px;
                }
            }
        }
    }

}
</style>