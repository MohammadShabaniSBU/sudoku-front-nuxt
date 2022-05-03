<template>
  <div class="w-screen h-screen flex justify-center items-center px-48 py-32">
    <div class="w-full h-full bg-red-500 relative overflow-hidden">
      <div id="x" class="h-full w-1/2 origin-center bg-yellow-400 -ml-20 absolute">
      </div>
    </div>
    <div>
      <button @click="toRight" class="bg-blue-600 text-white px-3 py-1 rounded">
        to right
      </button>
      <button @click="toLeft" class="bg-blue-600 text-white px-3 py-1 rounded">
        to left
      </button>
    </div>
  </div>
</template>

<script>
import anime from '../node_modules/animejs/lib/anime.es.js'

export default {
    head()  {
        return {
            title: 'register'
        }
    },
    data() {
      return {
        left: true,
        animation: null,
      }
    },
    mounted() {
      let x = document.getElementById('x')
        this.animation = anime({
            targets: x,
            keyframes: [
              {
                right: "-5rem",
                duration: 1000,
                easing: 'easeInOutQuad'
              },
            ],
            easing: 'linear',
            autoplay: false,
          })
    },
    methods: {
      toRight() {

        this.animation.play()

        this.animation.finished.then(() => {
          this.animation.reverse()
        })
        

        
      },
      toLeft() {
        this.animation.reverse()
      }
  }
}
</script>

<style>

.input {
    @apply border border-2 border-blue-500 rounded px-2 py-1;
}

.label {
    @apply block text-lg my-1;
}

</style>
