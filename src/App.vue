<template>
  <div id="app">
    <!-- 左侧csscode模块-->
    <cmptLeft></cmptLeft>
    <!-- 右侧简历模块-->
    <cmptRight></cmptRight>
  </div>
</template>

<script>
import cmptLeft from 'components/css-code.vue';
import cmptRight from 'components/resume.vue'
export default {
  name: 'app',
  data() {
    return {

    }
  },
  components: {
    cmptLeft,
    cmptRight
  }

}
</script>

<style lang='scss'>
  /*基础样式重置*/
  @import '~normalize.css/normalize.css';
  /*公共样式*/
  @import 'assets/style/_commom.scss';
</style>

<style lang="scss" scoped>
  #app{
    height: 100%;
    width: 100%;
  }

</style>
