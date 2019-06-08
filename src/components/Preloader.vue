<template>
    <transition name="fade">
        <div v-if="show" class="bubble-wrapper page">
            <div ref="bubble" class="bubble">
                <img class="bubble-image" src="@/assets/logo.png">
            </div>
            <div ref="bubblePulse" class="bubble-pulse"></div>
        </div>
    </transition>
</template>

<script>

import { TimelineLite, Back, Elastic, Expo } from 'gsap'

export default 
{
  name: 'preloader',
  data() 
  {
    return {
      show: true,
      timeline: null,
    }
  },

  mounted() 
  {
    this.showToggle()

    const { bubble, bubblePulse } = this.$refs
    const timeline = new TimelineLite()

    this.timeline = new TimelineLite(
    {
      onComplete: () => this.timeline.restart()
    })
    
    timeline.to(bubble, 0.2, 
    {
      scale: 0.8,
      rotation: 10,
      ease: Back.easeOut.config(1.7),
    })   
    timeline.to(
      bubblePulse,
      0.5, 
      {
        scale: 0.9,
        opacity: 1,
      },
     '-=0.6' 
    )

    this.timeline.to(bubble, 1.2, 
    {
      scale: 1,
      rotation: '-=10',
      ease: Elastic.easeOut.config(2.5, 0.5),
    })
    this.timeline.to(
      bubblePulse,
      1.3,
      {
        scale: 3,
        opacity: 0,
        ease: Expo.easeOut,
      },
      '-=1.2'
    )
  },
  methods:
  {
    showToggle()
    {
      setTimeout(() => {
        this.show = false
      }, 900);
    }
  }
}

</script>

<style>

/*
*   Bubble Animation
*/

.bubble-wrapper
{
  z-index: 3;
  width: 100vw;
  height: 100vh;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.bubble
{
  z-index: 2;
  width: 150px;
  height: 150px;
  border-radius: 50%;
}

.bubble-pulse 
{
  position: absolute;
  z-index: 1;
  height: 150px;
  width: 150px;
  top: 50%;
  left: 50%;
  margin-left: -75px;
  margin-top: -75px;
  background: #272727;
  border-radius: 50%;
  opacity: 0;
  transform: scale(0);
}

.bubble-image
{
  height: 100%;
}

.fade-enter-active, .fade-leave-active
{
    animation-name: scaleOut;
    animation-duration: .5s;
}

.fade-enter, .fade-leave-to
{
    opacity: 0;
}

@keyframes scaleOut
{
    from
    {
        transform: scale(1);
        opacity: 1;
    }
    to
    {
        transform: scale(0);
        opacity: 0;
    }
}

</style>