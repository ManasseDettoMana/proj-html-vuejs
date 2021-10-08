<template>
    <footer>
        <div class="my_container">
            <div class="row">
                <div class="col-3">
                    <img src="images/author-logo-round-small.png" alt="">
                </div>
                <div class="col-3"></div>
                <div class="col-3"></div>
                <div class="col-3"></div>
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
                    text: 'lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc lorem ipsum ecc ecc '
                }
            ],
            usefulLinks: [
                {
                    link: 'Latest Book',
                },
                {
                    link: 'Upcoming Events',
                },
                {
                    link: 'Reecent Articles',
                },
                {
                    link: 'Busines Enquiries',
                },
                {
                    link: 'Visit My Foundation',
                },
            ],
            contactInfo: [
                {
                    link: '63 ga6sdoa9ufah aksfha 342'
                },
                {
                    link: 'Phone: (800) 000 000 00'
                },
                {
                    link: 'Mobile: (800) 000 000 00'
                },
                {
                    link: 'Email: pippo@gmail.com'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
footer{
    background-image: url('../assets/footer-3.jpg');
    background-position: center;
    height: 600px;
}

</style>