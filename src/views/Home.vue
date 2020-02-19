<template>
  <div class="home-container container">
    <div class="welcome-box">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum minus provident fugit velit cupiditate sint! Sed quisquam eaque eum molestias odit eligendi quae dolorum sequi quos ab quia aperiam minus, cupiditate cumque rem modi alias ad. Sit dolores consequuntur numquam, veritatis expedita aspernatur, soluta, ipsa quos iure sequi atque blanditiis alias voluptas laboriosam tempore voluptate.
    </div>
    <SkillCard v-for="skill in skills" 
    :skillTitle="skill.skillTitle" 
    :skillList="skill.skillList" 
    />
  </div>
</template>

<script>
import SkillCard from '@/components/SkillCard';

export default {
  name: 'Home',
  components: {
    SkillCard
  },
  data(){
    return {
      skills: [
        {
          skillTitle: 'Frontend',
          skillList: [
            '<img src="'+require("../assets/skills/html5-64.png")+'" class="skill-icon">html', 
            '<img src="'+require("../assets/skills/css-64.png")+'" class="skill-icon">css', 
            '<img src="'+require("../assets/skills/js-64.png")+'" class="skill-icon">javascript'
          ]
        },
        {
          skillTitle: 'Backend',
          skillList: [
            '<img src="'+require("../assets/skills/php-64.png")+'" class="skill-icon">php'
          ]
        },
        {
          skillTitle: 'Frameworks',
          skillList: [
            '<img src="'+require("../assets/skills/vue.png")+'" class="skill-icon">vue'
          ]
        },
        {
          skillTitle: 'Lnaguages',
          skillList: [
            'polish - native',
            'english - B2',
            'spanish - basic'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.welcome-box{
  padding: 15px;
  box-shadow: 10px 8px 2px 0px rgba(0,0,0,0.85);
  border: 2px solid rgb(212, 212, 212);
  margin: 5px;
}

</style>