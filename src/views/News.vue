<template>
    <v-container class="my-10">
        <v-row>
            <!-- <p class="text-h4 font-weight-black brown--text">
            ニュース一覧                                                
            </p> -->

            <v-col cols="auto">
                <v-tabs v-model="tab" 
                vertical slider-color="green">
                    <v-tabs-slider color="green" />
                    <v-tab>
                        <h1 class="text-h6">2022</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-h6">2021</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-h6">2020</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-h6">2020</h1>
                    </v-tab>
                </v-tabs>
            </v-col>

            <v-col cols="auto">

                <v-tabs-items v-model="tab">

                    <v-tab-item>
                        <v-col col="2">
                            <h1 class="text-sm-h6">2022/01/30</h1>
                        </v-col>
                        <v-col col="10">
                            <h1 class="text-sm-subtitle-1">書籍</h1>
                            <p class="text-sm-body-1">Springer社より書籍"The Plaston Concept"を出版しました。オープンアクセスとなっていますので、以下のリンクよりダウンロードいただけます。</p>
                            <p class="text-sm-body-1">“The Plaston Concept: Plastic Deformation in Structural Materials”  Editors: Isao TANAKA, Nobuhiro Tsuji, Haruyuki INUI, Springer, Singapore (2022)  ISBN 978-981-16-7714-4, 978-981-16-7715-1 (eBook)

                            本研究室教授の辻が"Proposing the Concept of Plaston and Strategy to Manage Both High Strength and Large Ductility in Advanced Structural Materials, on the Basis of Unique Mechanical Properties of Bulk Nanostructured Metals"と題された章を執筆しました。</p>
                                
                        </v-col>
                        <v-divider></v-divider>
                        <v-col col="2">
                            <h1 class="text-h6">2022/01/30</h1>
                        </v-col>
                        <v-col col="10">
                            書籍
                                Springer社より書籍"The Plaston Concept"を出版しました。オープンアクセスとなっていますので、以下のリンクよりダウンロードいただけます。

                                        “The Plaston Concept: Plastic Deformation in Structural Materials”  Editors: Isao TANAKA, Nobuhiro Tsuji, Haruyuki INUI, Springer, Singapore (2022)  ISBN 978-981-16-7714-4, 978-981-16-7715-1 (eBook)

                            本研究室教授の辻が"Proposing the Concept of Plaston and Strategy to Manage Both High Strength and Large Ductility in Advanced Structural Materials, on the Basis of Unique Mechanical Properties of Bulk Nanostructured Metals"と題された章を執筆しました。
                        </v-col>
                        <v-divider></v-divider>

                        

                    </v-tab-item>

                    <v-tab-item>
                        <v-col col="2">
                            <h1 class="text-h6">2022/01/30</h1>
                        </v-col>
                        <v-col col="10">
                            書籍
                                Springer社より書籍"The Plaston Concept"を出版しました。オープンアクセスとなっていますので、以下のリンクよりダウンロードいただけます。

                                        “The Plaston Concept: Plastic Deformation in Structural Materials”  Editors: Isao TANAKA, Nobuhiro Tsuji, Haruyuki INUI, Springer, Singapore (2022)  ISBN 978-981-16-7714-4, 978-981-16-7715-1 (eBook)

                            本研究室教授の辻が"Proposing the Concept of Plaston and Strategy to Manage Both High Strength and Large Ductility in Advanced Structural Materials, on the Basis of Unique Mechanical Properties of Bulk Nanostructured Metals"と題された章を執筆しました。
                        </v-col>
                        <v-divider></v-divider>
                    </v-tab-item>


                </v-tabs-items>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>

export default {
  data() {
    return {
        tab: null,
        NewsFeed: [
        {
          id: 1,
          name: "細田　秀樹",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
        },
        {
          id: 2,
          name: "田原　正樹",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
        },
        {
          id: 3,
          name: "海瀨　晃",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
        },
        {
          id: 4,
          name: "邱　琬婷",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",

        },
        {
          id: 5,
          name: "Volodymyr Chernenko",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
        //   src: require("../../assets/HomeMember_images/Chernenko.jpg")
        },
      ]
    };
  },
}

</script>