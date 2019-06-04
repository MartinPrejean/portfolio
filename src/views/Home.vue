<template>
  <transition name="fadeIn">
    <div v-if="show" class="home page">
      <div class="intro">
        <div class="design-home">
          <img class="img-home" src="@/assets/evaluations.jpg" alt="design">
        </div>
        <div class="development-home">
          <img class="img-home" src="@/assets/evaluations.jpg" alt="development">
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  data() 
  {
    return {
      show: false
    }
  },

  mounted() 
  {
    this.showToggle()
  },

  methods:
  {
    showToggle()
    {
      setTimeout(() => {
        this.show = true
      }, 3000);
    }
  }
}
</script>

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
  width: 50vw;
  height: 50vh;
}
  
</style>
