<template>
    <div>
        <card-disk v-for="(disco, i) in dischi" :key="i" :disco="disco" />
    </div> 
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

</style>