<template>
    <div class="menu-container" :class="{'sticky': sticky}">
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
    name: 'Menu',
    data(){
        return{
            sticky: false,
            startOffset: 0
        }
    },
    mounted(){
        let self = this;
        this.startOffset = this.$el.offsetTop;
        window.addEventListener('scroll', function(){
            if(window.scrollY > self.startOffset){
                self.sticky = true;
            } else {
                self.sticky = false;
            }
        });
    }
}
</script>

<style lang="scss" scoped>

.menu-container{
    background-color: whitesmoke;
    box-shadow: 0px 3px 8px 2px whitesmoke;
}

ul.main-menu{
    font-weight: 300;
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    justify-content: center;
    font-size: 1.1rem;
    li{
        line-height: 200%;
        padding: 0 10px;
    }
}

a.router-link-exact-active{
    border-bottom: 2px solid rgb(1, 201, 158);
}

.sticky{
    position: fixed;
    z-index: 100;
    width: 100%;
    top: 0;
    left: 0;
    border-top: 2px solid black;
}

</style>