<template>
    <main>
        <loader  class="loader" v-if="dischi.length <= 9"/>
        <div v-else class="card-box">
            <card-disk v-for="(disco, i) in dischi" :key="i" :disco="disco" />
        </div> 
    </main>
</template>

<script>
import Loader from './Loader.vue'
import CardDisk from './CardDisk.vue'

export default {
    components:{
        Loader,
        CardDisk
    },
    props: {
        dischi: Array
    }
}
</script>

<style lang="scss">
main{
    background-color: #1e2d3b;
    height: 92vh;
    position: relative;

    .loader{
        position: absolute;
        left: 50%;
        bottom: 50%;

    }
    .card-box{
        width:1500px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        padding: 50px;
    }
}
</style>