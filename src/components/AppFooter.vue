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
                    icon: "facebook",
                    link: "www.facebook.com"
                },
                {
                    icon: "twitter",
                    link: "www.twitter.com"
                },
                {
                    icon: "youtube",
                    link: "www.youtube.com"
                },
                {
                    icon: "pinterest",
                    link: "www.pinterest.com"
                },
                {
                    icon: "periscope",
                    link: "www.periscope.com"
                },
            ],
        };
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

        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;

.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    color: white;
    @include flex(row, space-between, null);

    .footer-container {
        display: flex;
        padding: 2rem 0;
        gap: 1rem;

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

        .right {
            background-position: center;
            background-repeat: no-repeat;
            background-image: url(../assets/img/dc-logo-bg.png);
            width: 60%;
            height: 360px;
        }
    }
}</style>