<template>
  <div>I am the child component
    <p> this is a message from the parent; pls decode it!</p>
    <p> the decoded msg is : {{ decode(msgFromParent) }} </p>
    <p> {{ msgFromParent }} </p>
    <button @click='mutateMsg'>click to mutate msg</button>
    <button @click='mutateFn()'>click to mutate msg callback style</button>
    <p> {{ msgFromSibling }} </p>
  </div>
</template>

<script>
  export default {
    props: [ 'msgFromParent', 'mutateFn', 'msgFromSibling' ],
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
