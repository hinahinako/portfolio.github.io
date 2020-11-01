<template>
  <v-app>
    <!-- 上部ナビゲーションバー -->
    <!-- <v-card class="overflow-hidden"> -->
    <v-app-bar
      app
      flat
      hide-on-scroll
      color="transparent"
      scroll-target="#scrolling-techniques-3"
      dense
    >
      <!-- <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(230,150,190,.7), rgba(250,120,200,.7)"
        ></v-img>
      </template> -->
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
      <!-- <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab to="/">{{ tab1 }}</v-tab>
          <v-tab to="/about">{{ tab2 }}</v-tab>
          <v-tab>{{ tab3 }}</v-tab>
          <v-tab>{{ tab4 }}</v-tab>
          <v-tab>{{ tab5 }}</v-tab>
        </v-tabs>
      </template> -->
    </v-app-bar>
    <!-- </v-card> -->

    <!-- メイン -->
    <v-main class="pa-0 pt-10">
      <v-container fluid class="pa-0">
        <nuxt />
      </v-container>
    </v-main>

    <!-- フッタ -->
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
      // tab1: "TOP",
      // tab2: "ABOUT ME",
      // tab3: "WORK",
      // tab4: "Tech Logs(Blog)",
      // tab5: "Other Logs",
    };
  },
};
</script>
