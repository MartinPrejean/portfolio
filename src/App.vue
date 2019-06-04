<template>
  <div id="app">
    <preloader/>
    <router-link class="nav-logo" to="/"><img class="logo" src="@/assets/logo.png" alt="Martin Préjean Logo"></router-link>
    <transition>
      <div id="nav">
        <router-link class="nav-link" to="/about">About</router-link>
        <router-link class="nav-link" to="/design">Design</router-link>
        <router-link class="nav-link" to="/development">Development</router-link>
      </div>
    </transition>
    <transition name="router-animation">
      <router-view/>
    </transition>
  </div>
</template>

<script>

import Preloader from '@/components/Preloader.vue'

export default {
  components:
  {
    Preloader
  }
}
</script>


<style>
body
{
  font-size: 62.5%;
  margin: 0 auto;
  background: #0E0E0E;
}

#app 
{
  width: 100vw;
  height: 90vh;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eeeeee;
}

/*
*   Nav style
*/

#nav 
{
  display: flex;
  justify-content: flex-end;
  margin: 30px;
  font-size: 1rem;
}

.nav-link
{
  margin-right: 5%;
}

#nav a 
{
  font-weight: bold;
  text-decoration: none;
  color: #eeeeee;
}

#nav a.router-link-exact-active 
{
  color: #42b983;
}

.logo
{
  width: 75px;
  height: 75px;
}

.nav-logo
{
  position: absolute;
  display: flex;
  justify-content: flex-start;
  top: 0;
  margin-left: 5%;
}

.page
{
  position: fixed;
  width: inherit;
}

/*
*   Custom cursor
*/

.cursor
{
  width: 20px;
  height: 20px;
  border: 1px solid white;
  border-radius: 50%;
}


/* 
*   Transition betwenn pages
*/

.router-animation-enter-active
{
  animation: coming 1s;
  animation-delay: .7s;
  opacity: 0;
}

.router-animation-leave-active
{
  animation: going 1s;
}

@keyframes going
{
  from
  {
    transform: translateX(0px);
  }
  to 
  {
    transform: translateX(-50px);
    opacity: 0;
  }
}

@keyframes coming
{
  from
  {
    transform: translateX(-50px);
    opacity: 0;
  }
  to 
  {
    transform: translateX(0px);
    opacity: 1;
  }
}

</style>
