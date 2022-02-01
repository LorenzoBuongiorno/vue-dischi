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

</style>