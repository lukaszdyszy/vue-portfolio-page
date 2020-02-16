<template>
  <div id="app">
    <header>
      <Header />
      <nav>
        <Menu />
      </nav>
    </header>
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Menu from '@/components/Menu';

export default {
  components: {
    Header,
    Menu
  }
}
</script>

<style lang="scss">

* {
  box-sizing: border-box;
}

body{
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
  background-color: whitesmoke;
}

a{
  color: inherit;
  text-decoration: none;
}

h1{
  font-size: 1.75rem;
  letter-spacing: 1px;
  margin: 0;
  padding: 15px 0 10px 0;
}

</style>
