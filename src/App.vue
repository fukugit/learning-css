<template>
  <div id="app">

    <div class="contanor">
      <div class="menu">
        <h2>中央揃え</h2>
        <div class="title"><a @click="currentComponent = 'BlockLevelElement'">BlockLevelElement</a></div>
        <div class="title"><a @click="currentComponent = 'InlineElement'">InlineElement</a></div>
      </div>

      <div class="code">
        <keep-alive>
          <component :is="currentComponent"></component>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script>
import BlockLevelElement from './components/centering/BlockLevelElement.vue'
import InlineElement from './components/centering/InlineElement.vue'

export default {
  name: 'App',
  data() {
    return {
      currentComponent: "BlockLevelElement"
    }
  },
  components: {
    BlockLevelElement,
    InlineElement
  }
}
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  max-width: 1600px;
  margin: auto;
  height: 100vh;
}
a {
  cursor: pointer;
}
.contanor {
  display: flex;
  margin-top: 20px;
  background-color: thistle;
}
.menu {
  width: 50%;
  background-color: red;
}
.title {
  width: 100%;
  height: 1.5rem;
  text-align: left;
  background-color: wheat;
  margin-bottom: 10px;
}
.code {
  width: 50%;
  display: flex;
  flex-direction: column; /* 子要素をflexboxにより縦方向に揃える */
  justify-content: center; /* 子要素をflexboxにより中央に配置する */
  align-items: center;  /* 子要素をflexboxにより中央に配置する */
  padding: 30px;
  box-sizing: content-box;
}
</style>
