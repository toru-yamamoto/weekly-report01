<template>
  <div id="app">
      <ul>
          <item v-for="item in items" :item="item"></item>
      </ul>
      <div>
          <input type="text" v-model="inputTitle">
          <button @click="addItem">追加</button>
      </div>
  </div>
</template>
<script>
import Item from './Item.vue';
export default {
    name: 'app',
    components: { Item },
    data () {
        return {
            inputTitle: "",
            items: [
                {is_do: false, title: 'タスク1'},
                {is_do: true, title: 'タスク2'},
                {is_do: false, title: 'タスク3'}
            ]
        }
    },
    methods: {
        addItem() {
            this.items.push({
                title: this.inputTitle,
                is_do: false
            });
        }
    }
}
</script>

<!--
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1></h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://gitter.im/vuejs/vue" target="_blank">Gitter Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
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
  margin-top: 60px;
}

h1, h2 {
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
-->
