<template>
  <div id="app">
    <div>{{msg}}</div>
    <vueCountup :end='2017' :start='100' :options='options'></vueCountup>
  </div>
</template>

<script>
import vueCountup from './index'

export default {
  name: "app",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      options:{
        duration: 3
      }
    };
  },
  mounted() {
  },
  methods:{
  },
  components:{
    vueCountup
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
