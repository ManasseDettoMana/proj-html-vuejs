<template>
    <footer>
        <div class="my_container">
            <div class="row d-flex " id="link_row">
                <div class="col-3">
                    <img src="images/author-logo-round-small.png" alt="">
                </div>
                <div class="col-3">
                    <h2>about me</h2>
                    <ul>
                        <li v-for="(element, index) in aboutME" :key="index">{{element.text}}</li>
                    </ul>
                </div>
                <div class="col-3" >
                    <h2>useful links</h2>
                    <ul id="central_link_column">
                        <li v-for="(element, index) in usefulLinks" :key="index"><a :href="element.link"><i class="fas fa-chevron-right"></i>{{element.text}}</a></li>
                    </ul>
                </div>
                <div class="col-3" >
                    <h2>contact info</h2>
                    <ul>
                        <li v-for="(element, index) in contactInfo" :key="index"><a :href="element.link">{{element.text}}</a></li>
                    </ul>
                </div>
            </div>
            <div class="row d-flex justify-content-center " id="bottom_row">
                <p>&copy; Copyright 2012-2020 | avada Theme by <span>ThemeFusion</span> | All rights Reserved | Powered by <span>WordPress</span></p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function(){
        return{
            aboutME: [              
                {
                    text: 'lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecclorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc'
                }
            ],
            usefulLinks: [
                {
                    text: 'Latest Book',
                    link: '#'
                },
                {
                    text: 'Upcoming Events',
                    link: '#'
                },
                {
                    text: 'Reecent Articles',
                    link: '#'
                },
                {
                    text: 'Busines Enquiries',
                    link: '#'
                },
                {
                    text: 'Visit My Foundation',
                    link: '#'
                },
            ],
            contactInfo: [
                {
                    text: '63 ga6sdoa9ufah aksfha 342',
                    link: '#'
                },
                {
                    text: 'Phone: (800) 000 000 00',
                    link: '#'
                },
                {
                    text: 'Mobile: (800) 000 000 00',
                    link: '#'
                },
                {
                    text: 'Email: pippo@gmail.com',
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

footer{
    background-image: url('../assets/footer-3.jpg');
    background-position: top;
    height: 450px;
    .my_container{
        height: 100%;
        ul{
            padding: 0;
            li{
                color: grey;
                list-style-type: none;
                padding-bottom: 15px;
                font-size: 14px;
                a{
                    color: grey;
                    text-decoration: none;
                    font-size: 14px;
                }
            }
        }
        h2{
            color: white;
            text-transform: uppercase;
            padding-bottom: 20px;
            font-size: 16px;
            font-weight: 600;
        }

    }
    .col-3{
        padding-top: 100px;
    }
    p{
        color: grey;
    }
    span{
        color: white;
    }
    #bottom_row{
        text-align: center;
    }
    #central_link_column{
        i{
            padding-right: 15px;
            font-size: 13px;
            color: white;
            a{
                color: white;
            }
        }
    }
}

</style>