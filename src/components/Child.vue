<template>
  <div>{{ anotherMsg }}</div>
</template>

<script>
  export default {
    data: function() {
      return {
        anotherMsg: 'Hello Universe!'
      }
    }
  }
</script>

<style scoped>
  div {
    border: 1px solid blue;
  }
</style>
