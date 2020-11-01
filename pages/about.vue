<template>
  <v-content>
    <section id="about-me">
      <!-- ABOUT ME -->
      <v-container class="text-center">
        <!-- <h2 class="display-2 font-weight-bold mb-3">ABOUT ME</h2>
        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive> -->

        <v-row justify="center" class="mx-3">
          <v-col cols="11" md="5">
            <!-- <v-avatar class="elevation-12 mb-12" size="250"> -->
            <v-img src="/image/profile.png" aspect-ratio="1.0"></v-img>
            <!-- </v-avatar> -->
          </v-col>
          <v-col cols="11" md="7" class="text-left">
            <h2 class="mb-4 ml-3">仕事</h2>
            <p>・ 医療事務、兼社内SEを2年</p>
            <p>・ SIerで金融企業のRPA、Java、JSを使った開発を2年経験</p>
            <p>・キャリアチェンジのためエンジニアスクールに6ヶ月通う</p>
            <h2 class="mb-4 ml-3 mt-10">趣味</h2>
            <p>・ ボードゲーム</p>
            <p>・ 麻雀</p>
            <p>・実家の犬をかまう</p>
          </v-col>
        </v-row>
      </v-container>
      <div class="py-12"></div>
    </section>
  </v-content>
</template>

<script>
export default {
  data: () => ({
    articles: [
      {
        src: "/image/blog.png",
        link: "https://hinahinako.github.io/mypage/archive.html",
        title: "myTips",
        text:
          "ITに関するTipsをためておくところとして使っています。ほぼすべて自分用の記事です。",
      },
    ],
    works: [
      {
        icon: "mdi-robot",
        title: "RPA開発・導入",
        text:
          "RPA事業の成長期真っ只中、6人全員初めてRPAに関わるというメンバー構成で新規導入案件に参画。ググっても情報が出ないため、公式ドキュメントを根気よく読む力がつきました。作ったロボットは20体以上。RPA導入プロジェクトのチームリーダーも経験しました。",
      },
      {
        icon: "mdi-language-java",
        title: "銀行システム開発",
        text:
          "地方銀行営業店舗向けのアプリケーション開発と、ネットバンクの預金システム大規模リファクタリング案件に携わりました(Javaを使用)。約2ヶ月間、数千行のソースコードを読んで読んで読みまくって、ひたすら設計書に起こすという作業も経験しました。",
      },
      {
        icon: "mdi-vuejs",
        title: "Webアプリケーション開発",
        text:
          "社内向けプレゼンテーション大会のフィードバックをするWebアプリケーションのフロントエンド開発を担当。2週間で設計、4週間で実装、3週間でテストを終える爆速スケジュール。アジャイル風に開発していたため、お客様の要望を吸い上げながら実装しました。",
      },
    ],
    stats: [
      ["1,285", "Github contributions"],
      ["60+", "tech blog posts"],
      ["840", "hours work with VSCode"],
    ],
  }),
};
</script>

