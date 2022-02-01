<template>
    <div>
        <select v-model="selected" @change="$emit('genre', selected)">
            <option disabled value="">Genre</option>
            <option>All</option>
            <option>Rock</option>
            <option>Pop</option>
            <option>Jazz</option>
            <option>Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selected: ''
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
}
</style>