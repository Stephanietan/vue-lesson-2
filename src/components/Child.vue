<template>
  <div>I am the child component
    <p> this is a message from the parent; pls decode it!</p>
    <p> the decoded msg is : {{ decode(msgFromParent) }} </p>
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
      }
    }
  }
</script>

<style scoped>

</style>
