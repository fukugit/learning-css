<template>
  <div>
    <div class="main">
      <div class="box">ブロックレベル要素</div>
    </div>
    <br>
    <pre><code>
      .main{
        border: 1px solid #aaa;
        width: 400px;
        height: 400px;
        text-align: center;
        background-color: #42b983;
        position: relative;
      }

      .box {
        width: 200px;
        height: 200px;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        position: absolute;
        margin: auto;
        background-color: wheat;
        line-height: 200px;
      }
    </code></pre>
  </div>
</template>

<style scoped>
.main{
  width: 400px;
  height: 400px;
  text-align: center;
  background-color: #42b983;
  position: relative;
}
.box {
  width: 200px;
  height: 200px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  position: absolute;
  margin: auto;
  line-height: 200px;
  background-color: wheat;
}
</style>
