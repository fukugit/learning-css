<template>
  <div id="app">

    <div class="contanor">
      <div class="menu">
        <div class="category">
          <h2>中央揃え</h2>
          <ol class="category-list">
            <li><a @click="currentComponent = 'BlockLevelElement'">ブロックレベル（div）その1</a></li>
            <li><a @click="currentComponent = 'InlineElement'">インライン（p）</a></li>
          </ol>
        </div>
        <div class="category">
          <h2>aタグ</h2>
          <ol class="category-list">
            <li><a @click="currentComponent = 'DivLink'">div全体をリンク化</a></li>
          </ol>
        </div>
        <div class="category">
          <h2>margin</h2>
          <ol class="category-list">
            <li><a @click="currentComponent = 'Bottom'">最下部に表示</a></li>
          </ol>
        </div>
      </div>


      <div class="code">
        <div class="component">
          <div class="main-header">
            <h2>{{title}}</h2>
          </div>
          <div class="main-explanation">
            {{explanation}}
            </div>
          <div class="component-detail">
            <keep-alive>
              <component :is="currentComponent" v-on:title="incrementNum"></component>
            </keep-alive>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import BlockLevelElement from './components/centering/BlockLevelElement.vue'
import InlineElement from './components/centering/InlineElement.vue'
import DivLink from './components/link/DivLink.vue'
import Bottom from './components/margin/Bottom.vue'

export default {
  name: 'App',
  data() {
    return {
      currentComponent: "BlockLevelElement",
      title: 'タイトルがありません',
      explanation: '説明がありません'
    }
  },
  components: {
    BlockLevelElement,
    InlineElement,
    DivLink,
    Bottom
  },
  methods: {
    /* ここのvalueは $eventの値が入ります。*/
    incrementNum(...value) {
      const [title, explanation] = value;
      this.title = title;
      this.explanation = explanation;
    }
  }
}
</script>

<style>
@import "https://unpkg.com/ress/dist/ress.min.css";

body {
  margin: 0;
  background-color: #222831;
  color: whitesmoke;
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
}
.menu {
  width: 50%;
  display: flex;
  padding: 10px;
  box-sizing: content-box;
  border: #393E46 solid 1px;
}
.category {
  background-color: #393E46;
  word-wrap: break-word;
  width: 200px;
  height: auto;
  max-height: 300px;
  padding: 10px;
  margin: 10px;
  box-sizing: content-box;
  font-size: 0.7rem;
}
.category-list {
  margin-left: 20px;
}
.code {
  width: 50%;
  height: auto;
  display: flex;
  justify-content: center; /* 子要素をflexboxにより中央に配置する */
  flex-direction: column;
  flex-wrap: wrap;
  align-items: center;
  box-sizing: content-box;
  margin-bottom: 10px;
  overflow: hidden;
}

.component {
  width: 90%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.component-detail {
  width: 100%;
}
.main-header {
  border: #393E46 solid 1px;
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  margin-bottom: 10px;
}
.main-explanation {
  border: #393E46 solid 1px;
  width: 100%;
  height: 100px;
  padding: 10px;
  box-sizing: border-box;
  margin-bottom: 10px;
}

/* 子コンポーネント内で共通 */
.main-sample {
  border: #393E46 solid 1px;
  color: #222831;
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
}
.main-sample-code {
  border: #393E46 solid 1px;
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  margin-bottom: 10px;
}
pre {
  width: 100%;
  margin: 0;
  padding: 0;
  background-color: #393E46;
  font-size: 0.7rem;
}
code {
  font-family: Monaco, Consolas, "Andale Mono", "DejaVu Sans Mono", monospace;
  color: beige;
}


</style>
