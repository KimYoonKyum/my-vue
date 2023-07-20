<template>
  <search-form v-on:setResult="result"/>
  <search-result-list v-bind:result="list"/>
</template>

<script>
import SearchForm from "@/components/SearchForm";
import SearchResultList from "@/components/SearchResultList.vue";

export default {
  name: 'App',
  components: {
    'search-form': SearchForm,
    'search-result-list': SearchResultList
  },
  data: function() {
    return {
      list: []
    }
  },
  computed: {
  },
  methods: {
    result: function(list) {
      this.list = list
    }
  }
}
</script>

<style>

</style>
