<i18n>
{
    "ja": {
        "研究室紹介": "研究室紹介"
    },
    "en": {
        "研究室紹介": "About"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('研究室紹介')"
        header-level="4">
    </b-jumbotron>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/about.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
</style>