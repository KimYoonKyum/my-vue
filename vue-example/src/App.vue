<template>
  <app-header
      v-bind:headerTitle="str"
      v-on:renew="renewStr"
  >

  </app-header>
  <div>
    {{str}}
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";

export default {
  name: 'App',
  components: {
    'app-header':AppHeader,
  },
  data: function() {
    return {
      str: 'HEADER'
    }
  },
  methods: {
    renewStr: function() {
      this.str = 'SENDED HEADER'
    }
  }
}
</script>

<style>

</style>
