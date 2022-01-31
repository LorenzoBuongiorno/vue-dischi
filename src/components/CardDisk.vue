<template>
    <div>
        <div>
            <img :src="disco.poster" alt="">
        </div>
        <div>{{disco.title}}</div>
        <div>{{disco.author}}</div>
        <div>{{disco.year}}</div>
    </div>
</template>

<script>

export default {
props: {
    disco: Object
}
}
</script>

<style lang="scss">

</style>