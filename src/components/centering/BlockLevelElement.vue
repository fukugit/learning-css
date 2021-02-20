<template>
    <div>

    <div class="main-sample">
      <div class="main">.main
        <div class="box">.box</div>
      </div>
    </div>

    <div class="main-sample-code">
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        &lt;div class=&quot;main&quot;&gt;.main
          &lt;div class=&quot;box&quot;&gt;.box&lt;/div&gt;
        &lt;/div&gt;
      </code></pre>
      <!-- ここまで -->
    </div>


    <div class="main-sample-code">
      <pre><code>
      .main{
        width: 30%;
        height: 100px;
        text-align: center;
        background-color: wheat;
        position: relative;
      }

      .box {
        width: 30%;
        height: 50px;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        position: absolute;

        /* 絶対値にしてdivを中央に持ってきます */
        margin: auto;

        /* 文字を上下中央に持ってきます。 */
        line-height: 50px;

        background-color: #393E46;
        color: whitesmoke;
      }
      </code></pre>
    </div>

  </div>

</template>

<script>
export default {
  data() {
    return {
      title: 'ブロックレベル要素(div)を中央表示',
      explanation: 'positionとmarginとline-heightを使って中央表示を実現しています。'
    }
  },
  activated() {
    this.$emit("title", this.title, this.explanation);
  }
}
</script>

<style scoped>
.main{
  width: 30%;
  height: 100px;
  text-align: center;
  background-color: wheat;
  position: relative;
}
.box {
  width: 30%;
  height: 50px;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  position: absolute;

  /* 絶対値にしてdivを中央に持ってきます */
  margin: auto;

  /* 文字を上下中央に持ってきます。 */
  line-height: 50px;

  background-color: #393E46;
  color: whitesmoke;
}
</style>
