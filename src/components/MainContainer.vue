<template>
    <main>
        <div class="card-box">
            <card-disk v-for="(disco, i) in dischi" :key="i" :disco="disco" />
        </div> 
    </main>
</template>

<script>
import CardDisk from './CardDisk.vue'

export default {
    components:{
        CardDisk
    },
    props: {
        dischi: Array
    }
}
</script>

<style lang="scss">
main{
    .card-box{
        width:1500px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
    }
}

</style>