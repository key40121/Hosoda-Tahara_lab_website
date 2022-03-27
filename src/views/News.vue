<template>
    <v-container class="my-10">
        <v-row>
            <!-- <p class="text-h4 font-weight-black brown--text">
            ニュース一覧                                                
            </p> -->

            <v-col cols="12" sm="4">
                <v-tabs v-model="tab" 
                vertical slider-color="green">
                    <v-tabs-slider color="green" />
                    <v-tab>
                        <h1 class="text-sm-h6">2022</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-sm-h6">2021</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-sm-h6">2020</h1>
                    </v-tab>
                    <v-tab>
                        <h1 class="text-sm-h6">2019</h1>
                    </v-tab>
                </v-tabs>
            </v-col>

            <v-col cols="12" sm="8">

                <v-tabs-items v-model="tab">

                    <v-tab-item>
                        <v-col col="10" v-for="news in NewsList_2022" :key="news.date">
                            <h1 class="text-sm-h6">{{ news.date }}</h1>
                            <h1 class="text-sm-subtitle-1">{{ news.event }}</h1>
                            <p class="text-sm-body-1">{{ news.description_1 }}</p>
                            <p class="text-sm-body-1">{{ news.description_2 }}</p>
                            <p class="text-sm-body-1">{{ news.description_3 }}</p>
                            <!-- <img :src="getUrl(news.image)"> -->
                            <div v-if="news.image != null">
                                テストテストテスト
                                <!-- <v-img :src="getUrl(news.image)"></v-img> -->
                            </div>
                            <!-- <v-img :src="getUrl(news.image)"></v-img> -->
                            <v-divider></v-divider>
                        </v-col>
                    </v-tab-item>

                    <v-tab-item>
                        <v-col col="10" v-for="news in NewsList_2021" :key="news.date">
                            <h1 class="text-sm-h6">{{ news.date }}</h1>
                            <h1 class="text-sm-subtitle-1">{{ news.event }}</h1>
                            <p class="text-sm-body-1">{{ news.description_1 }}</p>
                            <p class="text-sm-body-1">{{ news.description_2 }}</p>
                            <p class="text-sm-body-1">{{ news.description_3 }}</p>
                            <v-img :src="news.image"></v-img>
                            <v-divider></v-divider>
                        </v-col>
                    </v-tab-item>

                    <v-tab-item>
                        <v-col col="10" v-for="news in NewsList_2020" :key="news.date">
                            <h1 class="text-sm-h6">{{ news.date }}</h1>
                            <h1 class="text-sm-subtitle-1">{{ news.event }}</h1>
                            <p class="text-sm-body-1">{{ news.description_1 }}</p>
                            <p class="text-sm-body-1">{{ news.description_2 }}</p>
                            <p class="text-sm-body-1">{{ news.description_3 }}</p>
                            <v-divider></v-divider>
                        </v-col>
                    </v-tab-item>


                </v-tabs-items>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import NewsList_2022 from '../../src/assets/news_src/jsons/newslist_2022.json'
import NewsList_2021 from '../../src/assets/news_src/jsons/newslist_2021.json'

export default {
  data() {
    return {
        tab: null,
        NewsList_2022: NewsList_2022,
        NewsList_2021: NewsList_2021
      }
    },
    methods: {
        getUrl: function (url) {
            //   return `../../public/news/images/${url}`;
        let img = "../../public/news/images/" + url
        return require(img);
    }
  },
}

</script>