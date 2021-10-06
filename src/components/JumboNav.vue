<template>
    <nav>
        <ul>
            <li v-for="(element, index) in vettore" :key="index"><a href="element.link"><img :src="element.url" alt=""></a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'JumboNav',
    props: ['vettore']
}
</script>

<style lang="scss" scope>
nav{
    // display: flex;
    // justify-content: center;
    // align-items: center;
    ul{

        width: 65%;
        margin: 0 auto;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        justify-content:  space-between;

        li{
            list-style-type: none;

            img{
                width: 250px;
            }
        }
    }
}

</style>