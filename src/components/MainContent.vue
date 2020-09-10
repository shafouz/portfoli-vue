<template>
  <div class="main-content">
    <span class="anchor" id="portfolio"></span>
    <section>
      <project-gallery imageName="mtg-store.png" title="MTG Cards Store" />
      <project-gallery imageName="trello-clone.png" title="Trello Clone" />
      <project-gallery imageName="twitch-bot.png" title="Twitch.tv chatbot" />
    </section>
    <span class="anchor" id="resumee"></span>
    <section>
    </section>
    <span class="anchor" id="about"></span>
    <section>
    </section>
      </div>
</template>

<script>
import ProjectGallery from './ProjectGallery.vue'
export default {
  name: "main-content",

  components: { ProjectGallery },

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

