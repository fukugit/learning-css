<template>
  <div>
    <div class="main-sample">
      <!-- ここの中でHTMLを記述して下さい。 -->

      <div class="main">
        <p>内側のPタグ</p>
      </div>

      <!-- ここまで -->
    </div>

    <div class="main-sample-code">
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        &lt;div class=&quot;main&quot;&gt;
          &lt;p&gt;内側のPタグ&lt;/p&gt;
        &lt;/div&gt;
      </code></pre>
      <!-- ここまで -->
    </div>

    <div class="main-sample-code">
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        .main{
          width: 400px;
          height: 400px;
          /* 左右で中央寄せします。 */
          text-align: center;
          background-color: #42b983;
        }

        p {
          /* 上下で中央寄せします。 */
          line-height: 400px;
        }
      </code></pre>
      <!-- ここまで -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'インライン要素(p)を中央表示',
      explanation: 'text-alignとline-heightを使って 真ん中へ表示します'
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
  /* text-alignを使って左右で中央寄せします。 */
  text-align: center;
  background-color: wheat;
}
p {
  line-height: 100px;
}
</style>
