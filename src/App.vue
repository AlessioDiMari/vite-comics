<script>
import AppNav from './components/AppNav.vue';
import AppFoot from './components/AppFoot.vue';
import BlueLinks from './components/BlueLinks.vue';
import AppProduct from './components/AppProduct.vue';
import AppHero from './components/AppHero.vue';

export default{

    data(){
        return{

        }
    },
    components:{
        AppNav,
        AppHero,
        AppProduct,
        BlueLinks,
        AppFoot,
    }

}
</script>

<template>

<AppNav></AppNav>

<AppHero></AppHero>

<AppProduct></AppProduct>

<BlueLinks></BlueLinks>

<AppFoot></AppFoot>

</template>

<style lang="scss">
@use '../src/styles/general.scss' as *;


</style>
