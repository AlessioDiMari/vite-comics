<script>
export default{
    name: 'BlueLinks',

    data(){
        return{

            links:[
                {
                    nome: 'Digital Comics',
                    img: 'buy-comics-digital-comics.png'
                },
                {
                    nome: 'DC Merchandise',
                    img: 'buy-comics-merchandise.png'
                },
                {
                    nome: 'Subscription',
                    img: 'buy-comics-subscriptions.png'
                },
                {
                    nome: 'Comic Shop Locator',
                    img: 'buy-comics-shop-locator.png'
                },
                {
                    nome: 'DC Power Visa',
                    img: 'buy-dc-power-visa.svg'
                },
            ]

        }
    }
}
</script>


<template>

<div id="blue-links">
    <div class="container">
        <div class="row">
            <div v-for="link in links" class="col">
                <img :src=" '/img/' + link.img " alt="">
                <span>{{ link.nome }}</span>
            </div>
        </div>
    </div>
</div>

</template>


<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/_variables.scss' as *;

#blue-links{
    background-color: $primary;

    .row{
        display: flex;
        gap: 74px;
        padding: 50px;

        .col{
            display: flex;
            align-items: center;
            gap: 16px;
            height: 55px;
            text-transform: uppercase;
            cursor: pointer;

            img{
                max-width: 55px;
                height: 100%;
            }
        }

    }

}


</style>