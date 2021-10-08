<template>
    <div class="row" id="bg_principale">
        <div id="contenitoreJumbo" class="">
            <div class="col-6" id="left-column">
                <img src="images/audible-app-2x-400x418.png" alt="" id="immagie_telefono">
            </div>
            <div class="col-6 d-flex flex-column justify-content-center align-items-center">
                <div class="row">
                    <h2>New Audiobook</h2>
                    <h3>no time to read? no problem. listen to it</h3>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Perferendis ab esse magnam nihil illo voluptatibus explicabo vero numquam perspiciatis, in eaque officia saepe porro, error consequatur ea. Quidem, doloribus illo.</p>
                </div>
                <div class="row" id="JumboBannerRowImg">
                    <img src="images/audible-logo.png" alt="">
                    <img src="images/bn-logo-tall.png" alt="">
                    <img src="images/kindle-logo-tall.png" alt="">
                </div>
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'JumboBanner'
}
</script>

<style lang="scss" scoped>
@import './style/variables.scss';
@import '~bootstrap/scss/bootstrap.scss';
#bg_principale{
    height: 700px;
    background-image: url('../assets/banner.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    #contenitoreJumbo{
        display: flex;
        width: 65%;
        margin: 0 auto;
        #left_column{
            display: flex;
            align-items: flex-end;
        }
        h2{
            color: white;
        }
        h3{
            text-transform: uppercase;
            color: $primaryGold;
        }
        p{
            color: grey;
            font-size: 18px;
        }
        #JumboBannerRowImg{
            display: flex;
            justify-content: space-between;
            display: none;
        }
    }
}
</style>