<template>
  <div>
    <p>I am the parent component</p>
    <hr>
    <child-comp :msg-from-parent='text' @emitMutateEvent='text = $event' :mutateFn='mutateMe'></child-comp>
    <hr>
    <sibling-comp></sibling-comp>
  </div>
</template>

<script>
import Child from './components/Child.vue';
import Sibling from './components/Sibling.vue';

export default {
  components: { 'child-comp' : Child, 'sibling-comp' : Sibling },
  data: function() {
    return {
      msg : 'Hello world!',
      text: 'sedun dnes'
    }
  },
  methods: {
    mutateMe: function() {
      this.text = 'callback mutation react style'
    }
  }
}
</script>

<style scoped>

</style>
