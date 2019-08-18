<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">资讯</router-link> |  
      <router-link to="/about">订阅</router-link> |
      <router-link to="/topic">话题</router-link>
    </div>
    <router-view/>
  </div>
</template>
<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50

#nav
  padding 30px
  a
    text-text-decoration none
    width 33%
    // font-weight bold
    color #2c3e50
    &.router-link-exact-active
      color #42b983
</style>
