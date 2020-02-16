<template>
    <div class="header-container">
        <div class="header-content">
            <h1>John Doe</h1>
            <div class="socials">
                <i class="fab fa-github fa-1.5"></i>
                <i class="fab fa-linkedin-in"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>

.header-container{
    background-image: url('../assets/webdev.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: rgb(218, 218, 218);
    padding: 30px 0;
    border-bottom: 3px solid black;
    text-align: center;
    position: relative;
    &::before{
        content: "";
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        background-color: rgba(0, 0, 0, 0.45);
    }
}

.header-content{
    position: relative;
    z-index: 2;
}

.socials{
    font-size: 1.3rem;
    i{
        padding: 0 10px;
    }
}

</style>