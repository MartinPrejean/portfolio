<template>
  <div class="about"> <!-- ref="about" -->
    <h1 class="about-right-title">About me</h1> <!-- :style="titleStyle" -->
    <div class="about-description">
       <p>I am a second-year student at HETIC. I have a creative and structured mind. As a long-time athlete, I am also rigorous in the work I receive. I always want to surpass myself in what I do and to face new challenges.</p>
       <br>
       <p>I did about a dozen group projects. I worked on the design of wireframes/prototypes, logos, graphic charts. I also participated in the web-development of the projects.</p>
    </div>
    <div class="about-skills">
      <h2>My skills</h2>
      <p>Photoshop, Illustrator, Sketch, Figma, HTML, CSS, Javascript, Vue.js, React.js, Google Analytics, Google AdWords.</p>
      <p>Native French speaker, Bilingual in English</p>
    </div>
  </div>
</template>

<style>

.about
{
  padding: 3rem;
  font-size: 1rem;
}

.about-description
{
  width: 50vw;
}

.about-skills
{
  padding-top: 1.5rem;
  width: 50vw;
}

.about-skills h2
{

  padding: 1rem 0 1rem 0;
  font-size: 1.563rem;
}

.about-right-title
{
  font-size: 8rem;
}

.img-technologies
{
  display: flex;
}

.img-technologies img
{
  width: 100px;
  height: 100px;
}
  
</style>


