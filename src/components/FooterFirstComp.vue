<template>
    <section>
        <div class="container">
            <div class="left-footer">
                <div>
                    <p>Dc Comics</p>
                    <ul>
                        <li v-for="(item, index) in dcComicsList" :key="index">
                            <a :href="item.url">{{item.testo}}</a>
                        </li>
                    </ul>
                    <p>Shop</p>
                    <ul>
                        <li v-for="(item, index) in shopList" :key="index">
                            <a :href="item.url">{{item.testo}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <p>Dc</p>
                    <ul>
                        <li v-for="(item, index) in dcList" :key="index">
                            <a :href="item.url">{{item.testo}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <p>Sites</p>
                    <ul>
                        <li v-for="(item, index) in sitesList" :key="index">
                            <a :href="item.url">{{item.testo}}</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="right-footer">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterFirstComp',
    data(){
        return{
            dcComicsList:[
                {
                    testo: 'Characters',
                    url: '#',
                },
                {
                    testo: 'Comics',
                    url: '#',
                },
                {
                    testo: 'Movies',
                    url: '#',
                },
                {
                    testo: 'TV',
                    url: '#',
                },
                {
                    testo: 'Games',
                    url: '#',
                },
                {
                    testo: 'Videos',
                    url: '#',
                },
                {
                    testo: 'News',
                    url: '#',
                },
            ],
            shopList: [
                {
                    testo: 'Shop DC',
                    url: '#'
                },
                {
                    testo: 'Shop DC Collectibles',
                    url: '#'
                }
            ],
            dcList: [
                {
                    testo: 'Terms Of Use',
                    url: '#'
                },
                {
                    testo: 'Privacy policy (New)',
                    url: '#'
                },
                {
                    testo: 'Ad Choices',
                    url: '#'
                },
                {
                    testo: 'Advertising',
                    url: '#'
                },
                {
                    testo: 'Jobs',
                    url: '#'
                },
                {
                    testo: 'Subscriptions',
                    url: '#'
                },
                {
                    testo: 'Talent Workshop',
                    url: '#'
                },
                {
                    testo: 'CPSC Certificates',
                    url: '#'
                },
                {
                    testo: 'Ratings',
                    url: '#'
                },
                {
                    testo: 'Shop Help',
                    url: '#'
                },
                {
                    testo: 'Contact Us',
                    url: '#'
                },
            ],
            sitesList: [
                {
                    testo: 'DC',
                    url: '#'
                },
                {
                    testo: 'MAD Magazine',
                    url: '#'
                },
                {
                    testo: 'DC Kids',
                    url: '#'
                },
                {
                    testo: 'DC Univers',
                    url: '#'
                },
                {
                    testo: 'DC Power Visa',
                    url: '#'
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
    @import '../style/variables';
    @import '../style/general';

    section{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }
    .left-footer{
        display: flex;
        gap: 1rem;
        p{
            color: $whiteColor;
            font-size: 1.5rem;
            font-weight: bold;
            text-transform: uppercase;
            padding-bottom: 1rem;
        }
        ul{
            padding-bottom: 1rem;
            li{
                list-style: none;
                a{
                    color: $lightGrey;
                }
            }
        }
    }
    .right-footer img{
        width: 450px;
    }

</style>
