<i18n>
{
    "ja": {
        "お知らせ": "お知らせ",
        "鬼頭研究室": "鬼頭研究室"
    },
    "en": {
        "お知らせ": "News",
        "鬼頭研究室": "Kito Laboratory"
    }
}
</i18n>
<template>
  <div>
    <b-jumbotron
        fluid
        :header="$t('お知らせ')"
        header-level="4">
    </b-jumbotron>

    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <b-col md="9" class="mb-2">
          <b-card v-for="(article, index) in news" :key="index" class="article">
            <b-card-body class="text-center">
              <b-card-text v-html="article[$i18n.locale]"></b-card-text>
            </b-card-body>
            <b-card-text class="text-right">{{ article['date'] }}</b-card-text>
          </b-card>
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
      title: `${this.$t('お知らせ')} | ${this.$t('鬼頭研究室')}`
    }
  },
  components: {
    CardMenuColumn
  },
  data: function() {
        return {
            news: [
                {
                    "ja": `Socioeconomic Networks and Network Science Workshop をオンラインにて開催致します。<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`,
                    "en": `"Socioeconomic Networks and Network Science Workshop" will be held online.<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`,
                    "date": "2020/04/19"
                },
                {
                    "ja": `<b>当面、鬼頭研の研究活動はオンラインで行います。</b>`,
                    "en": `<b>We will conduct research activities online for the time being.</b>`,
                    "date": "2020/04/06"
                },
                {
                    "ja": `国際会議 NetSci-X が開催されました。ご参加いただいた皆様、ありがとうございました。<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`,
                    "en": `The international conference NetSci-X was held. Thank you to everyone who participated.<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`,
                    "date": "2020/01/25"
                }
            ]
        }
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
.article {
  margin-bottom: 1rem;
  border: none;
  border-radius: 0;
  border-top: 1px dotted black;
}

.article:first-child{
  border-top: none;
}
</style>