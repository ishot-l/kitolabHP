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
export default {
    data: function() {
        return {
            news: [
                {
                    "ja": `Socioeconomic Networks and Network Science Workshop をオンラインにて開催致します。<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`,
                    "en": `"Socioeconomic Networks and Network Science Workshop" will be held online.<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`
                },
                {
                    "ja": `当面、鬼頭研の研究活動はオンラインで行います。`,
                    "en": `<b>We will conduct research activities online for the time being.</b>`
                },
                {
                    "ja": `国際会議 NetSci-X が開催されました。ご参加いただいた皆様、ありがとうございました。<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`,
                    "en": `The international conference NetSci-X was held. Thank you to everyone who participated.<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`
                }
            ]
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