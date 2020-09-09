<template>
  <div class="main-content">
    <span class="anchor" id="portfolio"></span>
    <section>
      <carousel />
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
import Carousel from './Carousel.vue'
export default {
  name: "main-content",

  components: { Carousel },

  methods: {
    redirect(url){
      window.location=url;
    },
  }
}
</script>

<style scoped>
.main-content {
  margin-top: 3.3rem;
}
.anchor:target {padding-top: 3.3rem;}
</style>

