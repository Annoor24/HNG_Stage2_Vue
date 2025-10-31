<template>
  <div class="auth">
    <h2>Signup</h2>
    <form @submit.prevent="registerUser">
      <input type="email" v-model="email" placeholder="Email" required />
      <input type="password" v-model="password" placeholder="Password" required />
      <button type="submit">Signup</button>
    </form>
    <p>Already have an account? <router-link to="/login">Login</router-link></p>
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
    registerUser() {
      const users = JSON.parse(localStorage.getItem("users")) || [];
      if (users.some((u) => u.email === this.email)) {
        alert("User already exists");
        return;
      }
      users.push({ email: this.email, password: this.password });
      localStorage.setItem("users", JSON.stringify(users));
      alert("Signup successful!");
      this.$router.push("/login");
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
