<template>
    <div>
        <select v-model="selectedArtist" @change="$emit('artist', selectedArtist)">
            <option disabled value="">Artist</option>
            <option value="All">All</option>
            <option value="Metallica">Metallica</option>
            <option value="Deep Purple">Deep Purple</option>
            <option value="Eric Clapton">Eric Clapton</option>
            <option value="Iron Maiden">Iron Maiden</option>
            <option value="Steve Gadd Band">Steve Gadd Band</option>
            <option value="Sting">Sting</option>
            <option value="Queen">Queen</option>
            <option value="Dave Weckl">Dave Weckl</option>
            <option value="Michael Jacjson">Michael Jacjson</option>
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