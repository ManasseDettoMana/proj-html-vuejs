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

<style>

</style>