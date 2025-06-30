// =============================
// AboutView.vue
// =============================
<template>
  <main class="about-page">
    <h1>About Me</h1>

    <p>
      Hi! I'm Kee Yi — a fresh graduate in Computer Science specializing in Data Analysis who enjoys coding and discovering the hidden stories within data. 
      As a Data Analysis major at Asia Pacific University, I have hands-on experience in data manipulation and analysis. During my studies,
      I worked on various projects that involved data preprocessing, transformation, and visualization to extract meaningful insights.
    </p>

    <p>
      Although my major is data analysis, I also have a strong interest in software development. I am experienced in Java and Python with a solid understanding of object-oriented programming concepts,
      and I have self-learned HTML, CSS, and JavaScript. I completed an internship as a software development intern at a local company, where I contributed to front-end development using TypeScript.
    </p>

    <p>
      In my final year, I explored machine learning and developed predictive models using real-world datasets. I built classification systems for projects such as brain tumor detection
      and my final year project: bleached coral detection using image classification techniques.
    </p>

    <p>
      Outside tech, I enjoy research and often dive into topics across biology, physics, and chemistry — areas that help me understand myself and the world better.
      This knowledge even helps me solve everyday problems. I also love cooking and find it fascinating to learn about the chemical reactions between different ingredients.
    </p>

    <p>
      That's a brief introduction about me. I'm a passionate graduate actively looking for opportunities to grow as a Data Analyst or Software Developer.
      Feel free to reach out if you'd like to connect or collaborate!
    </p>
  </main>
</template>

<script setup>
</script>

<style scoped>
.about-page {
  width: 100%;
  max-width: none;
  margin: 6rem auto 3rem;
  padding: 0 1.5rem;
  line-height: 1.75;
  font-size: 1.1rem;
  font-family: 'Inter', 'Poppins', sans-serif;
}
.about-page h1 {
  font-size: 2.4rem;
  margin-bottom: 2rem;
  font-weight: 700;
  color: #00ffd9;
}
.about-page p {
  margin-bottom: 1.8rem;
  text-align: justify;
}
.about-page h1 {
  text-align: center;
}
</style>
