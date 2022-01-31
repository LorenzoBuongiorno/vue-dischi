<template>
    <div class="card">
        <div class="song">
            <div class="picture">
                <img :src="disco.poster" alt="">
            </div>
            <div class="title">{{disco.title}}</div>
        </div>
        <div class="description-box">
            <div class="description">
                <div class="author">{{disco.author}}</div>
                <div class="year">{{disco.year}}</div>
            </div>
        </div>
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
@import '@/style/card.scss';

</style>