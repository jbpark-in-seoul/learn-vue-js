<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">ID: </label>
      <input type="text" id="username" v-model="username">
    </div>
    <div>
      <label for="password">PASSWORD: </label>
      <input type="password" id="password" v-model="password">
    </div>
    <button type="submit">Login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      // event.preventDefault(); // js, jquery 방식
      // `v-on:submit.prevent` 사용
      var url = 'https://jsonplaceholder.typicode.com/users';
      var data = {
        username: this.username,
        password: this.password
      };
      axios.post(url, data)
      .then(function(response) {
        console.log(response);
      })
      .catch(function(error) {
        console.log(error);
      })
    }
  }
}
</script>

<style>

</style>