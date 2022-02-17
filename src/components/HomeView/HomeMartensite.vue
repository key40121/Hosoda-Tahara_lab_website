<template>
  <v-container class="my-10">
    <v-flex class="display-1 font-weight-black brown--text text-xs-center my-5">最先端・次世代 形状記憶合金の熱エンジン</v-flex>
      <div class="headline mt-3 brown--text font-weight-bold my-5">2つ動画を用意しました！クリックしてご覧ください。</div>
    <v-row>
      <v-col>
        <div>

          <!-- v-hover とv-cardの挙動がよくわからん -->

          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card :elevation="hover ? 16 : 2" :class="{ 'on-hover': hover }">
          <v-img src="../../assets/Martensite_videos/sma_b.jpg" max-width="500px" v-on:click="open"></v-img>
            <v-dialog v-model="dialog">
              <div>
                <h1>a</h1>
                <v-img src="../../assets/Martensite_videos/sma_b.jpg"></v-img>
              </div>
            </v-dialog>
            </v-card>
          </v-hover>


        </div>
      </v-col>
      

      <v-col>
        <div>
          <v-img src="../../assets/Martensite_videos/sma_b.jpg" max-width="500px" v-on:click="open"></v-img>
            <v-dialog v-model="dialog">
              <div>
                <h1>a</h1>
                <v-img src="../../assets/Martensite_videos/sma_b.jpg"></v-img>
              </div>
            </v-dialog>
        </div>
      </v-col>
    </v-row>

  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false
    };
  },
  methods: {
    open: function() {
      this.dialog = true;
    }
  }
};
</script>

<style scoped>
/* .v-card.on-hover.theme--dark
  background-color: rgba(#FFF, 0.8)
  >.v-card__text
    color: #000 */
</style>