<template>
  <div id="list">
    <div v-for="item in result" v-bind:key="item.idx">
      {{ item.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchResultList.vue",
  props: ['result'],
  data: function() {
  },
  computed: {
  },
  methods: {
  }
}
</script>

<style scoped>

</style>