<template>
  <div class="container p-0 m-0">
    <section class="section">
      <div class="oop" @click="toTop">
        Top
      </div>
      <div class="fixed">
        <h1>Chris Curry</h1>
        <h3>Full-stack Software Developer</h3>
      </div>
    </section>
    <section class="section">
      <div class="fixed">
        <h1>Applications</h1>
      </div>
    </section>
    <section class="section">
      <div class="fixed">
        <h1>Contact Me!</h1>
      </div>
    </section>
  </div>
</template>

<script>
import { onMounted, reactive } from 'vue'
export default {
  name: 'Home',
  setup() {
    const state = reactive({
    })
    onMounted(() => {
    })

    return {
      state,
      toTop() {
        window.scrollTo({
          top: 0,
          left: 0,
          behavior: 'smooth'
        })
      }
    }
  }
}
</script>

<style scoped lang="scss">

body {
  background: #222;
  padding: 0;
  margin: 0;
  font-family: 'Sintony', sans-serif;
  font-weight: 300;
  font-size: 13px;
  text-transform: uppercase;
  color: #000;
}

header {
  background-color: rgb(0, 135, 212);
  padding: 0;
  margin: 0;
}

.section {
  text-align: center;
  position: absolute;
  width: 100%;
  height: 50rem;
  letter-spacing: 4px;
  overflow: hidden;
  clip: rect(0, auto, auto, 0);
  .fixed {
    overflow: hidden;
    position: fixed;
    top: 50%;
    left: 50%;
  }
}

@for $i from 1 through 10 {
  .section:nth-child(#{$i}) {
    @if($i==1) {
      background-image: url('../assets/1282257.jpg');
      height: 50rem;
      color: #000;
      top: 0;
    }
    @else if($i==2) {
      background-color: #953bc1;
      color: #fff;
      top: (50rem * ($i - 1));
    }
    @else {
      box-shadow: inset 0 1px 80px rgba(0, 0, 0, 0.14);
      background-color: #5fb0b7;
      color: #fff;
      top: (50rem * ($i - 1));
    }
    z-index: ($i);
    .fixed {
      transform: translate(-50%, -50%);
    }
  }
}

.oop {
  position: fixed;
  z-index: auto;
  width: 100%;
  height: 2rem;
  align-content: center;
  justify-content: center;
  background: linear-gradient(141deg, #48ded4 0%, #a026bf 51%, #e82c75 75%);
}
</style>
