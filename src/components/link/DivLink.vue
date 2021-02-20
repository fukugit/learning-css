<template>
  <div>
    <div class="main-sample">
      <!-- ここの中でHTMLを記述して下さい。 -->

      <div class="main">
        <a href="https://www.google.com/">Googleへ飛びます。</a>
      </div>

      <!-- ここまで -->
    </div>


    <div class="main-sample-code">
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        &lt;div class=&quot;main&quot;&gt;
          &lt;a href=&quot;https://www.google.com/&quot;&gt;Googleへ飛びます。&lt;/a&gt;
        &lt;/div&gt;
      </code></pre>
      <!-- ここまで -->
    </div>

    <div class="main-sample-code">
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        .main{
          width: 30%;
          height: 100px;
          text-align: center;
          background-color:wheat;
        }
        a {
          /* ブロック要素にして縦横をいっぱいに広げます */
          display: block;
          width: 100%;
          height: 100%;
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
      title: 'Divタグ全体をリンク化する方法',
      explanation: 'aタグの縦横を外側のDiv要素100%に広げることでDiv全体をリンク化します。'
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
  background-color:wheat;
}
a {
  /* ブロック要素にして縦横をいっぱいに広げます */
  display: block;
  width: 100%;
  height: 100%;
}
</style>
