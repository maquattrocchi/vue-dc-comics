<template>
    <section>
        <div class="container">
            <p>Content here</p>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainGrid',
}
</script>

<style scoped lang="scss">
    @import '../style/variables';
    @import '../style/general';

    section{
        background-color: $blackColor;
        padding: 2rem 0;
    }
    p{
        color: $whiteColor
    }
</style>
