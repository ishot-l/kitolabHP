<i18n>
{
    "ja": {
        "お問い合わせ": "お問い合わせ"
    },
    "en": {
        "お問い合わせ": "Contact"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('お問い合わせ')"
        header-level="4">
    </b-jumbotron>
</template>
<script>
export default {
    
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