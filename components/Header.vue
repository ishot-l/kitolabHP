<i18n>
{
  "ja": {
    "鬼頭研究室": "鬼頭研究室",
    "logo": "logo.png",
    "早稲田大学": "早稲田大学",
    "Home": "トップページ",
    "About": "研究室紹介",
    "Projects": "プロジェクト",
    "Publications": "研究業績",
    "People": "メンバー",
    "News": "お知らせ",
    "Contact": "お問い合わせ",
    "Access": "アクセス"
  },
  "en": {
    "鬼頭研究室": "Kito Lab.",
    "logo": "logo_en.png",
    "早稲田大学": "Waseda University",
    "Home": "Home",
    "About": "About",
    "Projects": "Projects",
    "Publications": "Publications",
    "People": "People",
    "News": "News",
    "Contact": "Contact",
    "Access": "Access"
  }
}
</i18n>
<template>
    <b-navbar toggleable="md">
      <b-navbar-brand :to="localePath('/')">
        <h2>{{ $t('早稲田大学') }}</h2>
        <h1>{{ $t('鬼頭研究室') }}</h1>
      </b-navbar-brand>
      

      <b-navbar-nav class="ml-auto mr-2">
        <b-collapse is-nav class="contacts">
          <b-nav-item :to="localePath('/contact')">{{ $t('Contact') }}</b-nav-item>
          <b-nav-item :to="localePath('/access')">{{ $t('Access') }}</b-nav-item>
        </b-collapse>

        <b-nav-item :to="switchLocalePath('ja')" v-if="$i18n.locale !== 'ja'">日本語</b-nav-item>
        <b-nav-item :to="switchLocalePath('en')" v-if="$i18n.locale !== 'en'">English</b-nav-item>
      </b-navbar-nav>
      <b-navbar-toggle target="sidebar-1">
      </b-navbar-toggle>
      <b-collapse is-nav class="menu-wrapper">
          <ul class="menu">
            <li><nuxt-link :to="localePath('/')">{{ $t('Home') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/about')">{{ $t('About') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/projects')">{{ $t('Projects') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/publications')">{{ $t('Publications') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/people')">{{ $t('People') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/news')">{{ $t('News') }}</nuxt-link></li>
          </ul>
      </b-collapse>
    </b-navbar>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.navbar {
  flex-wrap: wrap;
}

.navbar-toggler {
  border: none;
}

.navbar-brand h1 {
  font-size: 1.5rem;
}

.navbar-brand h2 {
  font-size: .8rem;
  margin-bottom: 0;
  color: gray;
}


.menu-wrapper {
  margin: 0;
  flex-basis: 100%;
  align-self: flex-end;
}

.menu {
    margin: 0;
    padding: 0;
    width: 100%;
    display: table;
    table-layout: fixed;
}
.menu li {
    display: table-cell;
    margin: 0;
}
.menu li a{
  position: relative;
  display: inline-block;
  width: 100%;
  height: 100%;
  padding-top: 15px;
  padding-bottom: 15px;
  text-decoration: none;
  text-align: center;
  transition: .3s;
  overflow: hidden;
  color: #000;
  border-left: 1px solid gray;
}

.menu li:first-child a{
  border-left: 0;
}
.menu li a:hover{
  color: #fff;
}
.menu li a::before {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  content: '';
  width: 120%;
  height: 100%;
  background: #333;
  transform-origin: right top;
  transform: skewX(-30deg) scale(0, 1);
  transition: transform .3s;
}
.menu li a:hover::before {
  transform-origin: left top;
  transform: skewX(-30deg) scale(1, 1);
}

.contacts {
  padding-right: 2rem;
  font-size: .8rem;
}

.contacts .nav-link {
  padding-top: 0;
  padding-bottom: 0;
  color: rgba(0, 0, 0, 1);
}
</style>