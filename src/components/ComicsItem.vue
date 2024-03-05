<script>
export default{
    name: 'ComicsItem',

    // Prendo le proprieta(informazioni) necessarie dal genitore
    props:{
        // incico il nome di ogni props e il tipo
        comicName: String,
        comicImage: String,

    },

    data(){
        return{

        }
    }
}
</script>



<template>

<div class="product">
    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
    <h4>Action Comics</h4>
    <div class="price">$19.99</div>
</div>

</template>



<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/_variables.scss' as *;

</style>