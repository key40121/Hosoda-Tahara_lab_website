<template>
  <v-container fluid>
    <!-- <p class="text-sm-h3 mt-5 font-weight-black brown--text text-xs-center">
            研究について                                             
        </p>
    <v-row justify="center" align-content="center">
      <v-col cols="12" sm="8">

        <div>
          <div class="my-5 red" color="#385F73" dark>
            <div class="text-sm-h5">
              研究目的
            </div>
            <p class="text-sm-h6">
              当研究室では，エネルギー問題や環境を考え,人の役に立つ材料の開発と発展のために,
              原子・ナノ・マイクロレベルでの材料設計による新・高・多機能材料の創造を目的とし,
              多種多様な材料開発を行っています.
            </p>
          </div>
          <v-sheet color="#1F7087" dark>
            <div class="text-sm-h5">
              設計・開発手法
            </div>
            <p class="text-sm-h6">
              異方性制御,原子配列・結晶構造制御,多体相平衡設計,組織設計制御,マイクロメカニクスなど
            </p>
          </v-sheet>
          <v-sheet color="#952175" dark>
            <p class="text-sm-h5">
              研究対象
            </p>
            <p class="text-sm-h6">
              構造材料・機能材料・金属材料・有機材料・無機材料・複合材料・
              センサー・アクチュエーター・形状記憶合金 ・ピエゾ(圧電)材料・生体材料・
              水素吸蔵合金・高温材料・磁性材料・高電導性材料・皮膜・薄膜・バルク ・プロセス・
              理論・計算・シミュレーションなど
            </p>
          </v-sheet>
 
        </div>
      </v-col>

      <v-col cols="12" sm="4">
        <v-carousel cycle height="380">
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
      </v-col>

    </v-row>
    <v-row class="mt-10" justify="center">
      <v-btn to="/for_foreigners" color="green" outlined rounded style="font-weight: bold;">
            研究についてもっと詳しく
          </v-btn>
    </v-row>
    <v-row class="mt-10" justify="center">
          <v-btn to="/for_foreigners" color="green" outlined rounded style="font-weight: bold;">
            業績リスト
          </v-btn>
    </v-row> -->

    <v-row justify="center" style="height : 600px;">
      <v-col cols="12" sm="8" md="6" lg="4" xl="3" style="background-color: #FFCDD2">
        column1
      </v-col>
      <v-col cols="12" sm="8" md="6" lg="4" xl="3" style="background-color: #F8BBD0">
      column 2
    </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>

<style scoped>
</style>