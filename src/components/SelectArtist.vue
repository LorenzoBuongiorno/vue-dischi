<template>
    <div>
        <select v-model="selectedArtist" @change="$emit('artist', selectedArtist)">
            <option disabled value="">Artist</option>
            <option>All</option>
            <option>Metallica</option>
            <option>Deep Purple</option>
            <option>Eric Clapton</option>
            <option>Iron Maiden</option>
            <option>Steve Gadd Band</option>
            <option>Sting</option>
            <option>Queen</option>
            <option>Dave Weckl</option>
            <option>Michael Jacjson</option>
        </select>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selectedArtist: ''
        }
    }
}

</script>

<style lang="scss">
select{
    border: 0px;
    padding: 10px 15px;
    border-radius: 15px;
    background-color: #1e2d3b;
    color: #fff;
    font-size: 20px;
    text-align: center;
}
</style>