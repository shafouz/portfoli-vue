<template>
  <div class="sidebar ">
    <nav class="navbar">
      <ul class="">
        <li class="nav-item active" @mouseover="setHide(1)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 1" />
            <p class="nav-link">My portfolio</p>
        </li>
        <li class="nav-item active" @mouseover="setHide(2)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 2" />
            <p class="nav-link">Projects</p>
        </li>
        <li class="nav-item active" @mouseover="setHide(3)">
          <font-awesome-icon class="list-icon" :icon="['fas', 'chevron-right']" size="1x" v-if="hide == 3" /> 
            <p class="nav-link">About me</p>
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
p { color: white; text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; }
.sidebar { height: 100vh !important; }
.navbar { height: 80vh !important; }
.navbar-nav { padding: 20px; }
.list-icon { vertical-align: sub; margin: 0 10px 0 0; }
.nav-item { display: block ruby; }
</style>
