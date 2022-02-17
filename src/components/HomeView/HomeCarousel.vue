<template>
  <v-carousel cycle height="750" hide-delimiter-background show-arrows-on-hover>
    <v-carousel-item v-for="image in images" :key="image.id" :src="image.src">
      <v-row v-if="image.id == 1" class="fill-height" align="center" justify="center">
        <div>
          <h1 class="white--text mb-2 display-1 text-xs-center" style="font-weight: 900; text-shadow: 3px 2px #000000">
            細田・田原研究室へようこそ
          </h1>
        </div>
      </v-row>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          id: 1,
          name: "ob pictures",
          src: require("../../assets/HomeCarousel_images/ob.jpg")
        },
        {
          id: 2,
          name: "microstructure",
          src: require("../../assets/HomeCarousel_images/temp1.jpg")
        },
        {
          id :3,
          name: "",
          src: require("../../assets/HomeCarousel_images/temp2.jpg")
        },
      ]
    };
  }
}
</script>