<template>
    <div class="box">
        <div class="prod-card">
            <div class="card-image">
                <img :src="immagine" :alt="titolo">
            </div>
            <p>{{titolo}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ComicsCard',
    data(){
        return{

        }
    },
    props: {
        immagine: String,
        titolo: String,
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables';
    @import '../style/general';

    .box{
        width: calc((100% / 12) * 2);
        max-width: calc((100% / 12) * 2);
        flex: 0 0 auto;

        .prod-card{
            display: flex;
            flex-direction: column;
            padding: 1rem;

            .card-image{
                width: 100%;
                height: 150px;
                overflow: hidden;

                img{
                    width: 100%;
                }
            }
            p{
                color: $whiteColor;
                text-transform: uppercase;
                padding-top: 1rem;
            }
        }
    }
    
    @media screen and (max-width: 992px) {
        .box{
            width: calc((100% / 12) * 3);
            max-width: calc((100% / 12) * 3);
        }
    }
    @media screen and (max-width: 576px) {
        .box{
            width: calc((100% / 12) * 4);
            max-width: calc((100% / 12) * 4);
        }
    }
</style>