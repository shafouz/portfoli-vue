<template>
  <div class="sidebar bg-dark">
    <nav class="navbar">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active" @mouseover="setHide(1)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 1" />
            <a class="nav-link">My portfolio</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(2)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 2" />
            <a class="nav-link">Projects</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(3)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 3" /> 
            <a class="nav-link">About me</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "vertical-sidebar",
  data() { return {
    hide: 1,
  }},
  methods: {
    redirect(url){
      window.location=url;
    },
    setHide(num){
      this.hide = num
    }
  }
}
</script>

<style>
.sidebar { height: 100vh !important; }
.navbar { height: 80vh !important; }
.list-icon { vertical-align: sub; margin: 0 10px 0 0; }
.nav-item { display: block ruby; }
</style>
