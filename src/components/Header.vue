<template>
    <header>
        <div class="my_container">
            <div class="row">
                <!-- header logo -->
                <div class="col-6">
                    <img src="images/author-logo-round.png" alt="">
                </div>
                <!-- header nav  -->
                <div class="col-6">
                    <nav>
                        <ul>
                            <!-- aggiungere v-for headerLinkArray  -->
                            <li v-for="(element, index) in headerLinkArray" :key="index" :class="{active : element.isActive}"><a href="element.link">{{element.name}}</a></li>
                            <li><a href="#"><i class="fas fa-shopping-cart"></i></a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
        <div class="my_container">
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
                    link: '#',
                    isActive: true
                },
                {
                    name: 'About Me',
                    link: '#',
                    isActive: false

                },
                {
                    name: 'Testimonials',
                    link: '#',
                    isActive: false
                },
                {
                    name: 'My Blog',
                    link: '#',
                    isActive: false
                },
                {
                    name: 'Meetups',
                    link: '#',
                    isActive: false
                },
                {
                    name: 'Shop',
                    link: '#',
                    isActive: false
                },
                {
                    name: 'Contact Me',
                    link: '#',
                    isActive: false
                },
                
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@import '~bootstrap/scss/bootstrap.scss';
@import '~@fortawesome/fontawesome-free/css/all.css';
@import './style/variables.scss';
header{
    background-image:linear-gradient(to bottom, rgba(0,0,0,0.25) 0%,rgba(0,0,0,0.9) 100%), url('../assets/hero-07-2x.jpg') ;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 85vh;
    position: relative;
    .my_container{
        width: 90%;
        margin: 0 auto;
        nav{
            height: 75px;

            ul{
                display: flex;
                justify-content: space-between;
                height: 100%;
                // margin-top: 30px;
                li{
                    // height: 100%;
                    list-style-type: none;
                    padding-top: 30px;

                    &:hover{
                        color: $primaryGold;
                        border-top: 5px solid $primaryGold;
                        a{
                            color: $primaryGold;
                        }
                    }
                    a{
                        text-decoration: none;
                        color: white;
                        font-weight: 400;
                    }
                }
            }
        }

        img{
            width: 200px;
        }
        .active{
            border-top: 5px solid $primaryGold;
            
            a{
                color: $primaryGold;
            }
        }
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