<template>
  <div class="sidebar" @scroll.passive="handleScroll">
    <div class="portrait">
      <b-img v-bind="mainProps" rounded="circle"></b-img>
    </div>
    <nav class="navbar">
      <ul>
        <li class="nav-item active" @mouseover="setHide(1)" @scrolltrigger="setHide(1)">
          <img src="../assets/cursor.png" v-if="hide == 1">
          <a class="nav-link" href="#portfolio">My portfolio</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(2)" @scrolltrigger="setHide(2)">
          <img src="../assets/cursor.png" v-if="hide == 2">
          <a class="nav-link" href="#resumee">Projects</a>
        </li>
        <li class="nav-item active" @mouseover="setHide(3)" @scrolltrigger="setHide(3)">
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
      mainProps: { blank: true, blankColor: '#777', width: 150, height: 150, class: 'm1' },
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
console.log(window.scrollY)
      if (window.scrollY < 1650) { this.hide = 1 } else
        if (window.scrollY >= 1650 && window.scrollY < 2500) { this.hide = 2 }
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
