<template>
  <div class="home-container container">
    <div class="welcome-box">
      {{ $t('welcome') }}
    </div>
    <SkillCard v-for="skill in skills" 
    :skillTitle="$t(skill.skillTitle)" 
    :skillList="skill.skillList" 
    />
  </div>
</template>

<i18n>
{
  "en": {
    "welcome": "I am first year student of Computer Science at Silesian University of Technology. I have been inetersted in programming and web development for a couple of years.",
    "frontend": "Front end",
    "backend": "Back end",
    "frameworks": "Frmeworks",
    "languages": "Languages",
    "polish": "polish - native",
    "english": "english - B2"
  },
  "pl": {
    "welcome": "Jestem studenetem pierwszego roku Informatyki na Politechnice Śląskiej. Od kilku lat interesuję się programowaniem oraz web developmentem.",
    "frontend": "Front end",
    "backend": "Back end",
    "frameworks": "Frameworki",
    "languages": "Języki",
    "polish": "polski - natywnie",
    "english": "angielski - B2"
  }
}
</i18n>

<script>
import SkillCard from '@/components/SkillCard';

export default {
  name: 'Home',
  components: {
    SkillCard
  },
  computed: {
    skills: function(){
      return [
        {
          skillTitle: 'frontend',
          skillList: [
            '<img src="'+require("../assets/skills/html5-64.png")+'" class="skill-icon">html', 
            '<img src="'+require("../assets/skills/css-64.png")+'" class="skill-icon">css', 
            '<img src="'+require("../assets/skills/js-64.png")+'" class="skill-icon">javascript'
          ]
        },
        {
          skillTitle: 'backend',
          skillList: [
            '<img src="'+require("../assets/skills/php-64.png")+'" class="skill-icon">php',
            '<img src="'+require("../assets/skills/mysql-256.png")+'" class="skill-icon">MySql'
          ]
        },
        {
          skillTitle: 'frameworks',
          skillList: [
            '<img src="'+require("../assets/skills/vue.png")+'" class="skill-icon">vue',
            '<img src="'+require("../assets/skills/react.png")+'" class="skill-icon">react'
          ]
        },
        {
          skillTitle: 'languages',
          skillList: [this.$t('polish'), this.$t('english')]
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