<i18n>
{
  "ja": {
    "鬼頭研究室": "鬼頭研究室",
    "早稲田大学": "早稲田大学",
    "Home": "トップページ",
    "About": "研究室紹介",
    "Projects": "プロジェクト",
    "Publications": "研究業績",
    "People": "メンバー",
    "Contact": "お問い合わせ"
  },
  "en": {
    "鬼頭研究室": "Kito Laboratory",
    "早稲田大学": "Waseda University",
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
    <b-navbar toggleable="md">
      <b-navbar-brand :to="localePath('/')">
        {{ $t('早稲田大学') }}<br>
        {{ $t('鬼頭研究室') }}
      </b-navbar-brand>
      

      <b-navbar-nav class="ml-auto mr-2">
          <b-nav-item :to="switchLocalePath('ja')" v-if="$i18n.locale !== 'ja'">日本語</b-nav-item>
          <b-nav-item :to="switchLocalePath('en')" v-if="$i18n.locale !== 'en'">English</b-nav-item>
      </b-navbar-nav>
      <b-navbar-toggle class="border-none">
        <a v-b-toggle.sidebar-1>
          三
        </a>
      </b-navbar-toggle>
      <b-collapse is-nav class="menu-wrapper">
          <ul class="menu">
            <li><nuxt-link :to="localePath('/')">{{ $t('Home') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/about')">{{ $t('About') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/projects')">{{ $t('Projects') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/publications')">{{ $t('Publications') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/People')">{{ $t('People') }}</nuxt-link></li>
            <li><nuxt-link :to="localePath('/contact')">{{ $t('Contact') }}</nuxt-link></li>
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
</style>