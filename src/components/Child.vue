<template>
  <div>{{ anotherMsg }}
    <p> {{ decode(msgFromParent) }} </p>
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
