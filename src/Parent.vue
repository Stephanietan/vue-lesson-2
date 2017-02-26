<template>
  <div>
    <p>I am the parent component</p>
    <hr>
    <child-comp :msg-from-parent='text' @emitMutateEvent='text = $event' :mutateFn='mutateMe' :msg-from-sibling='msgFromSibling'></child-comp>
    <hr>
    <sibling-comp @siblingMsgEvent='msgFromSibling = $event'></sibling-comp>
  </div>
</template>

<script>
import Child from './components/Child.vue';
import Sibling from './components/Sibling.vue';

export default {
  components: { 'child-comp' : Child , 'sibling-comp' : Sibling },
  data: function() {
    return {
      msg : 'Hello world!',
      text: 'sedun dnes',
      msgFromSibling: ''
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
