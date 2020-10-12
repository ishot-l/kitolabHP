<i18n>
{
    "ja": {
        "Q&A": "Q&A",
        "鬼頭研究室": "鬼頭研究室"
    },
    "en": {
        "お知らせ": "Q&A",
        "鬼頭研究室": "Kito Laboratory"
    }
}
</i18n>

<template>
  <div>
    <b-jumbotron
        fluid
        :header="$t('Q&A')"
        header-level="4">
    </b-jumbotron>

    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <b-col md="9" class="mb-2">
          <h2>研究室についてのQ&A</h2>
          <p>研究室公開の際によく寄せられた質問をまとめました。</p>

          <h3>ゼミの頻度はどのくらいですか？</h3>
          <p>
            基本は関心の近いグループごとのゼミが週1で1～2コマ、月に1度ほど全体のゼミが行われます。<br>
            その他有志で勉強会を行っています。
          </p>

          <h3>卒業論文のテーマはどのように決めますか？</h3>
          <p>自分で興味のあるテーマを持ち込む人も、先生に与えてもらう人もいます。やりたいことがあれば自由にできます！</p>
        
          <h3>卒論テーマを決めるまでの過ごし方</h3>
          <p>
            ネットワーク科学についての本の輪読や、実データを対象としたデータ分析の実践によって勉強を行います。<br>
            卒論テーマを決める時期が決まっているわけではないので、自分で進めていきたい人はどんどん進めることが可能です。
          </p>

          <h3>プログラミングは必須ですか？どのような言語を使用しますか？</h3>
          <p>
            ほとんどの研究では使用しています。PythonやR、Netlogo等を使用します。<br>
            少しずつ慣れていくための時間も、先生や先輩によるサポートもあるので自信がない人でも大丈夫です！
          </p>

          <h3>データ解析をやる人もいますが？</h3>
          <p>
            研究の進め方は基本データ解析かシミュレーションで行います。
          </p>

          <h3>研究室のイベントは多いですか？</h3>
          <p>
            比較的に多くはない方だと思います。<br>
            しかし研究室内での交流は重要と考えるので、そのような機会は設けています！
          </p>

          <h3>ゼミでは何を行うのですか？</h3>
          <p>
            基本は研究の進捗を報告し、先生や他のメンバーから意見をもらったりします。<br>
            その他興味のある内容があれば勉強会を開くことができます。
          </p>

          <h3>サプライチェーン以外の研究を行っていますか？</h3>
          <p>交通系や企業経営、心理学実験など、さまざまな研究を行っている人がいます。</p>

          <h3>学会発表はありますか？</h3>
          <p>あります。2020年1月にはNetSciXという学会でB4の2人が発表しました。</p>

          <h3>GPAはどのくらい必要ですか？</h3>
          <p>年によって変わります。一昨年は第一志望で出せば通ったのですが、去年は結構高かったようです。</p>


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
      title: `${this.$t('Q&A')} | ${this.$t('鬼頭研究室')}`
    }
  },
  components: {
    CardMenuColumn
  },
  data: function() {
        return {
            news: [
                {
                    "ja": `Socioeconomic Networks and Network Science Workshop をオンラインにて開催致します。<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`,
                    "en": `"Socioeconomic Networks and Network Science Workshop" will be held online.<br><a href="https://sites.google.com/view/socioeco-netsci-waseda2020" target="_blank">https://sites.google.com/view/socioeco-netsci-waseda2020</a>`,
                    "date": "2020/04/19"
                },
                {
                    "ja": `<b>当面、鬼頭研の研究活動はオンラインで行います。</b>`,
                    "en": `<b>We will conduct research activities online for the time being.</b>`,
                    "date": "2020/04/06"
                },
                {
                    "ja": `国際会議 NetSci-X が開催されました。ご参加いただいた皆様、ありがとうございました。<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`,
                    "en": `The international conference NetSci-X was held. Thank you to everyone who participated.<br><a href="https://netscix2020tokyo.github.io/" target="_blank">https://netscix2020tokyo.github.io/</a>`,
                    "date": "2020/01/25"
                }
            ]
        }
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
.article {
  margin-bottom: 1rem;
  border: none;
  border-radius: 0;
  border-top: 1px dotted black;
}

.article:first-child{
  border-top: none;
}

/* 大見出しデザイン */
h2 {
  position: relative;
  padding: 0 0 0.5em 0.7em;
  border-bottom: 1px solid black;
  margin-top: 1rem;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}
h2::after {
  position: absolute;
  top: 0.2em;
  left: 0;
  content: "";
  width: 5px;
  height: 1em;
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

</style>