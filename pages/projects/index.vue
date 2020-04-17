<i18n>
{
    "ja": {
        "プロジェクト": "プロジェクト"
    },
    "en": {
        "プロジェクト": "Projects"
    }
}
</i18n>
<template>
    <b-jumbotron
        fluid
        :header="$t('プロジェクト')"
        header-level="4">
    </b-jumbotron>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/projects.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
</style>