<template>
<h2>Users</h2>

<div v-if="loading">
<div class="spinner-border text-info" role="status">
</div>
<p class="loading">Loading...</p>
</div>

<router-link to="/users/new"><button v-if="!loading" type="button" class="btn btn-warning">Add new user</button></router-link>

<section>
<div class="grid">
<div :key="user._id" v-for="user in users">
<User :user="user" />
</div>
</div>
</section>

<button v-if="!loading" @click.native="scrollToTop" class="btn btn-warning back-to-top">Back to top</button>

</template>

<script>
import User from '../components/User.vue';

export default {
    name: 'Users',
    components: {
        User
    },
    data() {
        return {
            users: [],
            loading: false
        }
    },
    methods: {
      async fetchUsers() {
        this.loading = true;
        const response = await fetch('https://automatrixapi.pythonanywhere.com/api/users');
        const {users} = await response.json();
        this.loading = false;
        return users;
      },
      scrollToTop() {
      window.scrollTo(0,0);
    }
    },
    async created() {
    this.users = await this.fetchUsers();
    this.loading = false;
  }
}
</script>

<style scoped>
button {
  margin: 0 auto 40px;
  font-size: 20px;
}

</style>