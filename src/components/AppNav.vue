<script>
export default{
    name: 'AppNav',
}
</script>

<template>

    <nav>
        <div class="container">
            <div id="logo-img">
                <img src="/public/img/dc-logo.png" alt="">
            </div>
            <ul id="nav-links">
                <li>characters</li>
                <li class="clicked">comics</li>
                <li>movies</li>
            </ul>
        </div>
    </nav>

</template>

<style lang="scss">
@use '../styles/general.scss';

nav{

    background-color: white;
    color: black;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        align-items: stretch;
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

            // link
            &.clicked{
                color: #0282F9;
            }

            &.clicked::before{
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 100%;
                height: 5px;
                background-color: #0282F9;
            }
        }
    }
}

</style>
