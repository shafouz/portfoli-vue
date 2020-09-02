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
    <div class="fa-icons">
      <div class="row mx-md-3">
        <div class="col-md-6 ">
          <font-awesome-layers class="fa-lg" @click="redirect('https://twitter.com/Shafouz')" alt="twitter link">
            <font-awesome-icon icon="circle" size="5x" :style="{color: 'white'}" />
              <font-awesome-icon class="fa-icon" :icon="['fab', 'twitter']" size="3x" />
          </font-awesome-layers>
        </div>
        <div class="col-md-6 ">
          <font-awesome-layers class="fa-lg" @click="redirect('https://github.com/shafouz/')" alt="github link">
            <font-awesome-icon icon="circle" size="5x" :style="{color: 'white'}" /> 
              <font-awesome-icon class="fa-icon" :icon="['fab', 'github']" size="3x" />
          </font-awesome-layers>
        </div>
      </div>
    </div>
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
.fa-icon { margin-left: 1.25rem !important; }
.fa-lg:hover { cursor: pointer; }
.list-icon { vertical-align: sub; margin: 0 10px 0 0; }
.nav-item { display: block ruby; }
</style>
