<template>
    <main>
        <div class="card-box">
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
    height: calc(100vh - 70px);

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