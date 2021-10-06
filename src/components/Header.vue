<template>
    <header class="p-relative">
        <div class="container">
            <div class="row">
                <!-- header logo -->
                <div class="col-6">
                    <img src="images/author-logo-round.png" alt="" href="#">
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
        <div id="latest_book_release">
            <div class="container">
                <div class="row justify-content-center" id="riga__">
                    <div class="col-6">
                        <img src="images/book-widget.png" alt="" id="book_widget">
                    </div>
                    <div class="col-6">
                        <h2>Latest Book Release</h2>
                        <h3 class="text-uppercase">d. vaughn autobiography</h3>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. In consectetur nesciunt sint veniam nostrum </p>
                    </div>
                    <img src="images/hover-button1.png" alt="" id="pay_button">
                </div>
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
    .p-relative{
        position: relative;
    }
    .container{
        width: 90%;
        margin: 0 auto;
        nav{
            height: 75px;

            ul{
                display: flex;
                justify-content: space-between;
                height: 100%;
                li{
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
    #latest_book_release{
        width: 600px;
        height: 50%;
        background-color: white;
        position: absolute;
        top: 101%;
        left: 100%;
        transform: translate(-100%, -100%);
        display: flex;
        justify-content: center;
        align-content: center;
        .container{
            display: flex;
            justify-content: center;
            align-content: center;
            #riga__{
                padding-top: 40px;
                #pay_button{
                    width: 100%;
                    height: 100px;
                }
                #book_widget{
                    width: 250px
                }
            }
        }
    }
}






</style>