// =============================
// ProjectView.vue
// =============================
<template>
  <section class="projects">
    <h1>Projects</h1>

    <ul class="grid">
      <li v-for="proj in projects" :key="proj.title" class="card">
        <img :src="proj.image" :alt="proj.title" />
        <h2>{{ proj.title }}</h2>
        <p>{{ proj.desc }}</p>
        <a :href="proj.link" target="_blank" rel="noopener" class="btn">View Repo</a>
      </li>
    </ul>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'Coral Bleaching Classifier',
    desc: 'CNN deep learning model that detects coral health from underwater images.',
    image: './img/coral image.jpg',
    link: 'https://github.com/PuaKeeYi/Deep-learning-on-coral-classification'
  },
  {
    title: 'Airport Simulation',
    desc: 'Concurrent Java simulation featuring the operations of an airport, including flight arrivals, departures, and passenger processing.',
    image: './img/airport simulation.png',
    link: 'https://github.com/PuaKeeYi/airport_simulation'
  },
  {
    title: 'Giant Bike sales drop analysis',
    desc: 'Data analysis project using Python to explore sales trends and identify factors affecting Giant Bike sales drop at specific year',
    image: './img/giant bike.png',
    link: 'https://github.com/PuaKeeYi/GiantBike_Analysis'
  }
]
</script>

<style scoped>
.projects {
  width: 80vw; /* 80% of the viewport width */
  padding: 6rem 1rem 3rem;
  max-width: 1200px;
  margin: 0 auto;
}
.projects h1 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.4rem;
}
.grid {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}
.card {
  background: #012525;
  color: #fff;
  border-radius: 8px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.card img {
  width: 100%;
  height: 170px;
  object-fit: cover;
}
.card h2 {
  font-size: 1.4rem;
  margin: 1rem;
}
.card p {
  flex: 1;
  margin: 0 1rem 1rem;
  font-size: 0.95rem;
  line-height: 1.4;
}
.btn {
  margin: 0 1rem 1.5rem;
  align-self: flex-start;
  background: #00ffd9;
  color: #012525;
  padding: 0.5rem 1.2rem;
  border-radius: 4px;
  text-decoration: none;
  font-weight: 600;
  transition: background 0.25s;
}
.btn:hover {
  background: #00c4aa;
}
</style>
