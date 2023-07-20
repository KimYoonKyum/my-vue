<template>
  <form v-on:submit.prevent="onSearch">
    <div>
      <label for="searchName">검색이름: </label>
      <input id="searchName" type="text" v-model="searchOptions.searchName">
    </div>
    <div>
      <label for="searchIdx">검색IDX: </label>
      <input id="searchIdx" type="text" v-model="searchOptions.searchIdx" disabled>
    </div>
    <button type="submit" v-bind:disabled="isValid">SEARCH</button>
  </form>
</template>

<script>
export default {
  name: "SearchForm.vue",
  data: function() {
    return {
      searchOptions: {
        searchName: '',
        searchIdx: 0
      }
    }
  },
  computed: {
    isValid: function() {
      return this.searchOptions.searchName === ''
    }
  },
  methods: {
    onSearch: function() {
      const originList = [
        {idx:1,name:'aaa'},
        {idx:2,name:'tom'},
        {idx:3,name:'back'},
        {idx:4,name:'go'},
        {idx:5,name:'bbb'},
        {idx:6,name:'ccc'},
      ]
      this.$emit('setResult', originList.filter((item)=>item.name === this.searchOptions.searchName))
    }
  }
}
</script>

<style scoped>

</style>