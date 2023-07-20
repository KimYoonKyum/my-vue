<template>
  <div id="list">
    <div v-for="item in propsResult" v-bind:key="item.idx">
      {{ item.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchResultList.vue",
  props: ['propsResult'],
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