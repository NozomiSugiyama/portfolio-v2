<template>
  <my-section class="MyActivitis">
    <my-section-title>Activities</my-section-title>
    <div class="MyActivitis_MainContent">
      <div class="MyActivitis_TimeLine"></div>
      <div>
        <div
          :offset="0.4"
          v-for="(contest, index) in contests"
          class="MyActivitis_ContestList"
          :key="index"
        >
          <div class="MyActivitis_Year">{{ contest.year }}</div>
          <parallax-float
            v-for="(item, itemIndex) in contest.items"
            :offset="innerWidth > 768 ? 0.2 : 0"
            :key="itemIndex"
          >
            <parallax-inview>
              <animation-fade-in-up>
                <div class="MyActivitis_Item">
                  <div class="MyActivitis_ItemInfo">
                    <span>{{
                      item.date ? (item.date.getMonth() + 1) + '/' + (item.date.getDate()) 
                    :             "未定"
                    }}</span>
                    <font-mplus>{{ item.name }}<span> {{ item.result }}</span></font-mplus>
                  </div>
                  <my-image :src="item.image" v-if="item.image" :cover="true"></my-image>
                </div>
              </animation-fade-in-up>
            </parallax-inview>
          </parallax-float>
        </div>
      </div>
    </div>
  </my-section>
</template>

<script>
import MyImage from '@/components/MyImage'
import MySection from '@/components/MySection'
import MySectionTitle from '@/components/MySectionTitle'

import AnimationFadeInUp from '@/components/effect/animation/AnimationFadeInUp'
import FontMplus from '@/components/font/FontMplus'
import ParallaxFloat from '@/components/parallax/ParallaxFloat'
import ParallaxInview from '@/components/parallax/ParallaxInview'

import ICTSC5Image from '@/assets/img/contests/ICTSC5.jpg'
import SECCON2016Image from '@/assets/img/contests/SECCON-2016.jpg'
import SPAJAM2016Image from '@/assets/img/contests/SPAJAM-2016.jpg'
import ICTSC6Image from '@/assets/img/contests/ICTSC6.jpg'
import SPAJAM2017Image from '@/assets/img/contests/SPAJAM-2017.jpg'
import MBSD2017Image from '@/assets/img/contests/MBSD-2017.jpg'
import ICTSC9Image from '@/assets/img/contests/ICTSC9.jpg'
import ETRoboCon2015 from '@/assets/img/contests/ETRoboCon-2015.jpg'

export default {
  name: 'MyActivitis',
  components: {
    MyImage,
    MySection,
    MySectionTitle,
    FontMplus,
    ParallaxInview,
    ParallaxFloat,
    AnimationFadeInUp
  },
  data: () => ({
    innerWidth: window.innerWidth,
    contests: [
      {
        year: 2015,
        items: [ 
          {
            date: new Date(2015, 8),
            name: 'ETロボコン2015',
            result: '東京予選出場',
            image: ETRoboCon2015
          },
          {
            date: new Date(2015, 11),
            name: 'SECCON 2015 online',
            result: '予選出場'
          },
        ]
      },
      {
        year: 2016,
        items: [ 
          {
            date: new Date(2016, 1),
            name: 'ICTSC 5',
            result: '出場',
            image: ICTSC5Image
          },
          {
            date: new Date(2016, 4),
            name: 'SPAJAM 2016',
            result: '予選出場',
            image: SPAJAM2016Image
          },
          {
            date: new Date(2016, 7),
            name: 'ICTSC 6',
            result: '優秀賞',
            image: ICTSC6Image
          },
          {
            date: new Date(2016, 8),
            name: 'ISUCON 6',
            result: '予選出場'
          },
          {
            date: new Date(2016, 11),
            name: 'SECCON 2016 online',
            result: '予選出場',
            image: SECCON2016Image
          },
        ]
      },
      {
        year: 2017,
        items: [ 
          {
            date: new Date(2017, 5),
            name: 'SPAJAM2017',
            result: '予選出場',
            image: SPAJAM2017Image
          },
          {
            date: new Date(2017, 9),
            name: 'ISUCON7 online',
            result: '予選出場'
          },
          {
            date: new Date(2017, 11),
            name: 'SECCON2017',
            result: '予選出場'
          },
          {
            date: new Date(2017, 11),
            name: 'MBSD Cybersecurity Challenges 2017',
            result: '第５位',
            image: MBSD2017Image
          },
        ]
      },
      {
        year: 2018,
        items: [ 
          {
            date: new Date(2018, 2),
            name: 'ICTSC9',
            result: '出場',
            image: ICTSC9Image
          },
          {
            date: new Date(2018, 3),
            name: 'SPAJAM道場',
            result: '出場決定'
          },
          {
            date: new Date(2018, 5),
            name: 'SPAJAM2018',
            result: '出場予定'
          },
          {
            date: new Date(2018, 5),
            name: 'ICTSC2018',
            result: '運営出場決定'
          }
        ]
      },
    ]
  })
}
</script>

<style scoped>
.MyActivitis {
  background-color: #eaeaea;
}

.MyActivitis > :nth-child(2) {
  position: relative;
  padding: 0 6rem;
  padding-left: 15rem;
}

.MyActivitis_Year {
  position: relative;
  width: max-content;
  font-size: 2rem;
  letter-spacing: .5rem;
  border-bottom: 1px solid #333;
  margin-top: 1rem;
  margin-bottom: 1.3rem;
  margin-left: -11rem;
}

.MyActivitis_TimeLine {
  min-width: 12px;
  max-width: 12px;
  background: linear-gradient(-45deg, #EE7752, #E73C7E, #23A6D5, #23D5AB);
  border-radius: 6px;
  left: 1rem;
  top: 0;
}

.MyActivitis_MainContent {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  width: 100%;
  justify-content: center; 
}

.MyActivitis_MainContent > * {
  display: flex;
  flex-direction: column;
}

.MyActivitis_MainContent > :nth-child(2) {
  padding-left: 1rem;
}

.MyActivitis_Item {
  display: flex;
  align-items: flex-end;
  flex-direction: row;
  justify-content: space-between;
  position: relative;
  box-sizing: border-box;
  border-bottom: 1px solid #888;
}

.MyActivitis_Item::before {
  content: "";
  position: absolute;
  bottom: 0;
  width: 10rem;
  background-color: black;
  border-radius: 50%;
  z-index: 1;
}

.MyActivitis_Item > :nth-child(1) {
  height: fit-content;
  padding: 1rem 2rem;
}

.MyActivitis_Item > :nth-child(2) {
  min-width: 20rem;
  max-width: 20rem;
  max-height: 12rem;
}

.MyActivitis_ItemInfo {
  display: flex;
  flex-direction: column;
}

.MyActivitis_ItemInfo > :nth-child(1) {
  font-size: 1.7rem;
  letter-spacing: .2rem;
  margin-right: -.2rem;
  margin-bottom: .5rem;
}

.MyActivitis_ItemInfo > :nth-child(2) {
  font-size: 1.5rem;
  margin-right: -0.3rem;
  letter-spacing: .3rem;
}

@media (max-width: 768px) {
  .MyActivitis_MainContent {
    padding: 0 !important;
  }

  .MyActivitis_TimeLine {
    display: none;
  }

  .MyActivitis_Year {
    position: static;
    margin-left: initial;
  }
  
  .MyActivitis_MainContent > :nth-child(2) {
    padding-left: 0;
    width: 100%;
  }

  .MyActivitis_Item::before {
    content: none;
  }

  .MyActivitis_Item::after {
    content: none;
  }

  .MyActivitis_Item > :nth-child(2) {
    min-width: 10rem;
    max-width: 10rem;
    max-height: 10rem;
  }

  .MyActivitis_ItemInfo > :nth-child(1) {
    font-size: 1.2rem;
  }

  .MyActivitis_ItemInfo > :nth-child(2) {
    font-size: 1.2rem;
  }
}
</style>
