<template>
  <div class="css">
    <div class="css-container js-css-container">
      <pre class="pre-code" v-html="styleMsg"></pre>
    </div>

  </div>
</template>

<script>
export default {
  name: 'css',
  data () {
    return {
      styleMsg: ""
    }
  },
  methods: {
    writeStyleCode: function (code) {
          this.styleMsg = code;
          // 每写一行 code ，滚动条滚动到最下面
          document.getElementsByClassName('js-css-container')[0].scrollTop = 
          document.getElementsByClassName('js-css-container')[0].scrollHeight;
    }
  }
}
</script>

<style scoped>
  .css{
    width: 30%;
    height: 100%;
    float: left;
    box-sizing: border-box;
    padding: 15px;
  }
  .css-container{
    height: 100%;
    border-radius: 4px;
    box-shadow: 0 4px 12px 0 rgba(0,0,0,0.5);
    overflow: auto;
  }
  .pre-code{
     height: 100%;
     margin: 0;
  }

</style>
