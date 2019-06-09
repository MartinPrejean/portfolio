<template>
  <transition name="fadeIn">
    <div class="home page">
      <div class="intro">
        <div class="design-home">
          <router-link to="/design">
            <img class="img-home" src="@/assets/evaluations.jpg" alt="design">
          </router-link>
        </div>
        <div class="development-home">
          <router-link to="/development">
            <img class="img-home" src="@/assets/evaluations.jpg" alt="development">
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

.intro
{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.design-home, .development-home
{
  width: 80vw;
  height: 80vh;
}

.img-home
{
  filter: grayscale();
  transition: .5s;
  width: 50vw;
  height: 50vh;
}

.img-home:hover
{
  transition: .5s;
  filter:none;
}
  
</style>
