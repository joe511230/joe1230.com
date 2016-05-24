<template>
	<div class="wrapper">
  		<joe-header></joe-header>
	</div>
</template>

<script>
import JoeHeader from "./components/header/header.vue";
import Hello from "./components/Hello.vue";
export default {
  components: {
    JoeHeader
  }
}
</script>
<style>
	html,
	body{
		height: 100%;
	}
	.wrapper{
		width: 1170px;
		margin: 0 auto;
	}
	.clearfix:after{content:"";display:block;height:0;clear:both;visibility:hidden}
</style>
