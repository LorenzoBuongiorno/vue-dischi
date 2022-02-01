<template>
    <div>
        <select v-model="selected">
            <option disabled value="">Genre</option>
            <option>Rock</option>
            <option>Pop</option>
            <option>Jazz</option>
            <option>Metal</option>
        </select>
        <span>Selected: {{ selected }}</span>
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