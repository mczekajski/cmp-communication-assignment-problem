<template>
  <div class="component">
    <h2>{{ username }}</h2>
    <h3>{{ age }}</h3>
  </div>
</template>

<script>
export default {
  props: ["username", "age"],
};
</script>

<style>
    .component {
        width: 40%;
    }
</style>
