<template>
  <div class="css">
    <div class="css-container">
      <pre class="pre-code"></pre>
    </div>

  </div>
</template>

<script>
export default {
  name: 'css',
  data () {
    return {
     
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
  }
  .pre-code{
     height: 100%;
     margin: 0;
  }

</style>
