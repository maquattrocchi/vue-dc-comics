<template>
    <section>
        <div class="container">
            <nav>
                <ul class="flex">
                    <li v-for="(item, index) in mainLinks" :key="index">
                        <img :src="item.image" :alt="item.testo">
                        <a :href="item.url">{{item.testo}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainBlueComponent',
    data(){
        return{
            mainLinks:[
                {
                    image: require("../assets/img/buy-comics-digital-comics.png"),
                    testo: 'Digital Comics',
                    url: '#',
                },
                {
                    image: require("../assets/img/buy-comics-merchandise.png"),
                    testo: 'Dc Merchandise',
                    url: '#',
                },
                {
                    image: require("../assets/img/buy-comics-subscriptions.png"),
                    testo: 'Subscription',
                    url: '#',
                },
                {
                    image: require("../assets/img/buy-comics-shop-locator.png"),
                    testo: 'Comic Shop Locator',
                    url: '#',
                },
                {
                    image: require("../assets/img/buy-dc-power-visa.svg"),
                    testo: 'Dc Power Visa',
                    url: '#',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/variables';
    @import '../style/general';

    section{
        background-color: $blueColor;
    }
    .container{
        justify-content: center;
    }
    nav{
        padding: 2rem 0,
    }
    ul{
        align-items: center;
        a{
            color: $whiteColor;
            text-transform: uppercase;
            vertical-align: middle;
        }
        img{
            height: 30px;
            vertical-align: middle;
            margin-right: 0.5rem;
        }
    }
</style>
