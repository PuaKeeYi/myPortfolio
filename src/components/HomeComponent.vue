<template>
    <section id="home" class="home-section">
      <div class="content-wrapper">
        <h1>Hi! I'm <span class="highlight">Kee Yi</span></h1>
        <h2>A Freah Grade Data Analyst</h2>
        <h3>from Asia Pasific University</h3>
        <p>I'm a fresh graduate studied the course Computer Science Specialize in Data Analysis, so I have experience in manipulating and analyze data. 
          Although my major is data analysis, I also have a strong interest in software development where I'm am experience in Java and Python and also selflearned HTML, CSS and JavaScript.
          I am currently looking for a oppertunity to work as a Data Analyst or Software Developer, feel free to contact me if you have any questions or opportunities!</p>
      </div>
    </section>
</template>


<script>
export default {
  name: 'HomeComponent'
}
</script>


<style scoped>
.home-section {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #ffffff;
  padding: 1rem;
}

.content-wrapper {
  font-family: 'Poppins', sans-serif;
  max-width: 800px;
  color: #ffffff;
  text-align: left;
  line-height: 1.5;
}

.highlight {
  color: #c8ff00; 
  font-weight: 600;
}

h1 {
  margin: 0;
  line-height: 1.2;
  font-size: 3rem;
}

h2 {
  margin: 0;
  line-height: 1.2;
  font-size: 3.4rem;
}

h3 {
  margin: 0 0 0.4rem 0;
  line-height: 1.2;
  font-size: 1.5rem;
}

p {
  font-size: 1rem;
  margin: 0.3rem 0;
}
</style>