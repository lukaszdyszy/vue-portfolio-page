<template>
    <div class="project-card-container">
        <header class="header">
            <h2>{{ title }}</h2>
        </header>
        <div class="content">
            <div class="thumbnail">
                <img :src="require('../assets/projects/'+thumbnail)" alt="">
            </div>
            <div class="description">
                <p class="dscr">{{ description }}</p>
                <p class="techs"><span class="subheader">{{ $t('technologies') }}: </span><span v-for="tech in technologies">{{ tech }}, </span></p>
            </div>
            <div class="links">
                <a :href="demoLink" target="blank"><i class="fas fa-desktop fa-2x"></i></a>
                <a :href="githubLink" target="blank"><i class="fas fa-code fa-2x"></i></a>
            </div>
        </div>
    </div>
</template>

<i18n>
{
    "en": {
        "technologies": "Technologies"
    },
    "pl": {
        "technologies": "Technologie"
    }
}
</i18n>

<script>
export default {
    name: 'ProjectCard',
    props: {
        title: String,
        thumbnail: String,
        description: String,
        technologies: Array,
        demoLink: String,
        githubLink: String
    }
}
</script>

<style lang="scss" scoped>

.project-card-container{
    background-color: white;
    margin: 20px 25px;
    box-shadow: 0px 3px 2px 3px rgb(0,0,0);
    font-weight: 300;
    transition: transform 0.45s;
    @media (min-width: 720px){
        &:hover{
            transform: scale(1.05);
        }
    }
}

header.header{
    text-align: center;
    padding: 0;
    box-shadow: 0px 0px 10px -2px rgba(0,0,0,0.75);
}


.content{
    display: flex;
    padding: 20px 0 0 0;
}
.thumbnail, .description, .links{
    padding: 5px;
}
.thumbnail{
    flex: 2;
    img{
        max-width: 100%;
        height: auto;
    }
}
.description{
    flex: 4;
    border-right: 1px solid rgb(220, 220, 220);
    p{
        margin: 0;
        padding: 0;
        line-height: 150%;
        &.dscr{
            padding: 0 0 15px 0;
            border-bottom: 1px solid rgb(220, 220, 220);
        }
    }
}
span.subheader{
    font-weight: 600;
}
.links{
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    a{
        display: block;
        &:hover{
            color: rgb(1, 201, 158);
        }
    }
}


@media (max-width: 720px){
    .content{
        flex-direction: column;
    }
    .description{
        border: none;
    }
    .links{
        flex-direction: row;
        padding: 20px 0 0 0;
    }
}

</style>