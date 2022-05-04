<template>
    <header>
        <div class="container display-flex">
            <img src="../assets/img/dc-logo.png" alt="dc-logo">
            <nav>
                <ul>
                    <li v-for="(item, index) in links" :key="index">
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

    header{
        padding: 1rem 0;
    }
    .display-flex{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    img{
        width: 50px;
    }
    ul{
        display: flex;
        gap: 1rem;
        li {
            list-style: none;
            a{
                color: $blackColor;
                font-size: 0.8rem;
                text-transform: uppercase;
                font-weight: bold;
                padding: 1rem 0;
            }
        }
    }
    a.selected{
        color: $blueColor;
        border-bottom: 3px solid $blueColor;
    }
</style>
