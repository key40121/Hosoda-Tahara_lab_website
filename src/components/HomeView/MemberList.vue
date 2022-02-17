<template>
  <v-card flat class="ma-3 text-xs-center">
    <v-img v-bind:src="memberList.src" aspect-ratio="1"></v-img>
    <v-card-title primary-title>
      <div>
        <h3 class="headline pink--text text--accent-2">{{ memberList.name }}</h3>
        <div>{{ memberList.position }}</div>
      </div>
    </v-card-title>
    <v-card-subtitle>{{ memberList.description }}</v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange lighten-2" text>詳細</v-btn>
      <v-spacer></v-spacer>
      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>
        <v-card-text>
          {{ memberList.description }}
        </v-card-text>
      </div>
    </v-expand-transition>

  </v-card>
</template>

<script>
export default {
  props: ["memberList"],
  data() {
    return {
      show: false,
    };
  }
};
</script>