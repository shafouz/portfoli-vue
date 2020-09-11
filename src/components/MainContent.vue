<template>
  <div class="main-content" >
    <span class="anchor" id="portfolio"></span>
    <section>
      <project-gallery imageName="mtg-store.png" title="MTG Cards Store" github="https://github.com/shafouz/mtg-cards-store" demo="http://mtg-cards-store.herokuapp.com/" />
        <project-gallery imageName="trello-clone.png" title="Trello Clone" github="https://github.com/shafouz/portfolio-vue" demo="http://portfolio-joaoluca.herokuapp.com/" />
          <project-gallery imageName="twitch-bot.png" title="Twitch.tv chatbot" github="https://github.com/shafouz/twitch-bot" hideDemo="true" />
    </section>
    <span class="anchor" id="resumee"></span>
    <section>
      <resumee />
    </section>
    <span class="anchor" id="about"></span>
    <section>
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
  }
}
</script>

<style scoped>
.anchor:target {
  padding-top: 3.3rem;
}
</style>

