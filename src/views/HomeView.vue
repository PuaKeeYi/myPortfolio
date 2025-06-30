// =============================
// HomeView.vue
// =============================
<script setup>
import { ref } from 'vue'

const email = ref('aronpua14@gmail.com')
const copied = ref(false)

function copyToClipboard() {
  navigator.clipboard.writeText(email.value).then(() => {
    copied.value = true
    setTimeout(() => copied.value = false, 2000) // Message disappears after 2 seconds
  })
}
</script>

<template>
  <section class="home">
    <div class="container">
      <!-- Main Hero Text -->
      <div class="overlay">
        <h1 class="name">Hi, I'm <span class="highlight">Kee Yi</span></h1>
        <h2 class="tagline">A fresh grade Data Analyst & Software Developer</h2>
        <RouterLink to="/projects" class="cta">View My Work</RouterLink>
      </div>

      <!-- Right Profile Info -->
      <div class="profile">
        <img src="/img/avatar.jpg" alt="Kee Yi avatar" class="avatar" />
        <div class="socials">
          <a href="https://github.com/PuaKeeYi" target="_blank" rel="noopener" aria-label="GitHub">
            <font-awesome-icon icon="fa-brands fa-github" />
          </a>
          <a href="https://linkedin.com/in/kypua" target="_blank" rel="noopener" aria-label="LinkedIn">
            <font-awesome-icon icon="fa-brands fa-linkedin" />
          </a>
        </div>
        <div>
          <a class="email-container">
            <font-awesome-icon icon="fa-brands fa-google" />
            <p class="email">aronpua14@gmail.com</p>
            <font-awesome-icon icon="copy" class="copy-icon" @click="copyToClipboard" title="Copy email"/>
            <p v-if="copied" class="copied-msg">Copied!</p>
          </a>
          
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.home {
  height: 100vh;
  background: url("/home.webp") center/cover fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
}
.container {
  width: 80vw; /* 80% of the viewport width */
  max-width: 1200px; /* Optional: prevent it from getting too big */
  display: flex;
  align-items: center;
  justify-content: center; /* if you want content inside also centered */
  gap: 4rem;
  padding: 2rem;
  max-width: 3000px; 
}
.profile {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
  text-align: center;
}
.avatar {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #00ffd9;
}
.socials {
  display: flex;
  gap: 1.2rem;
  font-size: 1.8rem;
}
.socials a {
  color: #fff;
  transition: color 0.3s;
}
.socials a:hover {
  color: #00ffd9;
}
.email {
  font-size: 1rem;
  color: #ccc;
}
.overlay {
  text-align: left;
  max-width: 600px;
}
.name {
  font-size: clamp(2.5rem, 6vw, 5rem);
  font-weight: 700;
  margin: 0;
}
.highlight {
  color: #00ffd9;
}
.tagline {
  font-size: clamp(1.2rem, 3vw, 2rem);
  margin: 1rem 0 2.5rem;
  font-weight: 500;
}
.cta {
  display: inline-block;
  padding: 0.8rem 2rem;
  border: 2px solid #00ffd9;
  border-radius: 4px;
  color: #00ffd9;
  text-decoration: none;
  transition: background 0.25s;
}
.cta:hover {
  background: #00ffd9;
  color: #012525;
}

.email-container {
  display: flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
}

.copy-icon {
  cursor: pointer;
  transition: transform 0.2s;
}

.copy-icon:hover {
  transform: scale(1.2);
}

.copied-msg {
  font-size: 0.875rem;
  color: green;
  margin-left: 24px;
  margin-top: 4px;
}

</style>
