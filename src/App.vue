<template>
	<div class="wrapper">
  		<joe-header></joe-header>
  		<joe-section></joe-section>
	</div>
</template>

<script>
import JoeHeader from "./components/header/header.vue";
import JoeSection from "./components/section/section.vue";
import Hello from "./components/Hello.vue";
export default {
  components: {
    JoeHeader,
    JoeSection
  }
}
</script>
<style>
	html,
	body{
		height: 100%;
	}
	a{
		text-decoration: none;
	}
	.wrapper{
		min-width: 1170px;
	}
	.clearfix:after{content:"";display:block;height:0;clear:both;visibility:hidden}
	.center{
		width: 1170px;
		margin: 0 auto;
	}
</style>
