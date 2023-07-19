<template>
  <form v-on:submit.prevent="onSubmit">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="text" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    onSubmit: function() {
      const url = 'https://jsonplaceholder.typicode.com/users'
      const data = {
        username: this.username,
        password: this.password
      }
      axios.post(url,data)
          .then((res)=>{
            console.log(res)
          })
          .catch((err)=>{
            console.log(err)
          })
    }
  }
}
</script>

<style>

</style>
