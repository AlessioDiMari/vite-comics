<script>
export default{
    name: 'AppFoot',

    data(){
        return{
            linkList:[
                {
                    name: 'dc comics',
                    links: ['Chapters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    name: 'shop',
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    name: 'dc',
                    links: ['Terms Of Use', 'Privacy Policy(New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscription', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    name: 'sites',
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
            ]
        }
    }
}
</script>


<template>

    <footer>
        <!-- parte superiore del footer -->
        <div class="top-foot">
            <div class="container">
                <!-- lista dei links info -->
                <div class="link-info">
                    <!-- link info singolo dinamicizzato -->
                    <div v-for="actualLinkList in linkList" class="link-info-section">
                        <h4>{{ actualLinkList.name }}</h4>
                        <ul>
                            <li v-for="actualLink in actualLinkList.links">{{ actualLink }}</li>
                        </ul>
                    </div>
                </div>
                <div id="logo-big">
                    <img src="/public/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

        <!-- parte inferiore del footer -->
        <div class="bottom-foot">
            <div class="container">
                <!-- bottone di accesso -->
                <div class="left">
                    <button>
                        SIGN-UP NOW!
                    </button>
                </div>
    
                <div class="right">
                    <strong>FOLLOW US</strong>
                    <!-- lista social -->
                    <ul>
                        <li><img src="../../public/img/footer-facebook.png" alt=""></li>
                        <li><img src="../../public/img/footer-twitter.png" alt=""></li>
                        <li><img src="../../public/img/footer-youtube.png" alt=""></li>
                        <li><img src="../../public/img/footer-pinterest.png" alt=""></li>
                        <li><img src="../../public/img/footer-periscope.png" alt=""></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>

</template>


<style lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/_variables.scss' as *;

footer{

    max-height: 480px;

    .top-foot{
        display: flex;
        justify-content: space-between;
        // align-items: center;
        padding: 0 20px;
        // max-width: 1280px;
        width: 100%;
        max-height: 370px;
        background-image: url('../../public/img/footer-bg.jpg');
        background-position: cover;
        overflow: hidden;
        
        .container{
            width: 100%;
        }

        .link-info{
            display: flex;
            flex-flow: column wrap;
            gap: 28px 30px;
            padding: 36px 0;
            

            h4{
                text-transform: uppercase;
            }

            ul{
            // display: flex;
            list-style-type: none;
            padding: 0;
            color: grey;
            }

        }

        #logo-big{
            align-self: center;
        }

    }
    
    .bottom-foot{

        background-color: #303030;

        .container{
            align-items: center;
            max-height: 110px;
            padding: 30px 20px;
    
            button{
                padding: 17px 14px;
                background-color: transparent;
                border: 2px solid $primary;
                font-weight: bold;
                cursor: pointer;
            }
    
    
            .right{
                display: flex;
                align-items: center;
                gap: 30px;

                strong{
                    color: $primary;
                }
    
                ul{
                    display: flex;
                    align-items: center;
                    gap: 18px;
                    list-style-type: none;
                }
    
            }
        }

    }

    

}

</style>