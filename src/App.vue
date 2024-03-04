<script>
import AppNav from './components/AppNav.vue';
import AppFoot from './components/AppFoot.vue';

export default{

    data(){
        return{

        }
    },
    components:{
        AppNav,
        AppFoot,
    }

}
</script>

<template>

<AppNav></AppNav>
<AppFoot></AppFoot>

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>
