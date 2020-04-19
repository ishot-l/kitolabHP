<i18n>
{
    "ja": {
        "アクセス": "アクセス",
        "鬼頭研究室": "鬼頭研究室"
    },
    "en": {
        "アクセス": "Access",
        "鬼頭研究室": "Kito Laboratory"
    }
}
</i18n>
<template>
  <div>
    <b-jumbotron
        fluid
        :header="$t('アクセス')"
        header-level="4">
    </b-jumbotron>

    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <b-col md="9" class="mb-2">
          <h3>住所</h3>
          <p class="address">
            〒169-8555<br>
            東京都新宿区大久保3−4−1 早稲田大学 西早稲田キャンパス 51号館14階 <a href="https://goo.gl/maps/xsdLu4uKyw9vB1Gx6" target="_brank">MAP</a>
            <br><br>

            　教授室：14-03A<br>
            学生居室：14-01</p>
          
          <h3>ルート</h3>
          <p class="route">西早稲田キャンパス（西早稲田駅 徒歩0分）までお越しになり、51号館をエレベーターで14階までお上がりください。</p>
          <p class="route"><a href="https://www.waseda.jp/top/assets/uploads/2016/10/20161020nishiwaseda_campus_map.pdf" target="_brank">西早稲田キャンパスマップ</a></p>
          <!-- <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3239.8177151946115!2d139.70488031499738!3d35.706103080188505!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188d2492b7c117%3A0x3b993294bf3846f7!2z5pep56iy55Sw5aSn5a2mIOilv-aXqeeosueUsOOCreODo-ODs-ODkeOCuQ!5e0!3m2!1sja!2sjp!4v1587270364816!5m2!1sja!2sjp" width="600" height="450" frameborder="0" style="border:0; max-width: 100%" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe> -->
        </b-col>

        <b-col md="3">
          <CardMenuColumn />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import CardMenuColumn from '~/components/CardMenuColumn.vue'

export default {
  head() {
    return {
      title: `${this.$t('アクセス')} | ${this.$t('鬼頭研究室')}`
    }
  },
  components: {
    CardMenuColumn
  }
}
</script>
<style scoped>
.jumbotron {
    background-image: url("~assets/contact.jpg");
    background-size: cover;
    background-position: center 60%;
    color: #fff;
}
/* 大見出しデザイン */
h2 {
     position: relative;
     padding:0 0 0.5em 0.7em;
     border-bottom: 1px solid black;
}
h2::after {
     position: absolute;
     top: 0.2em;
     left:0;
     content: '';
     width: 5px;
     height:1em;
     background-color: #446689;
}

/* 小見出しデザイン */
h3 {
	position: relative;
  padding: 0 .3em 0 1.25em;
  font-size: 1.25rem;
  margin-top: 1em;
}
h3::after {
	position: absolute;
	top: .4em;
	left: .3em;
	content: '';
	width: 9px;
	height: 9px;
	background-color: #ff5a5f;
	-webkit-transform: rotate(45deg);
	transform: rotate(45deg);
	z-index: 2;
}

.address {
  padding-left: 1rem;
  padding-right: 1rem;
}

.route {
  padding-left: 1rem;
  padding-right: 1rem;
  text-indent: 1rem;
}
</style>