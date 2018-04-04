<template>
  <my-section class="MySkill">
    <my-section-title>Skill</my-section-title>
    <div>
      <div>
        <div>front-end</div>
        <ul>
          <li>ReactJS</li>
          <li>Angular5</li>
          <li>Polymer</li>
          <li>VueJS</li>
        </ul>
      </div>
      <div>
        <div>Programming Language</div>
        <ul>
          <li>JavaScript</li>
          <li>Python</li>
          <li>Java</li>
        </ul>
      </div>
      <div>
        <div>Etc...</div>
        <ul>
          <li>Linux</li>
          <li>Firebase</li>
        </ul>
      </div>
    </div>
  </my-section>
</template>

<script>
import MySection from '@/components/MySection'
import MySectionTitle from '@/components/MySectionTitle'

export default {
  name: 'MySkill',
  components: {
    MySection,
    MySectionTitle
  }
}
</script>

<style scoped>
.MySkill {
  background-color: #243b5d;
  color: white;
}

.MySkill > :nth-child(1) {
  color: white;
}

.MySkill > :nth-child(2) {
  display: flex;
  width: 100%;
  padding: 0px 6rem;
  box-sizing: border-box;
  justify-content: space-between;
}

.MySkill > :nth-child(2) > div {
  display: flex;
  flex-direction: column;
}


.MySkill > :nth-child(2) > div > :nth-child(1) {
  font-size: 1.3rem;
}

ul {
  font-size: 1.2rem;
  padding-left: 1.5rem;
}

li {
  list-style-type: circle;
  letter-spacing: .2rem;
}

@media (max-width: 768px) {
}
</style>
