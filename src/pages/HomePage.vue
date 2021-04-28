<template>
  <div class="oop text-center" @click="toTop">
    <h2>Top</h2>
  </div>
  <div class="container p-0 m-0">
    <section class="section">
      <MainComponent />
    </section>
    <section class="section">
      <ApplicationComponent />
    </section>
    <section class="section">
      <ContactComponent />
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

.section {
  text-align: center;
  position: absolute;
  width: 100%;
  height: 50rem;
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
      background: linear-gradient(to bottom, rgba(255,255,255,0) 90%,
              rgba(77, 211, 211, 1)), url('../assets/Personal.jpg');
      background-size: cover;
      height: 100vh;
      color: #000;
      top: 0;
    }
    @else if($i==2) {
      background: linear-gradient(#4dd3d3, #9b30c0);
      color: #fff;
      @media screen and (max-width: 768px) {
          height: 350vh;
      }
      @media screen and (max-width: 1200px) {
          height: 250vh;
      }
      @media screen and (min-width: 1200px) {
          height: 100vh;
      }

      top: (100vh * ($i - 1));
    }
    @else {
      background: linear-gradient(#9b30c0, #9b30c0);
      color: #fff;
      @media not screen and (min-width: 640px) {
        top: 350vh;
      }
      @media screen and (min-width: 640px) {
          top: (125vh * ($i - 1));
      }
      @media screen and (min-width: 768px) {
          top: (120vh * ($i - 1));
      }
      @media screen and (min-width: 968px) {
          top: (120vh * ($i - 1));
      }
      @media screen and (min-width: 1100px) {
          top: (15vh * ($i - 1));
      }
      @media screen and (min-width: 1200px) {
          top: (150vh * ($i - 1));
      }
      @media screen and (min-width: 1200px) {
          top: (100vh * ($i - 1));
      }

      height: 50vh;
    }
    z-index: ($i);
    .fixed {
      transform: translate(-50%, -50%);
    }
  }
}

.oop {
  position: fixed;
  z-index: 99;
  width: 100%;
  height: 5vh;
  align-content: center;
  justify-content: center;
  background: linear-gradient(141deg, #48ded4 0%, #a026bf 51%, #e82c75 75%);
}

</style>
