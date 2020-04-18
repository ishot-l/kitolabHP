<i18n>
{
    "ja": {
        "Publications": "研究業績"
    },
    "en": {
        "Publications": "Publications"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('Publications')"
        header-level="4">
    </b-jumbotron>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/paper.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
</style>