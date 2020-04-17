<i18n>
{
  "ja": {
    "鬼頭研究室": "鬼頭研究室",
    "研究室ホームページ": "研究室ホームページ",
    "about_here":
      "早稲田大学 理工学術院 創造理工学部 経営システム工学科／大学院経営デザイン専攻　鬼頭研究室のホームページです。",
    "about_here2":
     "この研究室では、「<span style=\"text-decoration:underline\">企業などの組織や人々が、お互いに関わり合いながら経済社会を織り成し、その中でいかに価値を創成・持続していくか？</span>」という、大きな関心を主軸にして、それに関わるさまざまな研究を幅広くおこなっています。"
  },
  "en": {
    "鬼頭研究室": "kitolab",
    "研究室ホームページ": "Labo homepage",
    "about_here":
      "Waseda University Keiei System Kougaku Ka no Homepage desu.",
    "about_here2":
      "Eigo wakarimasen. wakaran wakaran wakaran wakaran wakaran wakaran wakaran wakaran wakaran wakaran "
  }
}
</i18n>
<template>
  <div>
    <!-- トップ画像 -->
    <BillBoard />

    <!-- その下 -->
    <b-container fluid class="mt-2 pb-3">
      <b-row>

        <!-- メイン -->
        <b-col md="9" order-md="2" class="mb-2">
          <b-card class="mb-2">
            <b-card-body>{{ $t('about_here') }}</b-card-body>
            <b-card-body v-html="$t('about_here2')"></b-card-body>
          </b-card>
          <CardLatestNews />
        </b-col>

        <!-- 左カラム -->
        <b-col md="3" order-md="1">
          <CardMenuColumn />
        </b-col>

      </b-row>
    </b-container>

  </div>
</template>


<script>
import Logo from '~/components/Logo.vue'
import BillBoard from '~/components/BillBoard.vue'
import CardLatestNews from '~/components/CardLatestNews.vue'
import CardMenuColumn from '~/components/CardMenuColumn.vue'

export default {
  components: {
    Logo,
    BillBoard,
    CardLatestNews,
    CardMenuColumn
  }
}
</script>

<style scoped>
.card {
  border-radius: 0;
}
.card-header {
  border-bottom: 0;
  border-top: 2px solid rgba(25, 100, 240, 0.7);
}
.card-body {
  text-indent: 1rem;
}
</style>
