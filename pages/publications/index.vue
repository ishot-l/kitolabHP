<i18n>
{
    "ja": {
        "研究業績": "研究業績"
    },
    "en": {
        "研究業績": "Publications"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('研究業績')"
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