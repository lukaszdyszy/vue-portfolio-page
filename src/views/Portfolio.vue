<template>
    <div class="portfolio-container container">
        <ProjectCard v-for="project in projects" 
        :title="$t('projects.'+project.title+'.title')" 
        :thumbnail="project.thumbnail" 
        :description="$t('projects.'+project.title+'.description')" 
        :technologies="project.technologies" 
        :demoLink="project.demoLink" 
        :githubLink="project.githubLink" 
        />
    </div>
</template>

<i18n>
{
    "en": {
        "projects": {
            "rc-timer": {
                "title": "rc-timer",
                "description": "Rubik's Cube timer. Made with react.js. Contains scramble algorithm for five types of cubes and exporting times features."
            },
            "task-calendar": {
                "title": "task calendar",
                "description": "To-do application. Tasks are stored in MySql database, back end written in php, front end in vue."
            },
            "currency-calculator": {
                "title": "currency calculator",
                "description": "A currency calculator using API from NBP (Polish Ntional Bank)."
            },
            "piffko-kunst": {
                "title": "piffko-kunst.de",
                "description": "Website made for painter using Wordpress as CMS."
            }
        }
    },
    "pl": {
        "projects": {
            "rc-timer": {
                "title": "rc-timer",
                "description": "Timer do Kostki Rubika. Wykonany z użyciem biblioteki React.js. Posiada algorytm mieszający dla pięciu typów kostek oraz opcję eksportu czasów."
            },
            "task-calendar": {
                "title": "kalendarz zadań",
                "description": "Aplikacja listy zadań. Wykorzystuje bazę danych MySql, back end w php, front end we vue."
            },
            "currency-calculator": {
                "title": "kalkulator walut",
                "description": "Kalkulator walut. Używa API udostępnianego przez NBP."
            },
            "piffko-kunst": {
                "title": "piffko-kunst.de",
                "description": "Stron internetowa dla malarza, wykorzustuje CMS Wordpress."
            }
        }
    }
}
</i18n>

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
                    title: "rc-timer",
                    thumbnail: "rctimer.png",
                    technologies: ["react"],
                    demoLink: "https://lukaszdyszy.github.io/rc-timer/",
                    githubLink: "https://github.com/lukaszdyszy/rc-timer"
                },
                {
                    title: "task-calendar",
                    thumbnail: "taskcalendar.png",
                    technologies: ["MySql", "REST Api", "php", "vue"],
                    demoLink: "http://task-calendar.000webhostapp.com/",
                    githubLink: "https://github.com/lukaszdyszy/task-calendar-backend"
                },
                {
                    title: "currency-calculator",
                    thumbnail: "currencycalculator.png",
                    technologies: ["vue", "Api"],
                    demoLink: "https://lukaszdyszy.github.io/currency-calculator/#/",
                    githubLink: "https://github.com/lukaszdyszy/currency-calculator"
                },
                {
                    title: "piffko-kunst",
                    thumbnail: "piffkokunst.png",
                    technologies: ["Wordpress"],
                    demoLink: "http://piffko-kunst.de/",
                    githubLink: ""
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>



</style>