<template>
  <div id="app">
    <preloader/>
      <div id="nav" class="navbar" role="navigation" aria-label="main navigation">
        <div class="nav-left">
          <router-link class="nav-logo" to="/"><img class="logo" src="@/assets/logo.svg" alt="Martin Préjean Logo"></router-link>
        </div>
        <div class="navbar-brand">
          <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" @click="isOpen = !isOpen" v-bind:class="{'is-active': isOpen}">
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
          </a>
        </div>
          <div class="navbar-menu" v-bind:class="{'is-active': isOpen}">
            <transition name="burger">
              <div class="navbar-end">
                <div class="item item-1">
                  <router-link id="home" class="navbar-item is-tab" to="/">Home</router-link>
                </div>
                <div class="item item-2">
                  <router-link class="navbar-item is-tab" to="/about">About</router-link>
                </div>
                <div class="item item-3">
                  <router-link class="navbar-item is-tab" to="/design">Design</router-link>
                </div>
                <div class="item item-4">
                  <router-link class="navbar-item is-tab" to="/development">Development</router-link>
                </div>
                <div class="item item-5">
                  <router-link class="navbar-item is-tab" to="/contact">Contact</router-link>
                </div>
              </div>
            </transition>
          </div>
      </div>
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
  },
  data: function() {
        return {
            isOpen: false
        }
    }
}

</script>


<style>

@import "~bulma/css/bulma.css";

body
{
  font-size: 62.5%;
  font-family: 'Nunito', sans-serif;
  letter-spacing: 0.0625em;
  margin: 0 auto;
}

#app 
{
  width: 100vw;
  height: 100vh;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #eeeeee;
  background: #0E0E0E;
}

/*
*   Nav style
*/

.navbar 
{
  display: flex;
  justify-content: flex-end;
  width: 100vw;
}

.navbar-end .item
{
  padding: 25px 30px;
  transition:.5s;
  font-size: 1rem;
  display: flex;
  justify-content: flex-end;
}

.navbar, .navbar-menu
{
  background: #0E0E0E;
}

.navbar-item.is-tab:focus, .navbar-item.is-tab:hover {
    background-color: transparent;
    border-bottom-color: #0E0E0E;
}

#home
{
  display: none;
}

.nav-left
{
  width: 50vw;
  display: flex;
  justify-content: flex-start;
}

#nav a 
{
  font-weight: bold;
  text-decoration: none;
  color: #eeeeee;
}

#nav a.router-link-exact-active 
{
  color: #f0838c;
}

.logo
{
  width: 75px;
  height: 75px;
}

.nav-logo
{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  top: 0;
  left: 0;
  margin-left: 50px;
}

.page
{
  position: fixed;
  width: inherit;
}

/*
*   Project section
*/

.projects-section-right 
{
  display: flex;
  justify-content: center;
  padding: 3rem 0 20rem 0;
  will-change: transform;
}

.projects-section-left 
{
  display: flex;
  justify-content: center;
  padding: 3rem 0 20rem 0;
  will-change: transform;
}

.project-layout
{
  display: flex;
  align-items: center;
}

.project-img
{
  width: 50vw;
}
  
.projects-section-right .featured-text 
{
  padding: 2rem;
  border-left: 0.5rem solid #f0838c;
  width: 30vw;
}

.projects-section-left .featured-text 
{
  padding: 2rem;
  border-right: 0.5rem solid #f0838c;
  width: 30vw;
}

.project-text hr 
{
  border-color: #f0838c;
  border-width: .25rem;
  width: 30%;
}

.featured-text h4
{
  padding: 0 0 1rem 0;
  font-size: 1.263rem;
}

.featured-text p
{
  font-size: 0.9rem;
}

/* 
*   Animation betwenn pages
*/

.router-animation-enter-active
{
  animation: coming .5s;
  animation-delay: .7s;
  opacity: 0;
}

.router-animation-leave-active
{
  animation: going .5s;
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


/**

  RESPONSIVE

**/

@media screen and (max-width: 1024px) 
{
  .project-layout
  {
    display: block;
    margin-right: auto;
    margin-left: auto;
  }

  .project-img
  {
    margin-left: 1rem;
    width: 90vw;
  }

  .projects-section-right .featured-text, .projects-section-left .featured-text 
  {
    width: auto;
    border: none;
  }

  /**
  
    NAVIGATION / HAMBURGER
  
  **/

  .nav-left
  {
    display: none;
  }

  .navbar 
  {
    position: fixed;
    flex-direction: column;
    width: 100vw;
    padding: 0px;
    font-size: 1rem;
    bottom: 0;
    transition: .5s;
  }

  #home
  {
    display: block;
  }

  .logo
  {
    display: none;
  }

  .navbar-end .item
  {
   justify-content: center;
  }

  .navbar-brand
  {
    margin-right: auto;
    margin-left: auto;
  }

  .navbar-burger
  {
    margin-right: auto;
    margin-left: auto;
  }
  
  .navbar-menu .is-active
  {
    transition: .5s;
  }

  .is-active
  {
    transition: .2s ease-out;
  }

  .burger-enter-active, .burger-leave-active
  {
    transition: .2s ease-out;
  }

  .burger-enter, .burger-leave-to
  {
    transition: .2s ease-out;
  }
}
</style>
