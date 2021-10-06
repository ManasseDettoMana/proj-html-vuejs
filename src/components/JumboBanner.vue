<template>
    <div class="row" id="bg_principale">
        <div id="contenitoreJumbo">
            <div class="col-6" id="left-column">
                <img src="images/audible-app-2x.png" alt="" id="phone_image">
            </div>
            <div class="col-6"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'JumboBanner'
}
</script>

<style lang="scss" scoped>

#bg_principale{
    height: 600px;
    background-image: url('../assets/banner.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    #contenitoreJumbo{
        width: 65%;
        margin: 0 auto;
        #left_column{
            display: flex;
            align-items: flex-end;
            #phone_image{      
                width: 500px;
            }
        }
    }
}

</style>