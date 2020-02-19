<template>
    <div class="skill-card-container">
        <header class="skill-header">
            <h2>{{ skillTitle }}</h2>
        </header>
        <div class="skill-card-content">
            <div class="skill" v-for="skill in skillList" v-html="skill"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillCard',
    props: {
        skillTitle: String,
        skillList: Array
    }
}
</script>

<style lang="scss">

.skill-card-container{
    margin: 20px;
    padding: 15px;
    text-align: center;
    font-weight: 300;
    border-bottom: 1px solid rgb(212, 212, 212);
    position: relative;
    &::after{
        content: "";
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        box-shadow: inset 0px -7px 10px -10px rgba(138,50,138,1);
        opacity: 0;
        transition: opacity 0.3s;
    }
    &:hover{
        &::after{
            opacity: 1;
        }
    }
}

header.skill-header{
    text-align: center;
}

.skill-card-content{
    display: inline-block;
}
.skill{
    display: flex;
    align-items: center;
    padding: 5px 0;
}
img.skill-icon{
    width: 32px;
    height: 32px;
    margin: 0 10px 0 0;
}

</style>