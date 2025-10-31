<template>
  <div class="dashboard">
    <h2>Welcome, {{ userEmail }}</h2>
    <p>You’re now logged in!</p>
    <button @click="logout">Logout</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userEmail: localStorage.getItem("loggedInUser")
    };
  },
  methods: {
    logout() {
      localStorage.removeItem("loggedInUser");
      alert("You’ve been logged out.");
      this.$router.push("/");
    }
  }
};
</script>

<style>
.dashboard {
  text-align: center;
  margin-top: 5rem;
}
button {
  background: red;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 6px;
}
</style>
