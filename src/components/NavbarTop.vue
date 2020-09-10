<template>
  <nav class="navbar navbar-dark fixed-top bg-primary navbar-top" v-show="false">
  <div class="container">
    <a class="navbar-brand">
      <span>Joao Luca</span>
    </a>
    <div>
      <b-dropdown id="dropdown-1" text="Dropdown Button" class="m-md-2">
        <b-dropdown-item href="#portfolio">Portfolio</b-dropdown-item>
        <b-dropdown-item href="#resumee">Resumee</b-dropdown-item>
        <b-dropdown-item href="#about">About me</b-dropdown-item>
      </b-dropdown>
    </div>
  </div>
  </nav>
</template>

<script>
export default {
  name: "navbar-top",
}
</script>

<style scoped>
.navbar-top {
  display: none;
  padding: 0rem 2rem !important;
  background-color: #adace5 !important;
}
</style>
