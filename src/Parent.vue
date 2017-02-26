<template>
  <div>
    <p>I am the parent component</p>
    <child-comp :msg-from-parent='text' @emitMutateEvent='text = $event' :mutateFn='mutateMe'></child-comp>
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
