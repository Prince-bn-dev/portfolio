<template>
    <div class="mouse-follower" :style="{ left: mouseX + 'px', top: mouseY + 'px' }"></div>
  </template>
  
  <script>
  export default {
    name: 'MouseEffect',
    data() {
      return {
        mouseX: 0,
        mouseY: 0
      }
    },
    mounted() {
      window.addEventListener('mousemove', this.updateMousePosition)
    },
    beforeDestroy() {
      window.removeEventListener('mousemove', this.updateMousePosition)
    },
    methods: {
      updateMousePosition(e) {
        this.mouseX = e.clientX
        this.mouseY = e.clientY
      }
    }
  }
  </script>
  
  <style scoped>
  .mouse-follower {
    position: fixed;
    width: 50px;
    height: 50px;
    background: radial-gradient(circle, rgba(58, 133, 255, 0.788) 0%, rgba(58,134,255,0) 70%);
    border-radius: 50%;
    pointer-events: none;
    transform: translate(-50%, -50%);
    z-index: 9999;
    transition: transform 0.1s ease-out;
  }
  </style>