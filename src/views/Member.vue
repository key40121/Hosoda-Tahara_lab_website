<template>
<v-content>
    <v-container class="my-5">
    <v-row>
        <v-col>
            <v-card>
                <v-list>
                    <template v-for="(item, index) in items">
            <v-subheader
              v-if="item.header"
              :key="item.header"
            >
              {{ item.header }}
            </v-subheader>
            <v-divider
              v-else-if="item.divider"
              :key="index"
              :inset="item.inset"
            ></v-divider>
            <v-list-item
              v-else
              :key="item.title"
            >
            <v-avatar class="ma-3"
                size="250"
                tile>
                <v-img :src="item.src"></v-img>
            </v-avatar>

              <v-list-item-content>

                <v-list-item-title v-html="item.title"></v-list-item-title>
                <v-list-item-subtitle v-html="item.name_english"></v-list-item-subtitle>
                <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>

                <v-card-text class="text--primary">
                    <div v-html="item.department"></div>
                    <div v-html="item.research"></div>
                </v-card-text>

              </v-list-item-content>
            </v-list-item>
          </template>

          <vue-card>

          </vue-card>



                </v-list>
            </v-card>
        </v-col>
    </v-row>



    </v-container>
  </v-content>
</template>

<script>
  export default {
    data: () => ({
      items: [
        { header: '教員一覧' },
        { src:require("../assets/HomeMember_images/HidekiHosoda.jpg"), title: '細田　秀樹', name_english: "Hideki Hosoda", department: "教授(物質理工学院)", research: "専門分野：形状記憶合金，コンポジット", room: "R2-917" },
        { divider: true, inset: false },
        { src:require("../assets/HomeMember_images/HidekiHosoda.jpg"), title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>', subtitle: `<span class="font-weight-bold">to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend.` },
        { divider: true, inset: false },
        { src:require("../assets/HomeMember_images/HidekiHosoda.jpg"), title: 'Oui oui', subtitle: '<span class="font-weight-bold">Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?' },
      ],
    }),
  }
</script>