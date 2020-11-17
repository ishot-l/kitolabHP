<i18n>
{
    "ja": {
        "最近のお知らせ": "最近のお知らせ"
    },
    "en": {
        "最近のお知らせ": "Latest News"
    }
}
</i18n>
<template>
    <b-card :title="$t('最近のお知らせ')">
        <ul>
            <li v-for="(article, index) in news" :key="index" v-html="article[$i18n.locale]"></li>
        </ul>
    </b-card>
</template>
<script>
import news from '~/data/news.js'

export default {
    data: function() {
        return {
            // 最新3件のニュース
            news: news.slice(0, 3)
        }
    }
}
</script>
<style scoped>
li {
    margin-bottom: 1em;
}
.card {
    border: none;
}
.card-title {
    padding-bottom: 5px;
    border-bottom: 1px solid black;
}
</style>