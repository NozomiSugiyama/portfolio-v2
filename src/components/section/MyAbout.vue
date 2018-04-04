<template>
  <div class="MyAbout">
    <font-cormorant class="MyAboutTextContent">
      <div>Web Engineer</div>
      <div>Nozomi Sugiyama</div>
      <div>from WCDI</div>
    </font-cormorant>
    <div class="MyAboutPageTransition" v-on:click="scrollTo('MyProducts')">
      <div></div>
      <div></div>
    </div>
  </div>
</template>

<script>
import FontCormorant from '@/components/font/FontCormorant'

export default {
  name: 'MyAbout',
  components: {
    FontCormorant
  },
  methods: {
    scrollTo: id => {
      document.getElementById(id).scrollIntoView({
        behavior: 'smooth',
        block   : 'start',
        inline  : 'start'
      })
    }
  }
}
</script>

<style scoped>
  .MyAbout {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    box-shadow: rgba(0, 0, 0, 0.3) 0px 3px 6px 2px;
    background: linear-gradient(-45deg, #EE7752, #E73C7E, #23A6D5, #23D5AB);
    background-size: 400% 400%;
    animation: Gradient 15s ease infinite;
    position: relative;
    padding: 2rem;
    box-sizing: border-box;
  }

  .MyAboutTextContent {
    display: flex;
    flex-direction: column;
    color: white;
  }

  .MyAboutTextContent > :nth-child(1) {
    font-size: 1.5rem;
    letter-spacing: .5rem;
  }

  .MyAboutTextContent > :nth-child(2) {
    font-size: 4rem;
    letter-spacing: 1.5rem;
    margin: .5rem -1.5rem .5rem 0;
  }

  .MyAboutTextContent > :nth-child(3) {
    font-size: 1.1rem;
    letter-spacing: .5rem;
    align-self: flex-end;
  }

  .MyAboutPageTransition {
    background-color: transparent;
    border-radius: 50%;
    cursor: pointer;
    height: 5rem;
    margin: 2rem;
    width: 5rem;
    position: absolute;
    bottom: 1rem;
    left: calc(50vw - 5rem);
  }

  .MyAboutPageTransition > * {
    border-radius: 3px;
    border-left: 2px solid #eee;
    border-bottom: 2px solid #eee;
    top: 0;
    height: 2rem;
    transform: rotate(-45deg);
    transition: all .2s ease;
    width: 2rem;
    margin: 1.5rem;
    position: absolute;
  }

  .MyAboutPageTransition > :nth-child(2) {
    top: .8rem;
  }

  .MyAboutPageTransition:hover > :nth-child(1) {
    top: .8rem;
  }

  .MyAboutPageTransition:hover > :nth-child(2) {
    top: 0;
  }

  @keyframes Gradient {
    0% {
      background-position: 0% 50%
    }
    50% {
      background-position: 100% 50%
    }
    100% {
      background-position: 0% 50%
    }
  }


@media (max-width: 768px) {
  .MyAboutPageTransition {
    margin-bottom: 6rem;
  }
}
</style>