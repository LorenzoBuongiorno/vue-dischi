<template>
    <div>
        <select v-model="selected" @change="$emit('genre', selected)">
            <option disabled value="">Genre</option>
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
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
    margin-left: 15px;
}
</style>