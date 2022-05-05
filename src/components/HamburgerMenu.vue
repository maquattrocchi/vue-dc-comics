<template>
    <div class="hamb-menu">
        <div @click="openMenu = true">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <div class="menu" :class="{'menu-open' : openMenu}">
            <div class="close" @click="openMenu = false">
                <span></span>
                <span></span>
            </div>
            <ul>
                <li v-for="(item,index) in links" :key="index">
                    <a :href="item.url" :class="{'selected' : item.active}">{{item.testo}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HamburgerMenu',
    props: ['links'],
    data(){
        return{
            openMenu: false
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables';

    .hamb-menu{
        position: relative;
        cursor: pointer;

        span{
        display: block;
        width: 2rem;
        margin: 0.3rem;
        height: 5px;
        background-color: #0282F9;
        }
        .menu{
            background-color: $whiteColor;
            padding: 2rem 2rem 1rem 1rem;
            text-align: end;
            position: absolute;
            right: 0;
            top: 0;
            display: none;

            &.menu-open{
                display: block;
            }
            .close{
                position: absolute;
                top: 9px;
                right: 40px;

                span{
                    position: absolute;
                    transform: rotate(50deg);

                    &:last-of-type{
                        position: absolute;
                        transform: rotate(-50deg);
                    }
                }
            }
            li{
                padding: 0;

                a{
                    padding: 0;
                }
            }
        }
    }

    @media screen and (min-width: 992px) {
        .hamb-menu{
            display: none;
        }
    }
</style>