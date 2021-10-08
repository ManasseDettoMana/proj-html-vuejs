<template>
    <footer>
        <div class="my_container">
            <div class="row d-flex justify-content-center align-items-center" id="link_row">
                <div class="col-3">
                    <img src="images/author-logo-round-small.png" alt="">
                </div>
                <div class="col-3">
                    <h2>about me</h2>
                    <ul>
                        <li v-for="(element, index) in aboutME" :key="index">{{element.text}}</li>
                    </ul>
                </div>
                <div class="col-3">
                    <h2>useful links</h2>
                    <ul>
                        <li v-for="(element, index) in usefulLinks" :key="index"><a :href="element.link">{{element.text}}</a></li>
                    </ul>
                </div>
                <div class="col-3">
                    <h2>contact info</h2>
                    <ul>
                        <li v-for="(element, index) in contactInfo" :key="index"><a :href="element.link">{{element.text}}</a></li>
                    </ul>
                </div>
            </div>
            <div class="row"></div>
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
                    text: 'lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc'
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
    background-position: center;
    height: 600px;
    .my_container{
        height: 100%;
        #link_row{
            height: 80%;
            ul{
                padding: 0;
            }
            h2{
                color: white;
                text-transform: uppercase;
            }
            a{
                color: white;
                text-decoration: none;
            }
            li{
                color: white;
                list-style-type: none;
            }
        }
    }
}

</style>