<script>
export default{
    name: 'ComicsItem',

    // Prendo le proprieta(informazioni) necessarie dal genitore
    props:{
        // incico il nome di ogni props e il tipo
        comicName: String,
        comicImage: String,
        comicPrice: String,
    },

    data(){
        return{

        }
    }
}
</script>



<template>

<div class="product">
    <img :src="comicImage" alt="">
    <h4>{{ comicName }}</h4>
    <div class="price">{{ comicPrice }}</div>
</div>

</template>



<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/_variables.scss' as *;

</style>