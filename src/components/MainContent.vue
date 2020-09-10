<template>
  <div class="main-content" >
    <span class="anchor" id="portfolio"></span>
    <section>
      <project-gallery imageName="mtg-store.png" title="MTG Cards Store" />
        <project-gallery imageName="trello-clone.png" title="Trello Clone" />
          <project-gallery imageName="twitch-bot.png" title="Twitch.tv chatbot" />
    </section>
    <span class="anchor" id="resumee"></span>
    <section>
      <resumee />
    </section>
    <span class="anchor" id="about"></span>
    <section @scroll.passive="onScroll">
      <about-me />
    </section>
  </div>
</template>

<script>
import ProjectGallery from './ProjectGallery.vue'
import Resumee from './Resumee.vue'
import AboutMe from './AboutMe.vue'
export default {
  name: "main-content",

  components: { 
    ProjectGallery,
    Resumee,
    AboutMe
  },

  data(){
    return {
    }
  },

  methods: {
    redirect(url){
      window.location=url;
    },  
    onScroll(){
      console.log("adjwqdoiqwjdiowqdjqoiwd");
    }
  }
}
</script>

<style scoped>
.anchor:target {
  padding-top: 3.3rem;
}
</style>

