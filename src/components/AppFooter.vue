<template>
    <footer>
        <footer-first-comp/>
        <footer-sec-comp/>
    </footer>
</template>

<script>
import FooterFirstComp from './FooterFirstComp'
import FooterSecComp from './FooterSecComp.vue'
export default {
    name: 'AppFooter',
    components:{
        FooterFirstComp,
        FooterSecComp,
    }
}
</script>

<style lang="scss">
    @import '../style/variables';
    @import '../style/general';

    .container{
        justify-content: space-between;
    }
</style>
