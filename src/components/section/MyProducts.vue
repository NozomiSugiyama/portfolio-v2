<template>
  <my-section class="MyProducts" id="MyProducts">
    <my-section-title>Products</my-section-title>
    <div class="MyProducts_MainContent">
      <div class="MyProducts_Item">
        <div class="MyProducts_ItemTop">
          <parallax-float :offset="0.1">
            <parallax-inview class="MyProducts_ItemOverview">
              <animation-fade-in>
                <span>Familiar Chat</span>
                <a
                  href="https://github.com/familiar-chat/"
                  rel="noopener"
                  target="_blank"
                >
                  <icon-link/>
                </a>
              </animation-fade-in>
              <span>
                ホームページ上での運営者と来訪者とのリアルタイムチャットサポートシステム
              </span>
            </parallax-inview>
          </parallax-float>
          <my-image :src="FamiliarChatImage" class="MyProducts_ItemMainImage"/>
        </div>
        <div>
          <div class="MyProducts_ItemFeatures">
            <parallax-float :offset="innerWidth > 768 ? 0.3 : 0.1">
              <parallax-inview>
                <animation-widen>
                  <my-image-slider>
                    <my-image :src="FamiliarChatEditOperartorImage"/>
                    <my-image :src="FamiliarChatLoginImage"/>
                    <my-image :src="FamiliarChatOperartorChatingImage"/>
                    <my-image :src="FamiliarChatTriggerImage"/>
                  </my-image-slider>
                </animation-widen>
              </parallax-inview>
            </parallax-float>
            <div class="MyProducts_ItemFeaturesInfo">
              <div>Features</div>
              <div>
                <div>
                  <div>For operator</div>
                  <ul>
                    <li>チャット機能</li>
                    <li>画像送信機能</li>
                    <li>定型文</li>
                    <li>自動応答</li>
                    <li>訪問者情報</li>
                    <li>営業時間</li>
                    <li>履歴管理</li>
                  </ul>
                </div>
                <div>
                  <div>For visitor</div>
                  <ul>
                    <li>チャット機能</li>
                    <li>画像送信機能</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
          <!-- <my-button component="a" href="https://github.com/familiar-chat/" rel="noopener" target="_blank" class="MyProducts_ItemSourceButton">Source</my-button> -->
        </div>
        <parallax-float :offset="0.1" class="MyProducts_ItemPointList">
          <parallax-inview>
            <animation-widen-shadow>
              <div class="MyProducts_ItemPointItem">
                <div>
                  <my-image :src="FamiliarChatGoogleMaterialDesignLogoImage"></my-image>
                  <span>Material Designの実装</span>
                </div>
                <div>
                  ReactJSにてMaterial Designの各種UIコンポーネントの作成。
                </div>
                <!-- <my-button component="a" href="https://github.com/familiar-chat/react-material" rel="noopener" target="_blank" class="MyProducts_ItemSourceButton">Source</my-button> -->
              </div>
            </animation-widen-shadow>
          </parallax-inview>
          <parallax-inview>
            <animation-widen-shadow>
              <div class="MyProducts_ItemPointItem">
                <div>
                  <my-image :src="FamiliarChatHumanIconImage"></my-image>
                  <span>設計/開発/運用を一人で担当</span>
                </div>
                <div>
                  Productの外部設計、内部設計からそれらの実装、運用までを一人で行う。
                </div>
              </div>
            </animation-widen-shadow>
          </parallax-inview>
        </parallax-float>
      </div>
      <div class="MyProducts_Item">
        <div class="MyProducts_ItemTop">
          <parallax-float :offset="0.1">
            <parallax-inview class="MyProducts_ItemOverview">
              <animation-fade-in>
                <span>IS09 ECSite</span>
                <a
                  href="https://github.com/is09-ecsite/"
                  rel="noopener"
                  target="_blank"
                >
                  <icon-link/>
                </a>
                </animation-fade-in>
              <span>
                カレッジ内の生徒が利用する仮想ECサイト。
                フロントエンドはSPA 、バックエンドはRESTful APIとして実装。
              </span>
            </parallax-inview>
          </parallax-float>
          <my-image :src="IS09ECSiteImage" class="MyProducts_ItemMainImage"></my-image>
        </div>
        <div>
          <div class="MyProducts_ItemFeatures">
            <parallax-float :offset="innerWidth > 768 ? 0.3 : 0.1">
              <parallax-inview>
                <animation-widen>
                  <my-image-slider>
                    <my-image :src="IS09ECSiteCartImage"/>
                    <my-image :src="IS09ECSiteProductListImage"/>
                  </my-image-slider>
                </animation-widen>
              </parallax-inview>
            </parallax-float>
            <div class="MyProducts_ItemFeaturesInfo">
              <div>Features</div>
              <div>
                <div>
                  <div>User account</div>
                  <ul>
                    <li>ログイン認証</li>
                    <li>購入履歴</li>
                  </ul>
                </div>
                <div>
                  <div>Product</div>
                  <ul>
                    <li>閲覧</li>
                    <li>カート追加</li>
                    <li>購入</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
          <!-- <my-button component="a" href="https://github.com/is09-ecsite" rel="noopener" target="_blank" class="MyProducts_ItemSourceButton">Source</my-button> -->
        </div>
        <parallax-float :offset="0.1" class="MyProducts_ItemPointList">
          <parallax-inview>
            <animation-widen-shadow>
              <div class="MyProducts_ItemPointItem">
                <div>
                  <my-image :src="IS09ECSiteTeamIconImage"></my-image>
                  <span>Projectのリーダーを担当</span>
                </div>
                <div>
                  ソフトウェア設計、進捗管理、担当者割り当て、技術教育を務める。
                </div>
                <!-- <my-button component="a" href="https://github.com/familiar-chat/react-material" rel="noopener" target="_blank" class="MyProducts_ItemSourceButton">Source</my-button> -->
              </div>
            </animation-widen-shadow>
          </parallax-inview>
          <parallax-inview>
            <animation-widen-shadow>
              <div class="MyProducts_ItemPointItem">
                <div>
                  <my-image :src="FamiliarChatHumanIconImage"></my-image>
                  <span>システムの設計/開発を担当</span>
                </div>
                <div>
                  機能要件を定義、それに合わせた設計とフロントエンドの実装を行う。
                </div>
              </div>
            </animation-widen-shadow>
          </parallax-inview>
        </parallax-float>
      </div>
    </div>
  </my-section>
</template>
<script>

import MyButton from '@/components/MyButton'
import MyImage from '@/components/MyImage'
import MyImageSlider from '@/components/MyImageSlider'
import MySection from '@/components/MySection'
import MySectionTitle from '@/components/MySectionTitle'
import MySkillItem from '@/components/MySkillItem'

import EffectShadow from '@/components/effect/EffectShadow'
import EffectShadowText from '@/components/effect/EffectShadowText'
import AnimationFadeIn from '@/components/effect/animation/AnimationFadeIn'
import AnimationWiden from '@/components/effect/animation/AnimationWiden'
import AnimationWidenShadow from '@/components/effect/animation/AnimationWidenShadow'

import ParallaxFloat from '@/components/parallax/ParallaxFloat'
import ParallaxInview from '@/components/parallax/ParallaxInview'

import IconLink from '@/components/icon/IconLink'

import FamiliarChatEditOperartorImage from '@/assets/img/products/familiar-chat/edit_operator.png'
import FamiliarChatImage from '@/assets/img/products/familiar-chat/familiar-chat.png'
import FamiliarChatLoginImage from '@/assets/img/products/familiar-chat/login.png'
import FamiliarChatOperartorChatingImage from '@/assets/img/products/familiar-chat/operator_chatting.png'
import FamiliarChatTriggerImage from '@/assets/img/products/familiar-chat/trigger.png'
import FamiliarChatGoogleMaterialDesignLogoImage from '@/assets/img/products/familiar-chat/google_material_design_logo.png'
import FamiliarChatHumanIconImage from '@/assets/img/products/familiar-chat/human_icon.png'

import IS09ECSiteImage from '@/assets/img/products/is09-ecsite/is09-ecsite.png'
import IS09ECSiteTeamIconImage from '@/assets/img/products/is09-ecsite/team_icon.png'
import IS09ECSiteCartImage from '@/assets/img/products/is09-ecsite/cart.png'
import IS09ECSiteProductListImage from '@/assets/img/products/is09-ecsite/product_list.png'

import ReactImage from '@/assets/img/technology/react.png'
import Angularmage from '@/assets/img/technology/angular.png'
import FirebaseImage from '@/assets/img/technology/firebase.png'

export default {
  name: 'MyProducts',
  components: {
    MyButton,
    MyImage,
    MyImageSlider,
    MySection,
    MySectionTitle,
    MySkillItem,
    ParallaxFloat,
    ParallaxInview,
    IconLink,
    EffectShadow,
    EffectShadowText,
    AnimationFadeIn,
    AnimationWiden,
    AnimationWidenShadow
  },
  data: () => ({
    FamiliarChatEditOperartorImage,
    FamiliarChatImage,
    FamiliarChatLoginImage,
    FamiliarChatOperartorChatingImage,
    FamiliarChatTriggerImage,
    FamiliarChatGoogleMaterialDesignLogoImage,
    FamiliarChatHumanIconImage,
    IS09ECSiteImage,
    IS09ECSiteTeamIconImage,
    IS09ECSiteCartImage,
    IS09ECSiteProductListImage,
    ReactImage,
    Angularmage,
    FirebaseImage,
    innerWidth: window.innerWidth
  })
}
</script>

<style scoped>
.MyProducts {
}

ul {
  padding-left: 1.5rem;
}

.MyProducts_MainContent {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.MyProducts_Item:not(:last-child) {
  margin-bottom: 12rem;
}

.MyProducts_ItemTop {
  position: relative;
  display: flex;
  justify-content: flex-end;
  margin-bottom: 8rem;
}

.MyProducts_ItemTop > :first-child {
  position: absolute;
  bottom: 2rem;
}

.MyProducts_ItemOverview {
  width: 50vw;
  background-color: rgba(0, 0, 0, .5);
  color: white;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  z-index: 1;
}

.MyProducts_ItemOverview > :first-child {
  font-size: 3rem;
  letter-spacing: .5rem;
}

.MyProducts_ItemOverview > :nth-child(2) {
  font-size: 1rem;
  margin-top: 1rem;
  letter-spacing: .3rem;
  text-indent: 1.3rem;
}

.MyProducts_ItemTop > :nth-child(2) {
  width: 65vw;
}

.MyProducts_ItemFeatures {
  position: relative;
  height: 25rem;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  padding: 0 3vw 5rem 3vw;
  box-sizing: border-box;
}

.MyProducts_ItemFeatures > :nth-child(1) {
  display: flex;
  box-sizing: border-box;
  position: absolute;
  height: min-content;
  padding: 0 3vw;
}

.MyProducts_ItemFeatures > :nth-child(1) > * {
  width: 45vw;
}

.MyProducts_ItemFeatures > :nth-child(2) {
  position: relative;
  width: 40vw;
}

.MyProducts_ItemFeaturesInfo {
  white-space: nowrap;
}

.MyProducts_ItemFeaturesInfo > :nth-child(1) {
  text-align: center;
  margin: 1rem 0;
  letter-spacing: .4rem;
  font-size: 2rem;
}

.MyProducts_ItemFeaturesInfo > :nth-child(2) {
  display: flex;
  justify-content: space-around;
}

.MyProducts_ItemFeaturesInfo > :nth-child(2) > * > :nth-child(1) {
  font-size: 1.3rem;
  margin-bottom: .5rem;
  letter-spacing: .2rem;
}

.MyProducts_ItemFeaturesInfo > :nth-child(2) > * > :nth-child(2) {
  list-style-type: circle;
  letter-spacing: .2rem;
}

.MyProducts_ItemPointList {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-wrap: wrap;
  width: 100%;
}

.MyProducts_ItemPointList > * {
  margin: 1rem;
}

.MyProducts_ItemPointItem {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  width: 25rem;
}

.MyProducts_ItemPointItem> *:not(:last-child) {
  margin-bottom: 1rem;
}

.MyProducts_ItemPointItem > :nth-child(1) {
  display: flex;
  align-items: center;
}

.MyProducts_ItemPointItem > :nth-child(1) > :nth-child(1) {
  width: 4rem;
  height: 4rem;
}

.MyProducts_ItemPointItem > :nth-child(1) > :nth-child(2) {
  font-size: 1.3rem;
  letter-spacing: .2rem;
  margin-left: 1rem;
}

.MyProducts_ItemPointItem > :nth-child(2) {
  letter-spacing: .2rem;
  text-indent: 1.2rem;
}

@media (max-width: 768px) {
  .MyProducts_ItemOverview {
    width: 100%;
    box-sizing: border-box;
    bottom: -8rem;
    position: relative;
  }

  .MyProducts_ItemFeatures {
    flex-direction: column;
    height: initial;
    padding-top: 60vw;
  }

  .MyProducts_ItemPointItem {
    width: 100%;
  }

  .MyProducts_ItemFeatures > :nth-child(1) {
    top: 0;
  }

  .MyProducts_ItemFeatures > :nth-child(1) > * {
    width: 100%;
  }

  .MyProducts_ItemFeaturesInfo {
    width: 100% !important;
  }
  
  .MyProducts_ItemTop > :nth-child(2) {
    width: 100%;
  }

}
</style>
