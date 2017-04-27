<template>
  <div class="resume">
  	<div class="resume-container">
  		<div class="resume-left"></div>
  		<div class="resume-right"></div>
  	</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
     
    }
  }
}
</script>

<style scoped>
	.resume{
		width: 70%;
		height: 100%;
		float: right;
		box-sizing: border-box;
    	padding: 15px;
	}
	.resume-container{
		height: 100%;
	}
	.resume-left{
		width: 40%;
		float:left;
		height: 100%;
	}
	.resume-right{
		width: 60%;
		float:right;
		height: 100%;
	}

</style>
