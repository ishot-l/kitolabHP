<i18n>
{
    "ja": {
        "メンバー": "メンバー"
    },
    "en": {
        "メンバー": "Member"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('メンバー')"
        header-level="4">
    </b-jumbotron>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/member2.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
</style>