<template>
  <div>
    <div class="main">
      <p>インライン要素</p>
    </div>
    <br>
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
  </div>
</template>

<style scoped>
.main{
  width: 400px;
  height: 400px;
  /* text-alignを使って左右で中央寄せします。 */
  text-align: center;
  background-color: #42b983;
}
p {
  line-height: 400px;
}
</style>
