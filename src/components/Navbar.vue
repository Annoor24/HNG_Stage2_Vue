<template>
  <header class="navbar">
    <h1 class="logo">TicketApp</h1>
    <nav>
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/login">Login</router-link></li>
        <li><router-link to="/signup">Signup</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<style>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: white;
  padding: 1rem 2rem;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
.navbar ul {
  display: flex;
  list-style: none;
  gap: 1.5rem;
}
.navbar a {
  text-decoration: none;
  color: #0077cc;
  font-weight: bold;
}
.logo {
  color: #0077cc;
}
</style>
