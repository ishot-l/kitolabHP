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
          
          <div class="contact-form">
            <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfKA8a9pN9nKUJHgtdB44Mea9GvzrqGAPXCpp7t1t8odNZMHA/viewform?embedded=true" width="100%" height="1200" frameborder="0" marginheight="0" marginwidth="0">読み込んでいます…</iframe>
          </div>
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
.contact-form {
    padding-top: 2rem;
}

</style>