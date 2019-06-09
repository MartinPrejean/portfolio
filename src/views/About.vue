<template>
  <div class="about">
    <div class="about-description">
      <h1 class="about-title">About me</h1>
       <p>I am a second-year student at HETIC. I have a creative and structured mind. As a long-time athlete, I am also rigorous in the work I receive. I always want to surpass myself in what I do and to face new challenges.</p>
       <br>
       <p>I did about a dozen group projects. I worked on the design of wireframes/prototypes, logos, graphic charts. I also participated in the web-development of the projects.</p>
      <div class="about-skills">
        <h2>My skills</h2>
        <p>Photoshop, Illustrator, Sketch, Figma, HTML, CSS, Javascript, Vue.js, React.js, Google Analytics, Google AdWords.</p>
        <p>Native French speaker, Bilingual in English</p>
      </div>
    </div>
    <img class="img-about" src="@/assets/lapin.jpg" alt="Me with a rabbit">
  </div>
</template>

<style>

.about
{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 3rem;
  font-size: 1rem;
  background: #0E0E0E;
}

.about p 
{
  line-height: 1.563rem;
}

.about-description
{
  width: 40vw;
}

.about-skills
{
  padding-top: 1.5rem;
  width: 40vw;
}

.about-skills h2
{
  text-decoration: underline;
  padding: 1rem 0 1rem 0;
  font-size: 1.563rem;
}

.about-title
{
  font-size: 8rem;
}

.img-about
{
  margin-right: 2rem;
  height: 50vh;
  align-items: flex-end;
}

@media screen and (max-width: 1300px)
{
  .about-title
  {
    font-size: 6rem;
  }
}

@media screen and (max-width: 1024px)
{
  .img-about
  {
    margin-right: 2rem;
    height: 50vh;
    width: auto;
    align-items: flex-end;
  }

  .about-description
  {
    width: 80vw;
  }

  .about-skills
  {
    width: 80vw;
    margin-bottom: 3rem;
  }

  .about
  {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .img-about
  {
    margin: 0;
    margin-bottom: 3rem;
  }
} 

@media screen and (max-width: 500px)  
{
  .img-about
  {
    width: auto;
    height: auto;
  }
}
  
</style>


