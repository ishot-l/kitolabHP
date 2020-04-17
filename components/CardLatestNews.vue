<i18n>
{
    "ja": {
        "最近のお知らせ": "最近のお知らせ",
        "news1": "Socioeconomic Networks and Network Science Workshop をオンラインにて開催致します。",
        "news2": "当面、鬼頭研の研究活動はオンラインで行います。",
        "news3": "国際会議 NetSci-X が開催されました。ご参加いただいた皆様、ありがとうございました。"
    },
    "en": {
        "最近のお知らせ": "Latest News",
        "news1": "\"Socioeconomic Networks and Network Science Workshop\" will be held online.",
        "news2": "We will conduct research activities online for the time being.",
        "news3": "The international conference NetSci-X was held. Thank you to everyone who participated."
    }
}
</i18n>
<template>
    <b-card :title="$t('最近のお知らせ')">
        <ul>
            <li>{{ $t('news1') }}<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a></li>
            <li><b>{{ $t('news2') }}</b></li>
            <li>{{ $t('news3') }}<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a></li>
        </ul>
    </b-card>
</template>
<script>
export default {
    
}
</script>
<style scoped>
li {
    margin-bottom: 1em;
}
</style>