<i18n>
{
  "ja": {
    "プロジェクト": "プロジェクト"
  },
  "en": {
    "プロジェクト": "Projects"
  }
}
</i18n>
<template>
  <div>
    <!-- タイトル画像 -->
    <b-jumbotron fluid :header="$t('プロジェクト')" header-level="4"></b-jumbotron>

    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <!-- プロジェクト本文 -->
        <b-col md="9">

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
import CardMenuColumn from "@/components/CardMenuColumn.vue";
export default {
  components: {
    CardMenuColumn,
  },
};
</script>
<style scoped>
.jumbotron {
  background-image: url("~assets/projects.jpg");
  background-size: cover;
  background-position: center 60%;
  color: #fff;
}
</style>