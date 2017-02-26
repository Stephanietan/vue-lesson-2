<template>
  <div>I am the child component
    <slot name='groan'></slot>
    <p> this is a message from the parent; pls decode it!</p>
    <p> the decoded msg is : {{ decode(msgFromParent) }} </p>
    <p> {{ msgFromParent }} </p>
    <slot name='moan'></slot>
    <button @click='mutateMsg'>click to mutate msg</button>
  </div>
</template>

<script>
  export default {
    props: [ 'msgFromParent' ],
    data: function() {
      return {
        anotherMsg: 'Hello Universe!'
      }
    },
    methods: {
      decode: function(str) {
        return str.split('').reverse().join('')
      },
      mutateMsg: function() {
        this.$emit('emitMutateEvent', 'im going to mutate yoouuuu')
      }
    }
  }
</script>

<style scoped>

</style>
