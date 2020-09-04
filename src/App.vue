<template>
  <div class="container-fluid"> 
    <div class="row">
      <div class="col-md-3 position-fixed">
        <div class="row">
          <div class="col-md-11">
            <vertical-sidebar></vertical-sidebar>
          </div>
          <div class="col-md-1">
          </div>
        </div>
      </div>
      <div class="col-md-3">
      </div>
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
export default {
  components: { VerticalSidebar, MainContent }
}
</script>

<style>
@font-face { font-family: Connection; src: url('./assets/ConnectionIi-2wj8.otf'); }

body { 
  font-family: Connection, sans-serif !important;
}
.container-fluid {
  padding: 0 !important;
  height: 100vh;
  background: url("./assets/ground.png"), url("./assets/sky.png"); 
  background-repeat: repeat-x;
  background-size: 10%, cover;
  background-position: bottom, top;
}
.row {
  margin: 0 !important;
}
.position-fixed {
  padding: 0px !important;
}
.col-md-11, .col-md-1 {
  padding: 0px !important;
}
.col-md-11 {
  background-image: url("./assets/woodbg.png") !important;
}
.col-md-1 {
  background-image: url("./assets/block2.png");
  background-repeat: repeat-y;
}
.col-md-9 {
  margin-left: 25vw !important;
  padding: 0px !important;
}
</style>
