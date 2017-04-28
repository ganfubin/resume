<template>
  <div id="app">
    <!-- 左侧csscode模块-->
    <cmptLeft ref="cssModule"></cmptLeft>
    <!-- 右侧简历模块-->
    <cmptRight ref="resumeModule"></cmptRight>
  </div>
</template>

<script>
import cmptLeft from 'components/css-code.vue';
import cmptRight from 'components/resume.vue'
export default {
  name: 'app',
  data() {
    return {
        cssCode : ` 
          /*简历左侧*/
          .resume-left{
            width: 40%;
            float:left;
            height: 100%;
            padding: 15px;
            box-sizing: border-box;
            background: #ececec;
            border-right: 1px solid #e9e9e9;
            overflow: auto;
          }
          .resume-left .name{
            text-align: center;
          }
          
          .resume-left h4{
            text-align: center;
          }
          .resume-left .skill .sk .sk-title{
            text-align: right;
            width: 30%;
          }
          .resume-left .skill .sk .sk-wrap{
            width: 70%;
              height: 18px;
              border-radius: 4px;
              position: relative;
              top: -18px;
              padding-left: 30%;
          }
          .resume-left .skill .sk.top{
            margin-top: 21.8px;
          }
          .resume-left .skill .sk + .sk{
            margin-top: 10px;
          }
          .resume-left .skill .sk .sk-wrap .sk-per{
            width: 100%;
            background: rgba(151, 151, 151, 0.5);
              border-radius: 4px;
              height: 100%;
          }
          
          .resume-left .skill .sk .sk-wrap .html{
            width: 40%;
            height: 18px;
            background: rgba(151, 151, 151, 0.9);
            border-radius: 4px;
          }
          .resume-left .skill .sk .sk-wrap .js{
            width: 60%;
            height: 18px;
            background: rgba(151, 151, 151, 0.9);
            border-radius: 4px;
          }
          .resume-left .skill .sk .sk-wrap .css{
            width: 40%;
            height: 18px;
            background: rgba(151, 151, 151, 0.9);
            border-radius: 4px;
          }


          /*简历右侧*/
          .resume-right{
            width: 60%;
            float:right;
            height: 100%;
            padding: 15px;
            box-sizing: border-box;
            overflow: auto;
          }
          .resume-right .blog{
            text-align: right;
          }
          .resume-right .work-exp{
            margin-top: 15px;
          }
          .resume-right .work-exp .work-exp-title{
            padding: 15px 15px 0 15px;
          }
          .resume-right .work-exp .title-date{
            float: right;;
          }
          .resume-right .project-exp{
            margin-top: 15px;
          }
          .resume-right .project-exp .project-exp-container{
            padding: 15px 15px 0 15px;
          }`
    }
  },
  created(){
      let n = 0;
      let _vm = this;
      this.$nextTick(function () {
          let len = _vm.cssCode.length;
          var setIn = setInterval(function () {
              _vm.$refs.cssModule.writeStyleCode(_vm.cssCode.substring(0, n));
              _vm.$refs.resumeModule.writeRsesumeCss(_vm.cssCode.substring(0, n));
              n++;
              if (n >= len) {
                  clearInterval(setIn);
              }
          }, 50);
      })
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
