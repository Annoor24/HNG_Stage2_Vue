<template>
  <div class="auth">
    <h2>Login</h2>
    <form @submit.prevent="loginUser">
      <input type="email" v-model="email" placeholder="Email" required />
      <input type="password" v-model="password" placeholder="Password" required />
      <button type="submit">Login</button>
    </form>
    <p>Don’t have an account? <router-link to="/signup">Signup</router-link></p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: ""
    };
  },
  methods: {
    loginUser() {
      const users = JSON.parse(localStorage.getItem("users")) || [];
      const user = users.find(
        (u) => u.email === this.email && u.password === this.password
      );

      if (user) {
        localStorage.setItem("loggedInUser", this.email);
        alert("Login successful!");
        this.$router.push("/dashboard");
      } else {
        alert("Invalid email or password");
      }
    }
  }
};
</script>

<style>
.auth {
  text-align: center;
  margin-top: 5rem;
}
input {
  display: block;
  margin: 10px auto;
  padding: 10px;
  width: 250px;
}
button {
  background: #0077cc;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
}
</style>
