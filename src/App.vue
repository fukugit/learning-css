<template>
  <div id="app">

    <div class="contanor">
      <div class="menu">
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
        <div class="category">
          <h2>中央揃え</h2>
          <a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）</a>
          <a @click="currentComponent = 'InlineElement'">インライン（p）</a>
        </div>
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
@import "https://unpkg.com/ress/dist/ress.min.css";

body {
  margin: 0;
}
h1,h2,p {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* color: #2c3e50; */
  max-width: 1600px;
  margin: auto;
  height: 100vh;
}
a {
  cursor: pointer;
  display: block;
  text-decoration : underline;
}
.contanor {
  display: flex;
  margin-top: 20px;
  background-color: thistle;
}
.menu {
  width: 50%;
  background-color: goldenrod;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 10px;
  box-sizing: content-box;
}
.category {
  background-color: thistle;
  word-wrap: break-word;
  width: 200px;
  height: auto;
  border: 1px solid red;
  padding: 10px;
  margin: 10px;
  box-sizing: content-box;
  font-size: 0.7rem;
}
.code {
  width: 50%;
  height: auto;
  /* background-color: indigo; */
  display: flex;
  justify-content: center; /* 子要素をflexboxにより中央に配置する */
  align-items: flex-start;  /* 子要素をflexboxにより中央に配置する */
  padding-top: 50px;
  box-sizing: content-box;
  margin-bottom: 10px;
  overflow: hidden;
}
pre {
  margin: 0;
  padding: 0;
  background-color: sienna;
  width: 400px;
  font-size: 0.7rem;
  overflow: scroll;
}
code {
  font-family: Monaco, Consolas, "Andale Mono", "DejaVu Sans Mono", monospace;
  background-color: rgb(242, 153, 112);
}

</style>
