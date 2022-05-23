<template>
  <h1>Users list (total: {{ users.length }})</h1>
  <input type="text" v-model="query" placeholder="Type a name...">
  <p>Searched users count: {{ filteredUsers.length }}</p>
  <user v-for="user in filteredUsers" v-bind:user="user"></user>

  <br><img height="16" src="@/assets/github.png" alt="GitHub"> See <a href="https://github.com/solovevserg/2022-05-23-vue-users-list">source code on GitHub</a>. &copy; <a href="https://github.com/solovevserg">Solovev Sergei</a>, 2022
</template>

<script>
import User from './components/user.vue';

export default {
  name: 'app',
  components: {
    User,
  },
  data() {
    return {
      users: [],
      query: '',
    }
  },
  async mounted() {
    this.users = await fetch('https://sdal.pw/api/cdc/users')
      .then(r => r.json());
  },
  computed: {
    filteredUsers() {
      return this.users.filter(user => user.name.includes(this.query));
    }
  }
}
</script>

<style>
html {
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(150deg, rgb(255, 220, 144), rgb(255, 166, 197), rgb(253, 149, 255));
  min-height: 100%;
}
</style>