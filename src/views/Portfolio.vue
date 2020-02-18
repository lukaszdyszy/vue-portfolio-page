<template>
    <div class="portfolio-container container">
        <ProjectCard v-for="project in projects" 
        :title="project.title" 
        :thumbnail="project.thumbnail" 
        :description="project.description" 
        :technologies="project.technologies" 
        :demoLink="project.demoLink" 
        :githubLink="project.githubLink" 
        />
    </div>
</template>

<script>
import ProjectCard from '@/components/ProjectCard';

export default {
    name: 'Portfolio',
    components: {
        ProjectCard
    },
    data(){
        return {
            projects: [
                {
                    title: 'Project #1',
                    thumbnail: 'webdev.jpg',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur laudantium ratione eius voluptate.',
                    technologies: ['vue', 'scss'],
                    demoLink: 'http://www.google.com',
                    githubLink: 'http://www.github.com'
                },
                {
                    title: 'Project #2',
                    thumbnail: 'webdev.jpg',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur laudantium ratione eius voluptate.',
                    technologies: ['vue', 'scss'],
                    demoLink: 'http://www.google.com',
                    githubLink: 'http://www.github.com'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>



</style>