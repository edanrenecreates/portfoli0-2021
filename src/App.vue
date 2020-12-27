<template>
  <div id="app">
    <div class="nav">
      <b-navbar
        class="navbar-wrapper"
        toggleable="lg"
        type="light"
        variant="light"
      >
        <b-navbar-brand href="#">
          <img
            src="./assets/img/logo-tagline.png"
            alt="Logo"
            width="150"
          />
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" class="ml-auto" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class='ml-auto'>
            <b-nav-item href="#">Home</b-nav-item>
            <b-nav-item href="#">About</b-nav-item>
            <b-nav-item href="#">My Work</b-nav-item>
            <b-nav-item href="#">About</b-nav-item>
            <b-nav-item href="#">Blog</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <div>
      <b-jumbotron id="jumbotron">
        <div class="outline"></div>
        <video autoplay muted loop id='my-video'>
        <source src='./assets/video/hero-bg-video.mp4' type="video/mp4">
        </video>
        <template #header class="hero-logo">
          <img src="./assets/img/logo-tagline.png" alt="logo" width='300'>
        </template>
        <div class="shape-wrapper">
          <img class='homepage-shape' src="./assets/img/homepage shape.svg"/>
        </div>
        <b-button variant="primary" href="#">Do Something</b-button>
        <b-button variant="success" href="#">Do Something Else</b-button>
      </b-jumbotron>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {},
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  outline: none;
}

.navbar-wrapper {
  height: 80px;
  width: 100vw;
}

#my-video {
  position: fixed;
  right: 0;
  top: 0;
  min-width: 100%;
  min-height: 100%;
  z-index: -5;
  opacity: 90%;
}

#jumbotron {
  position: relative;
  background-color: transparent;
}

.outline {
  position: absolute;
  top: 10px;
  right: 30;
  border: 3px solid #627c85;
  width: 95vw;
  height: 90vh;
  z-index: 10;
}

</style>
