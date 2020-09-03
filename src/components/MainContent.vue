<template>
  <div>
    <div class="row">
      <div class="img-container my-3">
        <h1>Magic The Gathering store</h1>
        <img src="../assets/mtg-store.png">
      </div>
    </div>
    <div class="row">
      <div class="col-md-1" />
        <div class="col-md-1">
          <font-awesome-layers class="fa-stack fa-fw fa-3x" @click="redirect('https://github.com/Shafouz')" alt="twitter link">
            <font-awesome-icon class="icon-background" icon="circle" :style="{color: 'grey'}" />
              <font-awesome-icon class="icon" :icon="['fab', 'github']" />
          </font-awesome-layers>
        </div>
        <div class="col-md-1">
          <font-awesome-layers class="fa-stack fa-fw fa-3x" @click="redirect('https://twitter.com/Shafouz')" alt="twitter link">
            <font-awesome-icon class="icon-background" icon="circle" :style="{color: 'grey'}" />
              <font-awesome-icon class="icon" :icon="['fas', 'globe']" />
          </font-awesome-layers>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "main-content",

  methods: {
    redirect(url){
      window.location=url;
    },
  }
}
</script>

<style scoped>
.img-container { height: 25rem ; width: 50rem ; margin: auto; padding: 15px; }
img { height: 100%; width: 100%; }
.row { margin: 15px !important; padding: 15px !important; }
.icon { font-size: 2rem; }
</style>

