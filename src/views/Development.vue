<template>
  <div class="development">
    <h1>My projects</h1>
    <section class="projects-section-right" 
    v-for="project in projects" 
    :key="project.id">
          <!-- Featured Project Row dynamically generated -->
      <div class="project-layout">
        <router-link :to="project.url">
          <img class="project-img" :src="project.img" :alt="project.name">
        </router-link>
        <div class="featured-text">
          <h4>{{ project.name }}</h4>
          <p>{{ project.description }}</p>
        </div>
      </div>
    </section>
  </div>
</template>


<script>

const URL_PROJECT= 'projects/';

export default {
  data () {
    return {
      projects: [
        { 
          name: 'D\'ISS Cover',
          description: 'Here is a project I made with other students of my school. It\'s a website made in PHP where the location of the ISS is given and informations of the country below it.',
          url: `${URL_PROJECT}iss-cover`,
          img: require('@/assets/iss-cover.png')
        },
        { 
          name: 'Star Wars API',
          description: 'A little project I did using React.js for a technical test.', 
          url: `${URL_PROJECT}star-wars-api`,
          img: require('@/assets/star-wars-api.png')
        },
        { 
          name: 'PAC-Audit', 
          description: 'I gave a new and fresh look for the website of my father. Go check-it out ! (almost done)',
          url: `${URL_PROJECT}pac-audit`,
          img: require('@/assets/pac-audit.png')
        },
      ]
    }
  },
}
</script>

<style>

.development
{
  background: #0E0E0E;
}

.development h1
{
  text-align: center;
  font-size: 3rem;
  padding: 3rem 0 1rem 0;
}
</style>