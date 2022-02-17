<template>
  <v-main class="grey lighten-2">
    <v-container class="my-5">
      <v-flex class="display-1 font-weight-black brown--text text-xs-center my-5">メンバー紹介</v-flex>
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 v-for="member in memberList" :key="member.id">
        <MemberLists :memberList="member"/>
      </v-flex>
    </v-layout>
    <v-flex class="my-3">
      <v-btn>他のメンバーへ</v-btn>
    </v-flex>
    </v-container>
  </v-main>
</template>

<script>
import MemberLists from "./MemberList";

export default {
  data() {
    return {
      memberList: [
        {
          id: 1,
          name: "細田　秀樹",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
          src: require("../../assets/HomeMember_images/HidekiHosoda.jpg")
        },
        {
          id: 2,
          name: "田原　正樹",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
          src: require("../../assets/HomeMember_images/MasakiTahara.jpg")
        },
        {
          id: 3,
          name: "海瀨　晃",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
          src: require("../../assets/HomeMember_images/HidekiHosoda.jpg")
        },
        {
          id: 4,
          name: "邱　琬婷",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
          src: require("../../assets/HomeMember_images/HidekiHosoda.jpg")
        },
        {
          id: 5,
          name: "Volodymyr Chernenko",
          position: "未来研教授",
          description: "東京工業大学の物質理工学院で教授をしています。",
          src: require("../../assets/HomeMember_images/Chernenko.jpg")
        },
      ]
    };
  },
  components: {
    MemberLists
  }
}

</script>