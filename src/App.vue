<template>
  <v-app>
    <v-app-bar color="teal darken-1" dark app clipped-left>

      <v-app-bar-nav-icon @click="drawer = true" class="d-none d-xs-block"></v-app-bar-nav-icon>

      <v-toolbar-title>Hosoda and Tahara Laboratory</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>

        <v-btn text @click="scrollTop(), goToTop()">トップページ</v-btn>

        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn v-on="on" text>研究について<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>
          <v-list>
            <v-list-item v-for="research in researchs" :key="research">
              <v-list-item-content>
                <v-list-item-title>{{ research }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn v-on="on" text>メンバー<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>
          <v-list>
            <v-list-item v-for="member in members" :key="member">
              <v-list-item-content>
                <v-list-item-title>
                  <v-btn text to="/member">メンバー</v-btn>
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn v-on="on" text>実験装置<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>
          <v-list>
            <v-list-item v-for="equipment in equipments" :key="equipment">
              <v-list-item-content>
                <v-list-item-title>
                  <v-btn text to="/equipments">実験装置</v-btn>
                  </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-btn text to="/news">ニュース</v-btn>
        <v-btn text to="/for_foreigners">For Foreigners</v-btn>
        <v-btn text>リンク</v-btn>
        
        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn v-on="on" text>学内<v-icon>mdi-menu-down</v-icon></v-btn>
          </template>
          <v-list>
            <v-list-item v-for="equipment in equipments" :key="equipment">
              <v-list-item-content>
                <v-list-item-title>
                  <v-btn text to="/equipments">実験装置</v-btn>
                  </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>

      </v-toolbar-items>
    </v-app-bar>
    <v-navigation-drawer
        v-model="drawer"
        fixed
        temporary
        class="d-none d-xs-block"
      >
        <v-list
          nav
          dense
        >
          <v-list-item-group>
            <v-list-item>
              <v-list-item-title>HOME</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>ABOUT</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>WORK</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>SERVICE</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>BLOG</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>ACCESS</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>

    <!-- This is a footer -->
    <v-footer color="teal darken-1" dark app>
      Hosoda and Tahara Lab 
    </v-footer>

    <!-- Do not touch -->
    <v-main>
      <transition>
        <router-view></router-view>
      </transition>
    </v-main>

  </v-app>
</template>

<script>
export default {
  data() {
    return {
      researchs : [
        '研究について',
        '業績'
      ],
      members: [
        '現在のメンバー',
        'OBOG・歴史'
      ],
      equipments: [
        '実験装置',
        '共有装置(学内専用)'
      ],
      drawer: false,
    }
  },
  methods: {
    scrollTop() {
      window.scrollTo(0, 0);
    },
    goToTop() {
      this.$router.push('/');
    }
  } 
}
</script>

<style lang="scss" scoped>



.v-enter {
  transform: translate(-100px, 0);
  opacity: 0;
}
.v-enter-to {
  opacity: 1;
}
.v-enter-active {
  transition: all 1s 0s ease;
}
.v-leave {
  transform: translate(0, 0);
  opacity: 1;
}
.v-leave-to {
  transform: translate(100px, 0);
  opacity: 0;
}
.v-leave-active {
  transition: all .5s 0s ease;
}

.v-toolbar__title {
  overflow: visible !important;
  margin-right: 50px !important;
}
 
// .v-app-bar__nav-icon {
//   @include display_pc {
//     display: none !important;
//   }
// }

// .v-tabs {
//   display: none;
 
//   @include display_pc {
//     display: block !important;
//   }
// }

</style>