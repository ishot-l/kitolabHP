<i18n>
{
  "ja": {
    "メニュー": "メニュー",
    "Home": "トップ",
    "About": "研究室紹介",
    "Projects": "プロジェクト",
    "Publications": "研究業績",
    "People": "メンバー",
    "Contact": "お問い合わせ"
  },
  "en": {
    "メニュー": "Menu",
    "Home": "Home",
    "About": "About",
    "Projects": "Projects",
    "Publications": "Publications",
    "People": "People",
    "Contact": "Contact"
  }
}
</i18n>
<template>
    <b-card>
        <b-card-header>
            {{ $t('メニュー') }}
        </b-card-header>
        <b-list-group flush>
            <b-list-group-item :to="localePath('/')">{{ $t('Home') }}</b-list-group-item>
            <b-list-group-item :to="localePath('/about')">{{ $t('About') }}</b-list-group-item>
            <b-list-group-item :to="localePath('/projects')">{{ $t('Projects') }}</b-list-group-item>
            <b-list-group-item :to="localePath('/publications')">{{ $t('Publications') }}</b-list-group-item>
            <b-list-group-item :to="localePath('/People')">{{ $t('People') }}</b-list-group-item>
            <b-list-group-item :to="localePath('/contact')">{{ $t('Contact') }}</b-list-group-item>
        </b-list-group>
    </b-card>
</template>
<script>
export default {
}
</script>
<style scoped>
.card {
  border-radius: 0;
}
.card-header {
  border-bottom: 0;
  border-top: 2px solid rgba(25, 100, 240, 0.7);
}
</style>