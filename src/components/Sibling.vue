<template>
  <div>
    <p>some msg in component</p>
    <button @click='emitSiblingMsg'>click to emit sibling msg</button>
  </div>
</template>

<script>
  export default {
    data: function() {
      return {
      }
    },
    methods: {
      emitSiblingMsg: function() {
        this.$emit('siblingMsgEvent', 'Hello from sibling!!!')
      }
    }
  }
</script>

<style></style>
