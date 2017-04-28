<template>
  <div class="resume">
  	<div class="resume-container">
  		<div class="resume-left">
  			<h2 class="name">甘釜宾</h2>
  			<div class="base">
  				<label class="title">基本信息</label>	  			
	  			<h4>职业：前端开发工程师</h4>
	  			<h4>联系电话：15505923453</h4>
	  			<h4>籍贯：重庆璧山</h4>
	  			<h4>工作经验：两年</h4>
	  			<h4>邮箱：1209711358@qq.com</h4>
  			</div>
  			<div class="education">
  				<label class="title">教育背景</label>
  				<h4>学历：本科</h4>
  				<h4>毕业院校：厦门理工学院</h4>
  				<h4>毕业时间：2016.06.25</h4>
  			</div>
  			<div class="skill">
  				<label class="title">专业技能</label>
  				<div class="sk top">
  					<div class="sk-title">html：</div>
  					<div class="sk-wrap">
  						<div class="sk-per">
  							<div class="html"></div>
  						</div>
  					</div>
  				</div>
  				<div class="sk">
  					<div class="sk-title">js：</div>
  					<div class="sk-wrap">
  						<div class="sk-per">
  							<div class="js"></div>
  						</div>
  					</div>
  				</div>
  				<div class="sk">
					<div class="sk-title">css：</div>
  					<div class="sk-wrap">
  						<div class="sk-per">
  							<div class="css"></div>
  						</div>
  					</div>
  				</div>
  			</div>
  		</div>
  		<div class="resume-right">
  			<div class="blog">
  				<div class="link github">Github: <a target="_blank" href="https://github.com/ganfubin">https://github.com/ganfubin</a></div>
  			</div>
  			<div class="work-exp">
  				<label class="title">工作经历</label>
  				<div class="work-exp-title">
  					<label class="title-name">德医互联</label>
					<div class="title-date">2017.04 - 至今</div>
  				</div>
  				<div class="work-exp-title">
  					<label class="title-name">科技谷</label>
					<div class="title-date">2015.11 - 2017.04</div>
  				</div>	
  			</div>
  			<div class="project-exp">
  				<label class="title">项目经验</label>
  				<div class="project-exp-container">
  					<label class="project-name">vue 项目重构迁移/vue-cil + sass + jquery</label>
					<div class="project-desc">通过 vue-cil 来迁移项目,主要用到 vue 的一些基础 api,在这个过程中主要负责用 sass 来重写样式,包括 重置 bootstrap 样式,和根据 ui 设计来更改以前项目 ui 界面。</div>
  				</div>
  				<div class="project-exp-container">
  					<label class="project-name">用户画像/jquery + require</label>
					<div class="project-desc">用铁道部的数据做数据打标签,刻画用户画像等,用 jq,require,director,bootstarp,datatable, ztree.js 等插件。
					整个项目是前后端分离,我们布局基于 bootstarp3来布局,实现前后端交互。通过 ajax 实现数据请求,再 通过 js 转换需要格式,最后实现数据展示。
					</div>
  				</div>
  				<div class="project-exp-container">
  					<label class="project-name">开放平台/jquery + require</label>
					<div class="project-desc">项目涉及到许多插件和库,比如 jq,require,director,bootstarp,d3,echart,undesorse 等,主要实 现的是数据的可视化,搜索展现数据 ,利用 可视化 图表。整个项目是前后端分离,我们布局基于 bootstarp3来布局,通过 ajax 实现数据交换进而实现前后端交互。 有应用到 dashboard,大量使用 template 技术。
					</div>
  				</div>
  			</div>
  		</div>
  	</div>
  	<div v-html="resStyleCode"></div>
  </div>
</template>

<script>
export default {
  	data () {
    	return {
     		resStyleCode: ''
    	}
  	},
  	methods:{
	    writeRsesumeCss: function (code) {
	        this.resStyleCode = "<style>"+code+"</style>"
	    }
	}
}
</script>

<style scoped>
	/*简历整体*/
	.resume{
		width: 70%;
		height: 100%;
		float: right;
		box-sizing: border-box;
    	padding: 15px;
	}
	.resume-container{
		height: 100%;
		box-shadow: 0 4px 12px 0 rgba(0,0,0,0.5);
		border-radius: 4px;
	}
	.resume-container .title{
		border-left: 3px solid #0880f1;
		padding-left: 5px; 
	}

	/*简历左侧*/
/*	.resume-left{
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
	}*/


	/*简历右侧*/
	/*.resume-right{
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
	}*/
</style>
