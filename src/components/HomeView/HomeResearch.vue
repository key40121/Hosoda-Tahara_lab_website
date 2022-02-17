<template>
<v-main class="grey lighten-2">
  <v-container class="my-10">
    <!-- <v-container fluid> -->
      <h2>研究について</h2>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2 my-2">研究について</h1>
              <h1 class="font-weight-light display-1 mb-3">
                医療,エネルギー,ロボットなどの革新を目指した研究です
              </h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="../../assets/HomeParallax_images/TEM.jpg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    当研究室では，エネルギー問題や環境を考え,人の役に立つ材料の開発と発展のために,
                    原子・ナノ・マイクロレベルでの材料設計による新・高・多機能材料の創造を目的とし,
                    多種多様な材料開発を行っています.
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="../../assets/HomeParallax_images/TEM.jpg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    異方性制御,原子配列・結晶構造制御,多体相平衡設計,組織設計制御,マイクロメカニクスなど
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="../../assets/HomeParallax_images/TEM.jpg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    構造材料・機能材料・金属材料・有機材料・無機材料・複合材料・センサー・アクチュエーター・形状記憶合金 ・ピエゾ(圧電)材料・生体材料・水素吸蔵合金・高温材料・磁性材料・高電導性材料・皮膜・薄膜・バルク ・プロセス・理論・計算・シミュレーションなど
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="../../assets/HomeParallax_images/TEM.jpg"
                class="d-block ml-auto mr-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    <!-- </v-container> -->
  </v-container>
</v-main>
</template>


<script>
export default {
  data() {
    return {
      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4"
      ],
      slides: ["First", "Second", "Third", "Fourth", "Fifth"]
    };
  }
};
</script>

<style scoped>
</style>