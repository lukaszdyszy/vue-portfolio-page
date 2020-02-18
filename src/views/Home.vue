<template>
  <div class="home-container container">
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
            'html', 'css', 'javascript'
          ]
        },
        {
          skillTitle: 'Backend',
          skillList: [
            'php'
          ]
        },
        {
          skillTitle: 'Frameworks',
          skillList: [
            'vue'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>



</style>