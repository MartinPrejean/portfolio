<template>
  <div class="design">
    <h1>My projects</h1>
    <section class="projects-section-right" 
    v-for="project in projects" 
    :key="project.id">
          <!-- Featured Project Row dynamically generated -->
      <div class="project-layout">
        <img class="project-img" :src="project.img" :alt="project.name">
        <div class="featured-text">
          <h4>{{ project.name }}</h4>
          <p>{{ project.description }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>

const URL_PROJECT= 'http://martinprejean.com/';

export default {
  data () {
    return {
      projects: [
        { 
          name: 'World of Warships design',
          description: 'A little re-design I made with one of my favorite games and one of my favorite boats, the Yamato.', 
          url: `${URL_PROJECT}LdVOme`,
          img: require('@/assets/world-of-warships-design.png')
        },
        { 
          name: 'Wikipedia Re-design', 
          description: 'A wikipedia re-design I made in class for a project.',
          url: `${URL_PROJECT}LdVOme`,
          img: require('@/assets/wikipedia-re-design.png')
        },
        { 
          name: 'Typography Project',
          description: 'A work I made from a design project. We had to include the most out of a typography we purposefully chose.',
          url: `${URL_PROJECT}LdVOme`,
          img: require('@/assets/typography-project.png')
        },
        { 
          name: 'Graphic Work',
          description: 'I got bored so I decided to do this work.',
          url: `${URL_PROJECT}LdVOme`,
          img: require('@/assets/graphic-work.png')
        },
      ]
    }
  },

  // Method to get the image path dynamically but it didn't work
  // props: {
  //   folderImage: {
  //     type: String,
  //     default: '/img/'
  //   }
  // },
  // computed: {

  // },
  // methods: {
  //   /**
  //    * Sample thumbnail file name: `thumb--simon-game.jpg`
  //    * @param {String} projectName 
  //    */
  //   getThumbnailUrl (projectName) {
  //     return this.folderImage +
  //       projectName.toLowerCase().replace(/\s/g, '-') +
  //       '.png';
  //   }
  // },
  // mounted () {

  // }
}
</script>


<style>

.design
{
  background: #0E0E0E;
}

.design h1
{
  text-align: center;
  font-size: 3rem;
  padding: 3rem 0 1rem 0;
}
</style>

