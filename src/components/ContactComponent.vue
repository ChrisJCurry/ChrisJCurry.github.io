<template>
  <div class="fixed row w-100">
    <h1 class="col-12 mb-5">
      Contact Me!
    </h1>
    <div class="col-3 offset-3">
      <i class="fa fa-envelope h4" aria-hidden="true"></i>
      <h4>contact@chrisjcurry.me</h4>
    </div>
    <div class="col-3">
      <i class="fa fa-linkedin pr-3 h4"></i><br>
      <a href="linkedin.com/in/chrisjcurry/" class="text-light h4">Linkedin
      </a>
    </div>
    <div class="col-3"></div>
  </div>
</template>

<script>
export default {
  name: 'ContactComponent',
  setup() {
    return {

    }
  }

}
</script>

<style scoped lang="scss">
.fixed {
  position: absolute;
  left: 50% !important;
  top: 75% !important;
}
</style>
