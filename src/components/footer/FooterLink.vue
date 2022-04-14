<template>

    <div id="container">

        <!-- Prima lista -->
        <div>
            <ul>
                <h3>DC Comics</h3>
                <li v-for="(elem, index) in arrayDCComics" :key="index">
                    <a href="#">{{elem}}</a> 
                </li>
            </ul>
            <ul>
                <h3>Shop</h3>
                <li v-for="(elem, index) in arrayShop" :key="index">
                    <a href="#">{{elem}}</a>
                </li>
            </ul>
        </div>

        <!-- Seconda Lista -->
        <div>
            <ul>
                <h3>DC</h3>
                <li v-for="(elem, index) in arrayDC" :key="index">
                    <a href="#">{{elem}}</a>
                </li> 
            </ul>
        </div>

        <!-- Terza Lista -->
        <div>
            <ul>
                <h3>SITES</h3>
                <li v-for="(elem, index) in arraySites" :key="index">
                    <a href="#">{{elem}}</a>
                </li> 
            </ul>
        </div>

        <img src="../../assets/loghi/dc-logo-bg.png" alt="">
    </div>

</template>

<script>
    export default {
        name: 'FooterLink',

        data() {
            return {
                arrayDCComics: [
                    'Characters',
                    'Comics',
                    'Movies',
                    'TV',
                    'Games',
                    'Videos',
                    'News'
                ],
                arrayShop: [
                    'Shop DC',
                    'Shop DC Collectibles'
                ],
                arrayDC: [
                    'Terms Of Use',
                    'Privacy Police (New)',
                    'Ad Choises',
                    'Advertising',
                    'Jobs',
                    'Subscriptions',
                    'Talent Workshops',
                    'CPSC Certificates',
                    'Ratings',
                    'Shop Help',
                    'Contact Us'
                ],
                arraySites: [
                    'DC',
                    'MAD Magazine',
                    'DC Kids',
                    'DC Universe',
                    'DC Power Visa'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    #container {
        padding: 30px 0;
        position: relative;
    }

    div {
        display: flex;
        margin-right: 50px;
        ul {
            margin-bottom: 20px;
            list-style-type: none;
            text-align: left;

            h3 {
                color: white;
                margin-bottom: 15px;
            }

            li {
                color: grey;
                text-align: left;

                a{
                    font-size: $f-small;
                    color: white;
                    margin-bottom: 5px;
                }
                a:hover{
                    text-decoration: underline;
                }
            }
            
        }
    }
    img{
        position: absolute;
        top: -20%;
        left: 50%;
        width: 500px;
        z-index: 0;
    }
    // Il primo div viene incolonnato DC Comics - Shop
    div > div:nth-child(1){
        flex-direction: column;
    }
</style>