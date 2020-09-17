<template>
  <div class="container">
    <h1 class="text-center">{{ title }}</h1>
    <div class="img-container">
      <b-img :src="require(`../assets/${imageName}`)" fluid></b-img>
    </div>
    <div class="row">
      <div class="col-1" />
      <div class="col-auto">
        <font-awesome-layers class="fa-stack fa-fw fa-3x" @click="redirect(`${github}`)" alt="twitter link">
          <font-awesome-icon class="icon-background" icon="circle" :style="{color: 'grey'}" />
            <font-awesome-icon class="icon" :icon="['fab', 'github']" />
        </font-awesome-layers>
      </div>
      <div class="col-auto">
        <font-awesome-layers class="fa-stack fa-fw fa-3x" @click="redirect(`${demo}`)" alt="twitter link" v-if="!hideDemo">
          <font-awesome-icon class="icon-background" icon="circle" :style="{color: 'grey'}" />
            <font-awesome-icon class="icon" :icon="['fas', 'globe']" />
        </font-awesome-layers>
      </div>
    </div>
    <hr class="m-0">
  </div>
</template>

<script>
export default {
  name: "project-gallery",
  props: { 
    imageName: String,
    title: String,
    github: String,
    demo: String,
    hideDemo: Boolean
  },
  methods: {
    redirect(url){
      window.location=url;
    },  
  }
}
</script>

<style scoped>
.col-1 { 
  background: none;
}
.fa-stack { 
  height: 1em !important; 
  width: 1em !important;
}
.fa-stack:hover { 
  cursor: pointer;
}
.row { 
  margin: 0.625rem !important;
  padding: 0.625rem !important;
}
.icon { 
  font-size: 2rem;
}
img { 
  text-align: center;
  border: 1px solid rgba(0, 0, 0, 0.1);
}
.img-container {
  margin: auto;
  max-width: 90%;
  padding: 0 3rem;
}
</style>
