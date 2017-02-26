<template>
  <div>
    <p>{{ msg }}</p>
    <child-comp></child-comp>
  </div>
</template>

<script>
import Child from './components/Child.vue';

export default {
  components: { 'child-comp' : Child },
  data: function() {
    return {
      msg : 'Hello world!'
    }
  }
}
</script>

<style scoped>

</style>
