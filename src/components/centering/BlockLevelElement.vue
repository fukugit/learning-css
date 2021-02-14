<template>
  <div>
    <div class="main">
      <div class="box">ブロックレベル要素</div>
    </div>
    <br>
    <pre><code>
      .main{
        text-align: center;
        position: relative;
        width: 400px;
        height: 400px;
        background-color: #42b983;
      }

      .box {
        position: absolute;

        /* 絶対値にしてdivを中央に持ってきます */
        margin: auto;

        /* 文字を上下中央に持ってきます。 */
        line-height: 200px;

        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        height: 200px;
        width: 200px;
        background-color: wheat;
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
