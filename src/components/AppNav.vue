<script>
export default{
    name: 'AppNav',

    data(){
        return{
            links:[
                'Chatacter',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Collectibles',
                'Videos',
                'Fans',
                'News',
                'Shop',
            ],

            clickedLinksIndex: 1,
        }
    }
}
</script>

<template>

    <nav>
        <div class="container">
            <div id="logo-img">
                <img src="/public/img/dc-logo.png" alt="">
            </div>
            <ul id="nav-links">
                <li v-for="(link, index) in links"
                :class="index == clickedLinksIndex ? 'clicked' : '' "
                >{{ link }}</li>
            </ul>
        </div>
    </nav>

</template>

<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/_variables.scss' as *;

nav{

    background-color: white;
    color: black;
    
    .container{
        justify-content: space-between;
        align-items: center;
        align-items: stretch;
        padding: 0 20px;
        max-height: 120px;
    }

    #logo-img{
        padding: 18px 0;

        img{
            height: 100%;
        }
    }

    // lista link
    ul{
        display: flex;
        gap: 32px;
        list-style-type: none;
        font-weight: bold;
        text-transform: uppercase;
        margin: 0;

        // links
        li{
            position: relative;
            display: flex;
            align-items: center;

            // link cliccato/attivo
            &.clicked{
                color: $primary;
            }

            &.clicked::before{
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 100%;
                height: 5px;
                background-color: $primary;
            }
        }
    }
}

</style>
