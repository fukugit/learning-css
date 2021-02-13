<template>
  <div>
    <div class="main">
      <p>インライン要素</p>
    </div>
    <pre><code>
    .main{
      border: 1px solid #aaa;
      width: 400px;
      height: 400px;
      /* text-alignを使って左右で中央寄せします。 */
      text-align: center;
      background-color: #42b983;
    }
    </code></pre>
  </div>
</template>

<style scoped>
.main{
  border: 1px solid #aaa;
  width: 400px;
  height: 400px;
  /* text-alignを使って左右で中央寄せします。 */
  text-align: center;
  background-color: #42b983;
}
p {
  background-color: wheat;
}
</style>
