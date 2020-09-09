<template>
  <div class="carousel">
    <div class="img-container my-3">
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
        >
        <!-- Text slides with image -->
        <b-carousel-slide
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          img-src="https://picsum.photos/1024/480/?image=52"
          ></b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide :img-src="require('../assets/mtg-store.png')">
          <h1>Hello world!</h1>
        </b-carousel-slide>

        <!-- Slides with image only -->
        <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>

        <!-- Slides with img slot -->
        <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
        <b-carousel-slide>
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="https://picsum.photos/1024/480/?image=55"
              alt="image slot"
              >
          </template>
        </b-carousel-slide>

        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
          <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
          a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
          </p>
        </b-carousel-slide>
      </b-carousel>
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
  name: "carousel",
}
</script>

<style scoped>
.col-md-1 { 
  background: none 
}
.fa-stack { 
  height: 1em !important; 
  width: 1em !important;
}
.fa-stack:hover { 
  cursor: pointer;
}
.row { 
  margin: 15px !important;
  padding: 15px !important;
}
.icon { 
  font-size: 2rem;
}
img { 
  height: 100%;
  width: 100%;
}
.img-container {
  height: 25rem;
  width: 50rem ;
  margin: auto;
  padding: 15px;
}
</style>
