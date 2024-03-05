<script>
import AppNav from './components/AppNav.vue';
import AppFoot from './components/AppFoot.vue';
import BlueLinks from './components/BlueLinks.vue';
import AppProduct from './components/AppProduct.vue';

export default{

    data(){
        return{

        }
    },
    components:{
        AppNav,
        AppProduct,
        BlueLinks,
        AppFoot,
    }

}
</script>

<template>

<AppNav></AppNav>

<AppProduct></AppProduct>

<BlueLinks></BlueLinks>

<AppFoot></AppFoot>

</template>

<style lang="scss">
@use '../src/styles/general.scss' as *;


</style>
