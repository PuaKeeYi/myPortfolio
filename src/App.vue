// =============================
// App.vue
// =============================
<template>
  <header class="site-nav">
    <RouterLink to="/" class="logo">Kee Yi</RouterLink>
    <nav>
      <RouterLink to="/"  class="nav-item" exact>Home</RouterLink>
      <RouterLink to="/about" class="nav-item">About</RouterLink>
      <RouterLink to="/projects" class="nav-item">Projects</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<script setup>
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
  background: #001919;
  color: #eaeaea;
}

/* Navigation */
.site-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.8rem 2rem;
  background: rgba(0, 25, 25, 0.9);
  backdrop-filter: blur(6px);
  z-index: 1000;
  box-shadow: 0 2px 4px rgba(0,0,0,0.4);
}
.logo {
  font-weight: 700;
  font-size: 1.4rem;
  color: #00ffd9;
  text-decoration: none;
}
.nav-item {
  margin-left: 1.8rem;
  text-decoration: none;
  color: #eaeaea;
  font-weight: 500;
  transition: color 0.2s;
}
.nav-item:hover,
.nav-item.router-link-active {
  color: #00ffd9;
}

/* Give pages some top offset because nav is fixed */
main, section {
  scroll-margin-top: 80px; /* for anchor links */
}
</style>
