<i18n>
{
  "ja": {
    "鬼頭研究室": "鬼頭研究室",
    "研究室ホームページ": "研究室ホームページ",
    "about_here":
      "早稲田大学 理工学術院 創造理工学部 経営システム工学科／大学院経営デザイン専攻　鬼頭研究室のホームページです。<br><br>　この研究室では、「<span style=\"text-decoration:underline\">企業などの組織や人々が、お互いに関わり合いながら経済社会を織り成し、その中でいかに価値を創成・持続していくか？</span>」という、大きな関心を主軸にして、それに関わるさまざまな研究を幅広くおこなっています。"
  },
  "en": {
    "鬼頭研究室": "Kito Laboratory",
    "研究室ホームページ": "Labo homepage",
    "about_here":
      "At the <b>Complex Systems, Value Creation and Network Science Lab</b> (<b>Kito Lab</b>) at Waseda University (Department of Industrial & Management Systems Engineering, School of Science and Engineering / Department of Business Design), our primary research interest is in how people, companies, and organizations interact with each other to formulate an economy or a society and create value within."
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
        <b-col md="9" class="mb-2">
          <b-card class="mb-2 message">
            <b-card-body v-html="$t('about_here')"></b-card-body>
          </b-card>
          <CardLatestNews />
        </b-col>

        <!-- 右カラム -->
        <b-col md="3">
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
  head() {
    return {
      title: `${this.$t('鬼頭研究室')}`
    }
  },
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
.message{
  border: none;
}
</style>
