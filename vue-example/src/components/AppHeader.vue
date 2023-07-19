<template>
  <header>
    <h1>{{headerTitle}}</h1>
    <button v-on:click="onSend">send</button>
  </header>
</template>

<script>
export default {
  props:['headerTitle'],
  methods: {
    onSend: function() {
      console.log('renew')
      this.$emit('renew')
    }
  }
}
</script>

<style>

</style>