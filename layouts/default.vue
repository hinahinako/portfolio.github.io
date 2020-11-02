<template>
  <v-app>
    <!-- 上部ナビゲーションバー -->
    <v-app-bar
      app
      flat
      hide-on-scroll
      color="transparent"
      scroll-target="#scrolling-techniques-3"
      dense
    >
      <v-toolbar-title class="font-weight-black red--text text--lighten-2">{{
        title
      }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- ソーシャルアイコン -->
      <v-btn icon href="https://twitter.com/hinatwt503" target="_brank">
        <v-icon color="#03A9F4">mdi-twitter</v-icon>
      </v-btn>
      <v-btn icon href="https://github.com/hinahinako" target="_brank">
        <v-icon color="#263238">mdi-github</v-icon>
      </v-btn>
      <v-btn icon href="https://qiita.com/hinaqiita" target="_brank">
        <v-icon color="#4CAF50">mdi-alpha-q-box</v-icon>
      </v-btn>
    </v-app-bar>

    <!-- メイン -->
    <v-main class="pa-0 pt-10">
      <v-container fluid class="pa-0">
        <nuxt />
      </v-container>
    </v-main>

    <!-- フッター -->
    <v-footer absolute color="grey lighten-3">
      <span>&copy; {{ new Date().getFullYear() }}</span>
      <span class="ml-2">hinako</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      fixed: false,
      title: "Portfolio by hinako",
    };
  },
};
</script>
