<script>
import AppNav from './components/AppNav.vue';
import AppFoot from './components/AppFoot.vue';
import BlueLinks from './components/BlueLinks.vue';

export default{

    data(){
        return{

        }
    },
    components:{
        AppNav,
        BlueLinks,
        AppFoot,
    }

}
</script>

<template>

<AppNav></AppNav>

<BlueLinks></BlueLinks>

<AppFoot></AppFoot>

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>
