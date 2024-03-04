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
        <div class="top-foot">
            <div class="link-info container">
                <div v-for="actualLinkList in linkList" class="link-info-section">
                    <h4>{{ actualLinkList.name }}</h4>
                    <ul>
                        <li v-for="actualLink in actualLinkList.links">{{ actualLink }}</li>
                    </ul>
                </div>
            </div>
            
        </div>
        <div class="bottom-foot">
        </div>
    </footer>

</template>


<style lang="scss">
@use '../styles/general.scss';

footer{

    max-height: 480px;

    .top-foot{
        display: flex;
        justify-content: space-between;
        padding: 0 20px;
        width: 100%;
        max-height: 370px;
        background-image: url('../../public/img/footer-bg.jpg');

        
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

    }
    
    .bottom-foot{
        max-height: 110px;
    }

    

}

</style>