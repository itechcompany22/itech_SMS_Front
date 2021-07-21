<template>
  <Header />
  <Login />
  <Item />
</template>

<script>
import Header from './components/Header.vue'
import Login from './components/Login.vue'
import Item from './components/Item.vue'

export default {
  name: 'App',
  components: {
    Header,
    Login,
    Item
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
html, body, #app {
  width: 100%;
  height: 100%;
  min-width: 1300px
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
}
input:focus {
  outline: none;
}
</style>
