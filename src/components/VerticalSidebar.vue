<template>
  <div class="sidebar ">
    <nav class="navbar">
      <ul class="">
        <li class="nav-item active" @mouseover="setHide(1)">
          <img src="../assets/cursor.png" v-if="hide == 1">
          <p class="nav-link">My portfolio</p>
        </li>
        <li class="nav-item active" @mouseover="setHide(2)">
          <img src="../assets/cursor.png" v-if="hide == 2">
          <p class="nav-link">Projects</p>
        </li>
        <li class="nav-item active" @mouseover="setHide(3)">
          <img src="../assets/cursor.png" v-if="hide == 3">
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
p { 
  color: white; 
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.sidebar { 
  height: 100vh !important; 
}
.navbar { 
  height: 80vh !important; 
}
.navbar-nav { 
  padding: 20px; 
}
.nav-item { 
  display: block ruby; 
}
.nav-link { 
  padding: 0 .45rem !important;
}
</style>
