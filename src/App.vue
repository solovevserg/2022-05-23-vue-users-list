<template>
  <h1>Users list (toal: {{ users.length }})</h1>
  <input type="text" v-model="query">
  <p>Searched users count: {{ filteredUsers.length }}</p>
  <user v-for="user in filteredUsers" v-bind:user="user"></user>
</template>

<script>
import User from './components/user.vue';

export default {
  name: 'App',
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
    this.users = await fetch('https://sdal.pw/api/cdc/users').then(r => r.json());
  },
  computed: {
    filteredUsers() {
      return this.users.filter(user => user.name.includes(this.query));
    }
  }
}
</script>

