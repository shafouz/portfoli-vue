<template>
  <div class="sidebar">
    <div class="portrait">
      <b-img rounded="circle" v-bind="mainProps"></b-img>
    </div>
    <nav class="navbar">
      <ul>
        <li class="nav-item active" @mouseover="setHide(1)">
          <img src="../assets/cursor.png" v-if="hide == 1">
          <a class="nav-link" href="#portfolio">Testing stuff</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(2)">
          <img src="../assets/cursor.png" v-if="hide == 2">
          <a class="nav-link" href="#resumee">Projects</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(3)">
          <img src="../assets/cursor.png" v-if="hide == 3">
          <a class="nav-link" href="#about">About me</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "vertical-sidebar",
  data() { 
    return {
      hide: 1,
      mainProps: { width: 170, height: 170, class: 'm1', src: "pluto.jpg" },
      windowY: null,
    }
  },
  methods: {
    redirect(url){
      window.location=url;
    },
    setHide(num){
      this.hide = num
    },
    handleScroll(){
      if (window.scrollY < 1500) { this.hide = 1 } else
        if (window.scrollY >= 1500 && window.scrollY < 2500) { this.hide = 2 }
      else { this.hide = 3 }
    }
  }, 
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>

<style scoped>
a { 
  color: white !important; 
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; 
}
a:hover {
  color: white !important;
}
.sidebar { 
  text-align: center;
  height: 100vh !important; 
  padding: 1.25rem;
  margin: 0.625rem;
}
.portrait {
  padding: 0.625rem;
  margin: 0.625rem;
  margin-bottom: 2rem;
}
.nav-item { 
  display: block ruby; 
  text-align: start;
}
ul {
  list-style-type: none !important;
  width: 100%;
  margin: 1.25rem;
  padding: 0;
}
.navbar {
  margin: 0.625rem;
}
</style>
