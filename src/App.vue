<template>
  <div id="app">
    <header class="navbar">
      <h1>TicketApp</h1>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
    </header>

    <main class="hero">
      <div class="hero-content">
        <h2>Manage Your Tickets Seamlessly</h2>
        <p>
          A modern web app to create, track, and resolve tickets efficiently.
        </p>
        <div class="buttons">
          <button class="btn">Login</button>
          <button class="btn secondary">Get Started</button>
        </div>
      </div>

      <!-- Decorative wave background -->
      <svg class="wave" viewBox="0 0 1440 320">
        <path
          fill="#0077cc"
          fill-opacity="1"
          d="M0,160L80,154.7C160,149,320,139,480,128C640,117,800,107,960,122.7C1120,139,1280,181,1360,202.7L1440,224V320H1360C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320H0Z"
        ></path>
      </svg>

      <!-- Decorative circle -->
      <div class="circle"></div>
    </main>

    <footer>
      <p>© 2025 TicketApp. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body, #app {
  font-family: Arial, sans-serif;
  color: #333;
  background: #f5f5f5;
}

/* Navbar */
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

/* Hero Section */
.hero {
  position: relative;
  text-align: center;
  padding: 4rem 2rem;
  background: white;
  max-width: 1440px;
  margin: 0 auto;
  border-radius: 12px;
  overflow: hidden;
}

.hero-content {
  position: relative;
  z-index: 2;
}

.hero h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #222;
}

.hero p {
  max-width: 600px;
  margin: 0 auto 2rem;
  color: #555;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.btn {
  background: #0077cc;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1rem;
}

.btn.secondary {
  background: white;
  color: #0077cc;
  border: 1px solid #0077cc;
}

.btn:hover {
  opacity: 0.9;
}

/* Decorative Elements */
.wave {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
}

.circle {
  position: absolute;
  top: 20%;
  right: 10%;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: rgba(0, 119, 204, 0.2);
  z-index: 1;
}

/* Footer */
footer {
  text-align: center;
  padding: 1rem;
  background: #0077cc;
  color: white;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .hero h2 {
    font-size: 1.6rem;
  }

  .buttons {
    flex-direction: column;
  }
}
</style>


