<template>
  <div>
    <p>I am the parent component</p>
    <child-comp :msg-from-parent='text' @emitMutateEvent='text = $event'>
      <h1 slot='moan'>im doing this at 1am and Im so tired</h1>
      <h3 slot='groan'>sigghhh</h3>
    </child-comp>
  </div>
</template>

<script>
import Child from './components/Child.vue';

export default {
  components: { 'child-comp' : Child },
  data: function() {
    return {
      msg : 'Hello world!',
      text: 'sedun dnes'
    }
  }
}
</script>

<style scoped>

</style>
