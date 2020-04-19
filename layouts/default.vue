<i18n>
{
  "ja": {
    "鬼頭研究室": "鬼頭研究室",
    "メニュー": "メニュー",
    "Home": "トップ",
    "About": "研究室紹介",
    "Projects": "プロジェクト",
    "Publications": "研究業績",
    "People": "メンバー",
    "Contact": "お問い合わせ",
    "News": "お知らせ",
    "Access": "アクセス"
  },
  "en": {
    "鬼頭研究室": "Kito Laboratory",
    "メニュー": "Menu",
    "Home": "Home",
    "About": "About",
    "Projects": "Projects",
    "Publications": "Publications",
    "People": "People",
    "Contact": "Contact",
    "News": "News",
    "Access": "Access"
  }
}
</i18n>
<template>
  <b-container fluid="md" class="shadow">

    <Header />

    <b-sidebar id="sidebar-1" :title="$t('メニュー')" shadow>
      <div class="px-3 py-2">
        <b-list-group flush>
          <b-list-group-item :to="localePath('/')">{{ $t('Home') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/about')">{{ $t('About') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/projects')">{{ $t('Projects') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/publications')">{{ $t('Publications') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/people')">{{ $t('People') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/news')">{{ $t('News') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/access')">{{ $t('Access') }}</b-list-group-item>
          <b-list-group-item :to="localePath('/contact')">{{ $t('Contact') }}</b-list-group-item>
        </b-list-group>
      </div>
    </b-sidebar>

    <nuxt />

    <Footer />

  </b-container>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style scoped>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
}

.bg {
  background-color: gray;
}

.container-md {
  padding-left: 0;
  padding-right: 0;
}
</style>
