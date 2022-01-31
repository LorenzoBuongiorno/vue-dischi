<template>
    <div class="song">
        <div class="picture">
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
.song{
    width: calc(100% / 5);
    display: flex;
    flex-direction: column;
    align-items: center;
    .picture{
        height: 160px;
        img{
            height: 100%;
        }

    }
}

</style>