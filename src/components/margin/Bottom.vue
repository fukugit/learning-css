<template>
  <div>
    <div class="main-sample">
      <!-- ここの中でHTMLを記述して下さい。 -->

      <div class="main">.main
        <div class="box">.box</div>
      </div>

      <!-- ここまで -->
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
      <!-- ここの中でコードを記述して下さい。 -->
      <pre><code>
        .main{
          position: relative;
          width: 30%;
          height: 100px;
          text-align: center;
          background-color: wheat;
        }
        .box {
          width: 100%;
          height: 30px;
          position: absolute;
          text-align: center;
          bottom: 0;
          background-color: #393E46;
          color: whitesmoke;
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
      title: '要素内の一番下に要素を配置する方法',
      explanation: '親要素はrelativ, 子要素はabsoluteとして、子要素内でbottomの設定を行います。'
    }
  },
  activated() {
    this.$emit("title", this.title, this.explanation);
  }
}
</script>

<style scoped>
.main{
  position: relative;
  width: 30%;
  height: 100px;
  text-align: center;
  background-color: wheat;
}
.box {
  width: 100%;
  height: 30px;
  position: absolute;
  text-align: center;
  bottom: 0;
  background-color: #393E46;
  color: whitesmoke;
}
</style>
