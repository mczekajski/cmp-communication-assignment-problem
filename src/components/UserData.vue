<template>
  <div class="component">
    <label>Name input</label>
    <input name="name" v-model="name" @input="updateData">
    <label>Age input</label>
    <input name="age" v-model="age" @input="updateData">
  </div>
</template>

<script>

export default {
  data() {
    return {
      name: '',
      age: ''
    }
  },
  methods: {
    updateData() {
      this.$emit('update-data', { name: this.name, age: this.age })
    }
  }

}
</script>

<style>
  .component {
    width: 50%;
  }
</style>