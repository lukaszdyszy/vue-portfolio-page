<template>
    <div class="menu-container">
        <ul class="main-menu">
            <li>
                <router-link to="/">About</router-link>
            </li>
            <li>
                <router-link to="/portfolio">Portfolio</router-link>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Menu'
}
</script>

<style lang="scss" scoped>

ul.main-menu{
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    justify-content: center;
    li{
        line-height: 200%;
        padding: 0 10px;
    }
}

a.router-link-active{
    border-bottom: 2px solid rgb(1, 201, 158);
}

</style>