<template>
  <div id="app">
    <headerComponent></headerComponent>

    <router-view></router-view>
  </div>
</template>

<script>
import headerComponent from './components/header.vue'

export default {
  name: 'app',
  components: {
    headerComponent
  },

  mounted: function() {
    this.$router.push('/index');
    this.initUser();
  }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
