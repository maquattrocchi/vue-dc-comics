<template>
    <section>
        <div class="container">
            <div class="left-footer">
                <a href="#">Sign-up now</a>
            </div>
            <div class="right-footer">
                <p>Follow us</p>
                <ul>
                    <li v-for="(item, index) in socialLink" :key="index">
                        <a :href="item.url">
                            <img :src="item.image" :alt="item.alt">
                        </a>

                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterSecComp',
    data(){
        return{
            socialLink: [
                {
                    image: require("../assets/img/footer-facebook.png"),
                    alt: 'facebook',
                    url: '#',
                },
                {
                    image: require("../assets/img/footer-twitter.png"),
                    alt: 'twitter',
                    url: '#',
                },
                {
                    image: require("../assets/img/footer-youtube.png"),
                    alt: 'youtube',
                    url: '#',
                },
                {
                    image: require("../assets/img/footer-pinterest.png"),
                    alt: 'pinterest',
                    url: '#',
                },
                {
                    image: require("../assets/img/footer-periscope.png"),
                    alt: 'periscope',
                    url: '#',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables';
    @import '../style/general';
    section{
        background-color: $darkGrey;
        padding: 1.5rem 0;
    }
    .left-footer{
        padding: 1rem;
        border: 2px solid $blueColor;
        a {
            text-transform: uppercase;
            color: $whiteColor;
        }
    }
    .right-footer {
        display: flex;
        align-items: center;
        gap: 1rem;
        p{
            color: $blueColor;
            text-transform: uppercase;
            font-size: 1.5rem;
            font-weight: bold;
        }
        ul{
            display: flex;
            gap: 1rem;
            li{
                list-style: none;
            }
        }
    }
</style>