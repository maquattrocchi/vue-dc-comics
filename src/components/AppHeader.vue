<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="dc-logo">
            <nav>
                <ul class="flex">
                    <li v-for="(item, index) in links" :key="index" :class="{'selected' : item.active}">
                        <a :href="item.url" :class="{'selected' : item.active}">{{item.testo}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data(){
        return{
            links: [
                {
                    testo: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Comics',
                    url: '#',
                    active: true
                },
                {
                    testo: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Tv',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Games',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Collectibles',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Videos',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    testo: 'News',
                    url: '#',
                    active: false
                },
                {
                    testo: 'Shop',
                    url: '#',
                    active: false
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/variables';
    @import '../style/general';

    .container{
        justify-content: space-between;
    }
    img{
        width: 50px;
    }
    li {
        padding: 2rem 0;
        border-bottom: 3px solid transparent;
        a{
            color: $blackColor;
            font-size: 0.8rem;
            text-transform: uppercase;
            font-weight: bold;
            padding: 2rem 0;
        }
    }
    li.selected{
        border-color: $blueColor;
    }
    a.selected{
        color: $blueColor;
    }
    li:hover a{
        color: $blueColor;
    }
</style>
