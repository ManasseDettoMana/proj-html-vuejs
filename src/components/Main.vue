<template>
    <main>
        <div class="jumbotron">
            <div class="my_container">
                <div class="row" id="about">
                    <h2>more about damon vaughn</h2>
                    <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller "The story of my life"</p>
                    <a href="#"><img src="images/hover-button2.png" alt=""></a>
                </div>
            </div>
            <JumboNav :vettore="navBooksLink"/>
        </div>
    </main>
</template>

<script>
import JumboNav from './JumboNav.vue'
export default {
    name: 'Main',
    components: {
        JumboNav,
    },
    data: function(){
        return{
            navBooksLink: [
                {
                    url: 'images/ebay-logotan-2x.png',
                    link: '#'
                },
                {
                    url: 'images/audible-logotan-2x.png',
                    link: '#'
                },
                {
                    url: 'images/bb-logotan-2x.png',
                    link: '#'
                },
                {
                    url: 'images/kindlefire-logotan-2x.png',
                    link: '#'
                },

            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '~bootstrap/scss/bootstrap.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';
@import './style/variables.scss';

.jumbotron{
    text-align: center;
    #about{
        // margin-top: 100px;
        width: 60%;
        margin: 100px auto;
        h2{
            color: $primaryGold;
            margin-bottom: 25px;
        }
        p{
            font-size: 30px;
        }
    }
}
</style>