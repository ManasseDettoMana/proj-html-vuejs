<template>
    <header>
        <div class="container">
            <div class="row">
                <!-- header logo -->
                <div class="col-6">
                    <img src="images/author-logo-round.png" alt="">
                </div>
                <!-- header nav  -->
                <div class="col-6 d-flex">
                    <nav>
                        <ul class="d-flex">
                            <!-- aggiungere v-for headerLinkArray  -->
                            <li v-for="(element, index) in headerLinkArray" :key="index"><a href="element.link">{{element.name}}</a></li>
                            <li><a href="#"><i class="fas fa-shopping-cart"></i></a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row">
                <div id="lastest_book_release"></div>   
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function(){
        return{
            //array contenente le informazioni presenti nell'header 
            headerLinkArray: [
                {
                    name: 'Home',
                    link: '#'
                },
                {
                    name: 'About Me',
                    link: '#'
                },
                {
                    name: 'Testimonials',
                    link: '#'
                },
                {
                    name: 'My Blog',
                    link: '#'
                },
                {
                    name: 'Meetups',
                    link: '#'
                },
                {
                    name: 'Shop',
                    link: '#'
                },
                {
                    name: 'Contact Me',
                    link: '#'
                },
                
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@import '~bootstrap/scss/bootstrap.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';
header{
    background: url('../assets/hero-07-2x.jpg'), linear-gradient(rgba(0,0,0,.5), rgba(0,0,0,.9));
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 85vh;
    position: relative;

    img{
        width: 200px;
    }
    #lastest_book_release{
        width: 650px;
        height: 50%;
        background-color: white;
        position: absolute;
        top: 101%;
        left: 100%;
        transform: translate(-100%, -100%);
    }
}





</style>