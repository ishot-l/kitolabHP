<i18n>
{
    "ja": {
        "メンバー": "メンバー",
        "鬼頭 朋見": "鬼頭 朋見",
        "所属（准教授）": "所属（准教授）",
        "早稲田大学": "早稲田大学",
        "mgmt": "創造理工学部 経営システム工学科",
        "bdm": "大学院 創造理工学研究科 経営デザイン専攻",
        "その他の所属": "その他の所属",
        "winlab": "早稲田イノベーション研究所",
        "mathphys": "早稲田大学 数物系科学拠点",
        "学生": "学生",
        "修士課程": "修士課程",
        "学部生": "学部生"
    },
    "en": {
        "メンバー": "People",
        "鬼頭 朋見": "Tomomi Kito",
        "所属（准教授）": "Associate professor",
        "早稲田大学": "Waseda University",
        "mgmt": "Department of Industrial and Management System Engineering, School of Creative Science and Engineering",
        "bdm": "Department of Business Design and Management",
        "その他の所属": "Member of",
        "winlab": "Waseda Innovation Laboratory",
        "mathphys": "Waseda University Mathematics and Physics Unit",
        "学生": "Students",
        "修士課程": "Master's",
        "学部生": "Bachelor's",
        "池澤 太一": "Taichi Ikezawa",
        "上田 邦裕": "Kunihiro Ueda",
        "上田 真之介": "Shinnosuke Ueta",
        "近江 裕志": "Yuji Ohmi",
        "竹内 悠馬": "Yuma Takeuchi",
        "土井 俊彦": "Toshihiko Doi",
        "福重 寛隆": "Hirotaka Fukushige",
        "櫛野 智史": "Satoshi Kushino"
    }
}
</i18n>
<template>
  <div>
    <!-- タイトル画像 -->
    <b-jumbotron fluid :header="$t('メンバー')" header-level="4"></b-jumbotron>

    <!-- その下 -->
    <b-container fluid class="mt-2 pb-3">
      <b-row>
        <!-- メイン -->
        <b-col md="9" class="mb-2">
          <b-container fluid>
            <!-- Boss -->
            <h2>{{ $t('鬼頭 朋見') }}</h2>
            <b-row>
              <b-col md="4" order-md="2">
                <b-img center fluid src="~assets/boss.jpg" alt="Kito Tomomi" class="mt-2"></b-img>
              </b-col>
              <b-col md="8" order-md="1">
                <h3>{{ $t('所属（准教授）') }}</h3>
                <p class="pl-4 mb-0">{{ $t('早稲田大学') }}</p>
                <ul>
                  <li><a href="http://www.mgmt.waseda.ac.jp/" target="_brank">{{ $t('mgmt') }}</a></li>
                  <li><a href="http://www.bdm.waseda.ac.jp/" target="_brank">{{ $t('bdm') }}</a></li>
                </ul>

                <h3>{{ $t('その他の所属') }}</h3>
                <ul>
                  <li><a href="https://www.winlab.tokyo" target="_brank">{{ $t('winlab') }}</a></li>
                  <li><a href="http://www.sgu-mathphys.sci.waseda.ac.jp" target="_brank">{{ $t('mathphys') }}</a></li>
                  <li><a href="https://research.wpcarey.asu.edu/supply-networks/" target="_brank">Complex Adaptive Supply Networks</a></li>
                  <li><a href="https://www.cabdyn.ox.ac.uk/complexity_home.asp" target="_brank">Cabdyn Complexity Centre</a></li>
                </ul>
              </b-col>
            </b-row>

            <!-- Students -->
            <h2>{{ $t('学生') }}</h2>
            <b-row>
              <b-col md="6">
                <h3>{{ $t('修士課程') }}</h3>
                <ul>
                  <li>{{ $t("池澤 太一")}}</li>
                  <li>{{ $t("上田 邦裕") }}</li>
                  <li>{{ $t("上田 真之介") }}</li>
                  <li>{{ $t("近江 裕志") }}</li>
                  <li>{{ $t("竹内 悠馬") }}</li>
                  <li>{{ $t("土井 俊彦") }}</li>
                  <li>{{ $t("福重 寛隆") }}</li>
                </ul>
              </b-col>
              <b-col md="6">
                <h3>{{ $t('学部生') }}</h3>
                <ul>
                  <li>{{ $t("櫛野 智史") }}</li>
                </ul>
              </b-col>
            </b-row>
          </b-container>
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
  components: {
    CardMenuColumn
  }
};
</script>
<style scoped>
.jumbotron {
  background-image: url("~assets/people.jpg");
  background-size: cover;
  background-position: center 60%;
  color: #fff;
}

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