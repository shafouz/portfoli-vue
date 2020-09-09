<template>
  <div class="container-fluid"> 
    <navbar-top></navbar-top>
    <div class="row">
      <div class="position-fixed">
        <vertical-sidebar></vertical-sidebar>
      </div>
      <div class="col-md-3"></div>
      <div class="col-md-9">
        <main-content></main-content>
      </div>
    </div>
    <footer class="bg-bottom footer">
    </footer>
  </div>
</template>

<script>
import MainContent from './components/MainContent.vue'
import VerticalSidebar from './components/VerticalSidebar.vue'
import NavbarTop from './components/NavbarTop.vue'
export default {
  components: { VerticalSidebar, MainContent, NavbarTop }
}
</script>

<style>
@font-face { font-family: Connection; src: url('./assets/ConnectionIi-2wj8.otf'); }
@media only screen and (max-device-width : 1200px) {
  .position-fixed, .col-md-3 {
    display: none !important;
  }
  .navbar-top {
    display: flex !important; 
  }
}
html { 
  scroll-behavior: smooth;
}
body { 
  font-family: Connection, sans-serif !important;
  size: 1rem;
}
.container-fluid {
  padding: 0 !important;
  height: 100vh;
}
.row {
  margin: 0 !important;
}
.position-fixed {
  z-index: 1030;
  background-color: black;
  width: 25vw;
}
.col-md-9 {
  padding: 0px !important;
  margin: auto !important;
}
</style>
