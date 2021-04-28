<template>
  <div class="row w-100">
    <h1 class="col-12">
      Applications
    </h1>
    <div class="col-12 col-xs-6 col-md-6 p-2 m-3">
      <div class="card text-dark card-shadow">
        <div class="card-title">
          <h2>Proper</h2>
        </div>
        <div class="card-text">
          <h4>
            A program designed for Property Management companies to handle their rental properties easily and efficiently.
          </h4>
        </div>
        <div class="card-text">
          <h3>Technologies Used:</h3>
          <h5 class="row">
            <div class="col-6 pr-0 mr-0">
              <ul>
                <li>Vue.js</li>
                <li>Node.js/<br>Express</li>
                <li>MongoDb</li>
              </ul>
            </div>
            <div class="col-6 pl-0 ml-0">
              <ul>
                <li>HTML5/CSS3</li>
                <li>Javascript</li>
                <li>Firebase</li>
              </ul>
            </div>
          </h5>
        </div>
        <div class="card-text">
          <a href="https://github.com/ChrisJCurry/proper" target="_blank" class="text-dark"><button class="btn btn-primary">Proper</button></a>
        </div>
      </div>
    </div>
    <div class="col-12 col-md-4 p-2 m-3">
      <div class="card card-shadow text-dark">
        <div class="card-title">
          <h2>Keepr</h2>
        </div>
        <div class="card-text">
          <h4>
            An application designed to upload, share, and collect images in a social media-like manner.
          </h4>
        </div>
        <div class="card-text">
          <h3>Technologies Used:</h3>
          <h5 class="row">
            <div class="col-6 pr-0 mr-0">
              <ul>
                <li>Vue.js</li>
                <li>MySQL</li>
                <li>C#/.NET</li>
              </ul>
            </div>
            <div class="col-6 pl-0 ml-0">
              <ul>
                <li>HTML5/CSS3</li>
                <li>Javascript</li>
              </ul>
            </div>
          </h5>
        </div>
      </div>
    </div>
    <div class="col-4">
      test
    </div>
  </div>
</template>

<script>
export default {
  name: 'ApplicationComponent',
  setup() {
    return {

    }
  }

}
</script>

<style scoped lang="scss">
.card {
  border-radius: 5%;
}
.card-shadow {
  box-shadow: 5px 5px 5px black;
}
</style>
