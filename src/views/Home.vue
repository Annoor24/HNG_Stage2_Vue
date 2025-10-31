<template>
  <main class="hero">
    <div class="hero-content">
      <h2>Manage Your Tickets Seamlessly</h2>
      <p>
        A modern web app to create, track, and resolve tickets efficiently.
      </p>
      <div class="buttons">
        <router-link to="/login" class="btn">Login</router-link>
        <router-link to="/signup" class="btn secondary">Get Started</router-link>
      </div>
    </div>

    <img src="@/assets/wave.svg" class="wave" alt="wave" />
  </main>
</template>

<style>
.hero {
  text-align: center;
  padding: 4rem 2rem;
  background: white;
  max-width: 1440px;
  margin: 2rem auto;
  border-radius: 12px;
  position: relative;
}
.buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 2rem;
}
.btn {
  background: #0077cc;
  color: white;
  padding: 10px 20px;
  border-radius: 6px;
  text-decoration: none;
}
.btn.secondary {
  background: white;
  color: #0077cc;
  border: 1px solid #0077cc;
}
.wave {
  width: 100%;
  margin-top: 3rem;
}
</style>
