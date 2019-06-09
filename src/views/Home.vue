<template>
  <transition name="fadeIn">
    <div class="home">
      <h1>Choose your side.</h1>
      <div class="intro">
        <div class="design-home">
          <h2>Design</h2>
          <router-link to="/design">
            <img class="img-home" src="@/assets/design-noir.jpg" alt="design">
          </router-link>
        </div>
        <div class="development-home">
          <h2>Development</h2>
          <router-link to="/development">
            <img class="img-home" src="@/assets/development-noir.jpg" alt="development">
          </router-link>
        </div>
      </div>
    </div>
  </transition>
</template>


<style>

/*
*   Home
*/

.home h1 
{
  text-align: center;
  font-size: 1.563rem;
}

.intro
{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.design-home, .development-home
{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  width: 80vw;
  height: 80vh;
}

.design-home h2, .development-home h2
{
  display: flex;
  justify-content: center;
  font-size: 1.22rem;
  padding: 2rem;
}

.img-home
{
  filter: grayscale();
  transition: .5s;
  width: 50vw;
  height: 70vh;
}

.img-home:hover
{
  transition: .5s;
  filter:none;
}

@media screen and (max-width: 768px)
{
  .img-home
  {
    width: 100vw;
    height: 30vh;
  }
} 

@media screen and (max-width: 500px)  
{
  .home h1 
  {
    padding-top: 2rem;
  }
  .intro
  {
    display: flex;
    flex-direction: column;
  }

  .design-home, .development-home
  {
    width: 100vw;
    height: 40vh;
  }

  .development-home h2
  {
    padding-top: 3rem;
  }

  .img-home
  {
    width: 100vw;
    height: 30vh;
  }
}
  
</style>
