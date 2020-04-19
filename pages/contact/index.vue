<i18n>
{
    "ja": {
        "お問い合わせ": "お問い合わせ",
        "鬼頭研究室": "鬼頭研究室"
    },
    "en": {
        "お問い合わせ": "Contact",
        "鬼頭研究室": "Kito Laboratory"
    }
}
</i18n>
<template>
  <div>
    <b-jumbotron
        fluid
        :header="$t('お問い合わせ')"
        header-level="4">
    </b-jumbotron>

    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <b-col md="9" class="mb-2">
          
        </b-col>

        <b-col md="3">
          <CardMenuColumn />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import CardMenuColumn from '~/components/CardMenuColumn.vue'

export default {
  head() {
    return {
      title: `${this.$t('お問い合わせ')} | ${this.$t('鬼頭研究室')}`
    }
  },
  components: {
    CardMenuColumn
  }
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/contact.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
</style>