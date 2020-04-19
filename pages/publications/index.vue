<i18n>
{
    "ja": {
        "Publications": "研究業績",
        "鬼頭研究室": "鬼頭研究室",
        "修士論文": "修士論文",
        "卒業論文": "卒業論文",
        "学位論文（2018年～）": "学位論文（2018年～）",
        "学術論文・学会発表（2018年〜）": "学術論文・学会発表（2018年〜）",
        "書籍（2015年以降）": "書籍（2015年以降）",
        "招待講演（2015年以降）": "招待講演（2015年以降）"
    },
    "en": {
        "Publications": "Publications",
        "鬼頭研究室": "Kito Laboratory",
        "修士論文": "Master's",
        "卒業論文": "Bachelor's",
        "学位論文（2018年～）": "Theses (2018-)",
        "学術論文・学会発表（2018年〜）": "Conference Presentations (2018-)",
        "書籍（2015年以降）": "Books (2015-)",
        "招待講演（2015年以降）": "Invited Speeches (2015-)"
    }
}
</i18n>
<template>
  <div>
    <!-- タイトル画像 -->
    <b-jumbotron fluid :header="$t('Publications')" header-level="4"></b-jumbotron>
    
    <b-container fluid class="mt-2 pb-3">
      <b-row>

        <!-- 研究業績本文 -->
        <b-col md="9">

          <ul>
            <li><nuxt-link to v-scroll-to="'#thesis'">{{ $t('学位論文（2018年～）') }}</nuxt-link></li>
            <li><nuxt-link to v-scroll-to="'#public'">{{ $t('学術論文・学会発表（2018年〜）') }}</nuxt-link></li>
            <li><nuxt-link to v-scroll-to="'#book'">{{ $t('書籍（2015年以降）') }}</nuxt-link></li>
            <li><nuxt-link to v-scroll-to="'#talk'">{{ $t('招待講演（2015年以降）') }}</nuxt-link></li>
          </ul>
          
          <h2 id="thesis">{{ $t('学位論文（2018年～）') }}</h2>

          <h3>2019年度（卒業論文９件，修士論文３件）</h3>
          <p class="note">※修士論文３件は，筑波大学大学院システム情報工学研究科所属の学生によるものです．</p>
          <table class="table table-borderless">
            <tr><td colspan="2" class="table-title">{{ $t('修士論文') }}</td></tr>
            <tr v-for="(paper, index) in thesis['2019'].master" :key="'2019_master_' + index">
              <td class="publisher">{{ paper.publisher }}</td>
              <td class="paper-title">{{ paper.title }}</td>
            </tr>
            <tr><td colspan="2" class="table-title">{{ $t('卒業論文') }}</td></tr>
            <tr v-for="(paper, index) in thesis['2019'].bachelor" :key="'2019_bachelor_' + index">
              <td class="publisher">{{ paper.publisher }}</td>
              <td class="paper-title">{{ paper.title }}</td>
            </tr>
          </table>

          <h3>2018年度（修士論文２件）</h3>
          <p class="note">※修士論文２件は，筑波大学大学院システム情報工学研究科所属の学生によるものです．</p>
          <table class="table table-borderless">
            <tr><td colspan="2" class="table-title">{{ $t('修士論文') }}</td></tr>
            <tr><td class="publisher">谷中峻輔</td><td class="paper-title">企業依存度に着目した自動車産業ネットワークの構造および経年変化の分析</td></tr>
            <tr><td class="publisher">濱本章弘</td><td class="paper-title">大規模実データを用いた企業間取引ネットワークの複雑ネットワーク解析</td></tr>
          </table>

          <!-- 論文 -->
          <h2 class="mb-3" id="public">{{ $t('学術論文・学会発表（2018年〜）') }}</h2>
          <ul class="mb-5">
            <li v-for="(title, index) in papers" :key="'public_' + index" class="paper">
              {{ title }}
            </li>
          </ul>
          
          <!-- 書籍 -->
          <h2 class="mb-3" id="book">{{ $t('書籍（2015年以降）') }}</h2>
          <ul class="mb-5">
            <li v-for="(title, index) in books" :key="'book_' + index" class="paper">
              {{ title }}
            </li>
          </ul>

          <!-- 講演 -->
          <h2 class="mb-3" id="talk">{{ $t('招待講演（2015年以降）') }}</h2>
          <ul class="mb-5">
            <li v-for="(title, index) in talks" :key="'talk_' + index" class="paper">
              {{ title }}
            </li>
          </ul>

        </b-col>

        <!-- 右カラム -->
        <b-col md="3">
          <CardMenuColumn />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import CardMenuColumn from "@/components/CardMenuColumn.vue";
export default {
  head() {
    return {
      title: `${this.$t('Publications')} | ${this.$t('鬼頭研究室')}`
    }
  },
  components: {
    CardMenuColumn
  },
  computed: {
    thesis: () => ({
      "2019": {
        "master":
          [
            {
              "publisher": "二神克也",
              "title": "インタンジブルアセットに着目した企業間買収予測モデルの構築と検証"
            },{
              "publisher": "古川真由",
              "title": "製品と顧客の多角化に関する戦略間の関係性分析"
            },{
              "publisher": "守谷凪季",
              "title": "企業間抗告ネットワークを用いた競争関係の組成解析"
            }
          ],
        "bachelor":
          [
            {
              "publisher": "池澤太一",
              "title": "企業の概要文館の類似度ネットワーク分析を用いた業界動向に関する研究"
            },{
              "publisher": "上田邦裕",
              "title": "素材情報を用いた自動車部品間の類似性の定量化とサプライヤのポートフォリオ分析"
            },{
              "publisher": "上田真之介",
              "title": "MASを用いた多都市核・周辺モデルにおける集積・分散パターンの創発原理の研究"
            },{
              "publisher": "近江裕志",
              "title": "世界の自動車メーカ間の戦略の違いに着目したサプライベース・ネットワーク分析"
            },{
              "publisher": "後藤大知",
              "title": "地理的要因に着目した米国内の企業間買収ネットワーク分析"
            },{
              "publisher": "竹内悠馬",
              "title": "飲料メーカの商標データを用いた企業戦略に関するネットワーク分析"
            },{
              "publisher": "土井俊彦",
              "title": "技術領域間の繋がりに着目した企業エコシステムの発展に関するネットワーク分析"
            },{
              "publisher": "福重寛隆",
              "title": "経路探索APIを用いた東京近郊交通網の実データ分析とアクセシビリティ検証"
            },{
              "publisher": "馬浩成",
              "title": "営業職の職場内SNSにおける個人の業績評価と会話傾向の関係性に関する研究"
            }
          ]
      }
    }),
    papers: () => [
      "T. Kito, T. Ikezawa, T. Doi, Y. Fukazawa: “Capturing the trend in the IT industry via network analysis of company descriptions,” NetSci 2020 (under review – postponed).",
      "T. Kito, T. Doi, T. Ikezawa, Y. Fukazawa: “Business category network analysis for capturing the value of intangibles,” NetSci 2020 (under review – postponed).",
      "S. Judkowiak, C.S.A. Assuad, T. Kito, K. Martinsen: “Circularity assessment of recycling systems for plastic fish brackets in Norway using Agent-Based simulation,” 18th Global Conference on Sustainable Manufacturing (2020, postponed).",
      "K.A.B. Engh, C.S.A. Assuad, T. Kito, K. Martinsen: “Effects of customer preferences towards sustainable development on producers in recycling systems for aluminum-based products in Norway,” 18th Global Conference on Sustainable Manufacturing (2020, postponed).",
      "M. Furukawa, T. Kito, J. Yamanoi, H. Sayama: “An integrated index for product & customer diversification strategies,” oral presentation at NetSci-X 2020 (2020).",
      "N. Moriya, T. Kito, J. Yamanoi, H. Sayama: “Patent opposition network: Adversarial interactions of companies and trend of innovation,” oral presentation at NetSci-X 2020 (2020).",
      "H. Fukushige, T. Kito: “Road-Railway Detour Index for multimodal transportation networks,” poster at NetSci-X 2020 (2020).",
      "Y. Takeuchi, T. Kito, J. Yamanoi: “Trademark network analysis for investigation of name-branding strategies,” poster at NetSci-X 2020 (2020).",
      "K. Martinsen, C.S.A. Assuad, T. Kito, M. Matsumoto: “Closed loop tolerance engineering modeling and maturity assessment in a circular manufacturing perspective,” Proceedings of EcoDesign 2019 (2019).",
      "T. Kito, S. New, F. Reed-Tsochas: “Disentangling the complexity of supply relationship formations: Firm product diversification and product ubiquity in the Japanese car industry,” International Journal of Production Economics, Vol. 206, pp.159-168 (2018).",
      "T. Kito, P. Holme: “Triadic and quadratic closure as mechanisms for inter-firm transactional network dynamics,” lightening presentation at The International Conference on Complex Networks and Their Applications (2018).",
      "A. Hamamoto, T. Kito: “Effects of industrial and geographical proximities of firms on the Japanese inter-firm network,” lightening presentation at The International Conference on Complex Networks and Their Applications (2018).",
      "濱本章弘，鬼頭朋見：“企業間取引ネットワークの抽象化へ向けて：非均質なコミュニティの組成解析,” ネットワークが創発する知能研究会 (2018).",
      "濱本章弘，鬼頭朋見：“企業間取引ネットワークのコミュニティ分析による産業および地域クラスタの組成解析,” 日本経営工学会経営システム誌，Vol.27, No.4, pp.234-239 (2018).",
      "谷中峻輔，鬼頭朋見：“自動車産業サプライネットワークの構造分析と分類：サプライベースとサプライヤ依存度に注目したアプローチ,” 日本経営工学会経営システム誌，Vol.27, No.4, pp.227-233 (2018).",
    ],
    books: () => [
      "林幸雄，谷澤俊弘，鬼頭朋見，岡本洋（共著）：“Pythonと複雑ネットワーク分析―関係性データからのアプローチ（ネットワーク科学の道具箱II）―”（近代科学社，2019年）",
      "臼井翔平, 鬼頭朋見, 浅谷公威, 坂本陽平, 高野雅典, 伏見卓恭, 池田 圭佑 (翻訳)：“パワー・オブ・ネットワーク：人々をつなぎ社会を動かす６つの原則，”（森北出版，2018年）",
    ],
    talks: () => [
      "鬼頭朋見：“産業ネットワークの複雑さを紐解く：企業の多様性と繋がりの非均質性,” ネットワーク生態学シンポジウム (2017).",
      "鬼頭朋見：“サプライネットワークの非均質性と企業のポートフォリオ戦略,” ネットワーク科学セミナー2017＠統計数理研究所 (2017).",
      "鬼頭朋見：“社会・産業の持続的発展のための領域融合的研究：ビッグデータ＋ネットワーク科学アプローチ,” ＠立命館大学びわこ・くさつキャンパス(2017).",
      "鬼頭朋見：“社会・産業の持続的発展のための領域融合的研究：ビッグデータ＋ネットワーク科学アプローチ,” ＠立命館大学びわこ・くさつキャンパス(2017).",
      "T. Kito: “Detangling complexity of supply network formations: Large-scale data analysis by network science approach”, Faculty of Economics and Business, ＠University of Groningen (2016).",
      "鬼頭朋見: “サプライネットワーク解析とその最新動向,” ERATO河原林巨大グラフプロジェクト @国立情報学研究所 (2016).",
      "鬼頭朋見：”複雑創発系としての社会・経済システム,” @筑波大学人文社会系 歴史・人類学専攻 (2016).",
      "T. Kito, S. New, F. Reed-Tsochas: “Modelling protocols for supply chain mapping”, Discussion Meeting at Hertford College, @University of Oxford, UK (2015).",
    ],
  }
};
</script>
<style scoped>
.jumbotron {
  background-image: url("~assets/paper.jpg");
  background-size: cover;
  background-position: center 60%;
  color: #fff;
}

/* 大見出しデザイン */
h2 {
  position: relative;
  padding: 0 0 0.5em 0.7em;
  border-bottom: 1px solid black;
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
  padding: 0 0.3em 0 1.25em;
  font-size: 1.25rem;
  margin-top: 1em;
}
h3::after {
  position: absolute;
  top: 0.4em;
  left: 0.3em;
  content: "";
  width: 9px;
  height: 9px;
  background-color: #ff5a5f;
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
  z-index: 2;
}
/* 注意書き */
.note {
  padding-left: 1.25em;
  padding-right: 1em;
  font-size: 0.8em;
}
/* 著者 */
.publisher {
  width: 6em;
}

/* 論文リスト */
.paper {
    margin-bottom: .8em;
}
.table {
  width: auto;
  margin-left: 1rem;
  margin-right: 1rem;
}
.table .table-title {
  text-align: center;
  padding-top: 1rem;
  padding-bottom: .5rem;
  font-weight: bold
}
.table th, .table td {
  padding: .25rem;
}
</style>