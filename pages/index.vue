<template>
  <v-content>
    <section id="about-me">
      <!-- TOP -->
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">はじめまして！</h2>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>

        <v-avatar class="elevation-12 mb-12" size="250">
          <v-img src="/image/hinako.png"></v-img>
        </v-avatar>
        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >
          IT歴2年半のhinako(<a
            href="https://twitter.com/hinatwt503"
            target="_brank"
            >@hinatwt503</a
          >)です。<br />
          SESに転職して2年→フロントエンドの勉強して半年。<br />
          Nuxt.js + Vuetifyが得意です。
        </v-responsive>
        <div></div>
      </v-container>

      <div class="py-6"></div>
      <v-divider></v-divider>
      <div class="py-12"></div>
    </section>

    <section id="profile">
      <!-- 自己紹介 -->
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">自己紹介</h2>
        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>

        <v-row justify="center" class="mx-3">
          <v-col cols="11" md="5">
            <!-- <v-avatar class="elevation-12 mb-12" size="250"> -->
            <v-img src="/image/profile.png" aspect-ratio="1.0"></v-img>
            <!-- </v-avatar> -->
          </v-col>
          <v-col cols="11" md="7" class="text-left">
            <h2 class="mb-4 ml-3">やってきたこと</h2>
            <p>
              ・
              医療事務、兼社内SEを2年経験。院内のIT備品管理やウェブページの更新などを担当。その他にも、来院者管理システム導入の要件定義を手伝うなど、自分が関わりそうなものはなんでも首を突っ込んで色々挑戦させていただきました。
            </p>
            <p>
              ・
              IT一本でやりたくなったのでSIerに転職。お客様は主に金融系でした。RPA、VBA、Java、JavaScriptの設計〜テストをひととおり経験しました。数千行のソースコードを読んで、ひたすら設計書に起こすという作業も経験しました。
            </p>
            <p>
              ・
              現在はキャリアチェンジのためエンジニアスクールに通ってNuxt.jsを触っています。スタートアップ企業の方とチームを組み、Webアプリケーションを作成するなどしました。アジャイル風に開発していたので、お客様の要望を吸い上げながら実装しました。
            </p>
            <h2 class="mb-4 ml-3 mt-10">趣味</h2>
            <p>・ ボードゲーム</p>
            <p>・ 麻雀</p>
            <p>・実家の犬をかまう</p>
          </v-col>
        </v-row>
      </v-container>
      <div class="py-12"></div>
    </section>

    <!-- スキル -->
    <section id="works" class="grey lighten-3">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">スキル</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>

        <v-row>
          <v-col
            v-for="({ icon, title, skills }, i) in experiences"
            :key="i"
            cols="12"
            md="4"
          >
            <v-card class="py-12 px-4" color="grey lighten-5" flat>
              <v-theme-provider dark>
                <div>
                  <v-avatar color="red lighten-2" size="88">
                    <v-icon large v-text="icon"></v-icon>
                  </v-avatar>
                </div>
              </v-theme-provider>
              <v-card-title
                class="justify-center font-weight-black text-uppercase"
                v-text="title"
              ></v-card-title>
              <v-row v-for="({ name, years }, j) in skills" :key="j" cols="12">
                <v-col cols="5" align-self="center">
                  <v-card-subtitle v-text="name"></v-card-subtitle>
                </v-col>
                <v-col cols="3" align-self="center">
                  <v-rating
                    v-model="years"
                    background-color="grey"
                    color="grey darken-2 "
                    length="3"
                    size="14"
                    half-increments
                  ></v-rating>
                </v-col>
                <v-col cols="4" align-self="center">
                  <v-card-subtitle>{{ years }}年 </v-card-subtitle>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-container>

      <div class="py-12"></div>
    </section>

    <!-- ステータス -->
    <section id="stats">
      <v-parallax
        :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
        src="/image/status.png"
      >
        <v-container fill-height>
          <v-row class="mx-auto">
            <v-col
              v-for="[value, title] of stats"
              :key="title"
              cols="12"
              md="4"
            >
              <div class="text-center">
                <div
                  class="display-3 font-weight-black mb-4"
                  v-text="value"
                ></div>

                <div class="title font-weight-regular" v-text="title"></div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-parallax>
    </section>

    <!-- プログラミングクイズ成績 -->
    <section id="blog">
      <div class="py-12"></div>
      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-center">
          プログラミングクイズ成績
        </h2>
        <p class="font-weight-light text-center">
          JavaScriptでプログラミングクイズpaizaに挑戦した記録(2020/9/15時点)
        </p>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>

        <v-row justify="center">
          <v-col cols="10" md="6" class="pa-8">
            <h3 class="font-weight-black text-center mb-4">成績</h3>
            <v-img src="/image/paiza.png" aspect-ratio="1.7"></v-img>
            <div class="title font-weight-light mb-5 text-center"></div>
          </v-col>
          <v-col cols="10" md="6" class="pa-8">
            <h3 class="font-weight-black text-center mb-4">スキルの目安</h3>
            <v-img src="/image/rank.png" aspect-ratio="1.9"></v-img>
            <div class="title font-weight-light mb-5 text-center"></div>
          </v-col>
        </v-row>
        <v-row>
          <p>
            参考:
            <span class="text-decoration-underline">
              <v-btn
                text
                href="https://paiza.jp/challenges/info"
                target="_brank"
                class="red--text text--lighten-2"
              >
                paizaプログラミングスキルチェック</v-btn
              >
            </span>
          </p></v-row
        >
      </v-container>
      <div class="py-12"></div>
    </section>

    <!-- 制作物 -->
    <section id="works" class="grey lighten-3">
      <div class="py-12"></div>
      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">制作物</h2>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>
        <v-card
          v-for="({ src, link, tech, text, title }, i) in works"
          :key="i"
          flat
          height="100%"
          class="my-13"
        >
          <v-row no-gutters class="pa-8">
            <v-col cols="12" md="4" class="pa-0">
              <v-row>
                <v-col v-if="!!link" cols="12">
                  <a :href="link" target="_brank">
                    <v-img
                      :src="src"
                      height="230"
                      aspect-ratio="1.0"
                      eager
                    ></v-img>
                  </a>
                </v-col>
                <v-col v-else cols="12">
                  <v-img
                    :src="src"
                    height="230"
                    aspect-ratio="1.0"
                    eager
                  ></v-img>
                </v-col>
                <v-col cols="1">
                  <v-btn
                    v-if="link"
                    class="ml-n4 font-weight-black"
                    text
                    :href="link"
                    target="_blank"
                    color="red lighten-2"
                  >
                    開く
                    <span>
                      <v-icon>mdi-launch</v-icon>
                    </span>
                  </v-btn>
                  <v-btn v-else class="ml-n4 font-weight-black" text disabled>
                    開く
                    <span>
                      <v-icon>mdi-launch</v-icon>
                    </span>
                  </v-btn>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="1">
              <v-divider
                v-if="$vuetify.breakpoint.mdAndUp"
                vertical
                class="ml-5"
              />
            </v-col>
            <v-col cols="12" md="7" class="text-left align-self-center">
              <h3 class="font-weight-black mb-1" v-text="title"></h3>
              <h3 class="subtitle-1 mb-4" v-text="tech"></h3>
              <div class="subtitle-1 mb-5" v-text="text"></div>
            </v-col>
          </v-row>
        </v-card>
      </v-container>
    </section>

    <!-- 連絡先 -->
    <section id="blog">
      <div class="py-12"></div>
      <v-container>
        <h2 class="display-2 font-weight-bold mb-3 text-center">連絡先</h2>
        <p class="font-weight-light text-center">
          何かありましたらTwitterのDMでご連絡くださいませ！
        </p>
        <v-responsive class="mx-auto mb-12" width="56">
          <v-divider class="mb-1"></v-divider>
          <v-divider></v-divider>
        </v-responsive>

        <v-responsive class="mx-auto mb-12" width="250">
          <a
            href="https://twitter.com/hinatwt503"
            target="_brank"
            class="no-cursor"
          >
            <v-avatar class="mb-12" size="250" color="black">
              <v-img src="/image/hinatwt.png" class="pa-13"></v-img>
            </v-avatar>
          </a>
        </v-responsive>
      </v-container>
      <div class="py-12"></div>
    </section>
  </v-content>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        icon: "mdi-vuejs",
        title: "フロントエンド関連",
        skills: [
          { name: "HTML", years: 2.0 },
          { name: "Pug", years: 0.6 },
          { name: "JavaScript", years: 1 },
          { name: "Nuxt.js", years: 0.6 },
          { name: "Vuetify", years: 0.6 },
        ],
      },
      {
        icon: "mdi-language-java",
        title: "バックエンド関連",
        skills: [
          { name: "Java", years: 1 },
          { name: "node.js", years: 0.3 },
          { name: "Oracle", years: 0.3 },
          { name: "PostgreSQL", years: 0.3 },
          { name: "MySQL", years: 0.3 },
        ],
      },
      {
        icon: "mdi-desktop-mac",
        title: "その他",
        skills: [
          { name: "RPA(BizRobo!)", years: 1.0 },
          { name: "Slack", years: 2.0 },
          { name: "GitHub", years: 0.8 },
        ],
      },
    ],
    stats: [
      ["1,285", "Github contributions"],
      ["60+", "tech blog posts"],
      ["840", "hours work with VSCode"],
    ],
    works: [
      {
        src: "/image/feedbackApp.png",
        link: "",
        title: "社内プレゼン評価アプリケーション",
        tech: "SPA/Nuxt.js/Vuetify/OAuth",
        text:
          "スクールでの学習の一貫でスタートアップ企業の方とチームを組んで作成しました。納品物のためデモページやソースコードは公開しておりません。",
      },
      {
        src: "/image/spa.png",
        link: "https://pj003-nuxt.web.app/",
        title: "人材会社向けWebサイト",
        tech: "SPA/Nuxt.js/Vuetify",
        text:
          "スクールの学習の一貫で、トップページ、メニューページ、ニュースページ、コンタクトページを一人で作成しました。スマホ対応もしています。デザインに重きを置いています。",
      },
      {
        src: "/image/ngword.png",
        link: "",
        tech: "node.js/Express/PostgreSQL/Docker/Sequelize",
        title: "オン飲みで盛り上がる! NGワードゲーム",
        text:
          "個人的に作った遊びです。node.jsとマイグレーションツールを使ってみたくて作成しました。プライベートリポジトリでリファクタ中です..",
      },
      {
        src: "/image/blog.png",
        link: "https://hinahinako.github.io/mypage/archive.html",
        tech: "Jekill/github.io",
        title: "ITに関するTipsをためておくところ",
        text:
          "ブログです。「Qiitaに書くほどでもないけどメモしておきたい」というITのTipsを書いてます。自分用です。",
      },
    ],
  }),
};
</script>

<style>
no-cursor {
  cursor: none !important;
}
</style>

