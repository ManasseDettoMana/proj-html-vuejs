<template>
    <header>
        <div class="my_container">
            <div class="row">
                <!-- header logo -->
                <div class="col-6">
                    <a href="#"><img src="images/author-logo-round.png" alt=""  id="header_logo"></a>
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
        <div class="my_container" id="bottom_container">
            <div class="row" id="principal_row">
                <!-- left part  -->
                <div class="col-7" id="left_part">
                    <div class="my_container" >
                        <div class="row">
                            <div id="left_text_side">
                                <h1>DAMON VAUGHN</h1>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae culpa omnis modi iure ratione tempore, exercitationem</p>
                                <span><em>- The New York Times</em></span>

                            </div>
                        </div>
                    </div>
                </div>
                <!-- right part  -->
                <div class="col-5">
                    <div class="row h-30"></div>
                    <!-- background bianco qui -->
                    <div class="row " id="lbr">
                        <div class="my_container d-flex justify-content-center align-items-center flex-wrap pt-5" id="">
                            <div class="col-6">
                                <img src="images/book-widget.png" alt="">
                            </div>
                            <div class="col-6">
                                <h2>latest book release</h2>
                                <h3>d. vaughn autobiography</h3>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur ratione illo veritatis odit voluptate aperiam totam, sint voluptates ut quia illum placeat, distinctio modi commodi error, cupiditate repellat. Autem, delectus!</p>
                            </div>
                            <div class="col-12">
                                <img src="images/hover-button1.png" alt="">
                            </div>
                        </div>
                    </div>
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
                    link: '#about',
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

    #bottom_container{
        height: calc(100% - 205.28px);
        margin-right: 0;
        #principal_row{
            height: 100%;
        }
        #left_text_side{
            width: 90%;
        }
        #left_part{
            h1{
                color: $primaryGold;
                font-size: 75px;
            }
            p{
                font-size: 50px;
                color: white;
            }
            span{
                font-size: 25px;
                color: grey;
            }
        }
    }
    .my_container{
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

        #header_logo{
            width: 200px;
        }
        .active{
            border-top: 5px solid $primaryGold;
            
            a{
                color: $primaryGold;
            }
        }
    }
}
#lbr{
    background-color: white;
    height: 65%;
}
.h-30{
    height: 35%;
}






</style>