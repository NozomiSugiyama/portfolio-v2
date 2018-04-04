<template>
  <parallax-base class="MyMain">
    <parallax-float class="MyAboutWrapper" :offset="0.5">
      <my-about/>
    </parallax-float>
    <my-products class="MyProducts"/>
    <my-activitis class="MyActivitis"/>
    <my-skill class="MySkill"/>
    <footer>
      <div>
        Created by NozomiSugiyama with VueJS
      </div>
      <a href="https://github.com/NozomiSugiyama/portfolio-v2" rel="noopener" target="_blank">
        NozomiSugiyama/portfolio-v2
      </a>
    </footer>
  </parallax-base>
</template>

<script>
import ParallaxBase from '@/components/parallax/ParallaxBase'
import ParallaxFloat from '@/components/parallax/ParallaxFloat'

import MyAbout from '@/components/section/MyAbout'
import MyProducts from '@/components/section/MyProducts'
import MyActivitis from '@/components/section/MyActivitis'
import MySkill from '@/components/section/MySkill'

export default {
  name: 'MyMain',
  components: {
    MyAbout,
    MyProducts,
    MyActivitis,
    MySkill,
    ParallaxBase,
    ParallaxFloat
  }
}
</script>

<style scoped>
.MyMain {
  display: flex;
  flex-direction: column;
  position: relative;
}

.MyMain > .MyActivitis,
.MyMain > .MyProducts,
.MyMain > .MySkill {
  min-height: fit-content;
}

.MyAboutWrapper {
  z-index: 10;
}

.MyMain > :nth-child(2) {
  margin-top: -40vh;
  position: relative;
}

footer {
  align-items: center;
  background-color: #222;
  box-sizing: border-box;
  color: white;
  display: inline-flex;
  font-size: .7rem;
  justify-content: space-around;
  width: 100vw;
  padding: .5rem 2rem;
  min-height: 3rem;
}

footer > a {
  color: white;
  text-decoration: underline;
}
</style>
