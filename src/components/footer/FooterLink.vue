<template>
    <div>
        <div>
            <ul>
                <h3>DC Comics</h3>
                <li v-for="(elem, index) in arrayDCComics" :key="index">{{elem}}</li>
            </ul>
            <ul>
                <h3>Shop</h3>
                <li v-for="(elem, index) in arrayShop" :key="index">{{elem}}</li>
            </ul>
        </div>
        <div>
            <ul>
                <h3>DC</h3>
                <li v-for="(elem, index) in arrayDC" :key="index">{{elem}}</li>
            </ul>
        </div>
        <div>
            <ul>
                <h3>SITES</h3>
                <li v-for="(elem, index) in arraySites" :key="index">{{elem}}</li>
            </ul>
        </div>
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
    @import '../../style/mixin.scss';

    div {
        padding: 30px 0;
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
                // Stile bold e uppercase
                font-size: 0.7rem;
                margin-bottom: 5px;

            }
        }
    }
</style>