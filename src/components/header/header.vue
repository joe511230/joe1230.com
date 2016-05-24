<template>
	<header id="header" class="header">
		<nav class="nav">
			<div class="nav-l clearfix">
				<h1 class="title">JoE</h1>
				<h2 class="subtitle">FED,OCD,Learning &amp; Coding</h2>
			</div>
			<div class="nav-r">
				<ul class="nav-list">
					<li v-for="link in links" class="nav-item">
						<a v-bind:href="link.url">{{link.name}}</a>
					</li>
				</ul>
			</div>
		</nav>
		<joe-banner></joe-banner>
	</header>
</template>


<script>
	import JoeBanner from "./banner.vue";
	export default{
		components:{
			JoeBanner
		},
		data :function () {
			return {
				links: [
					{
						url : "/",
						name: "主页"
					},{
						url : "/video",
						name: "视频"
					},{
						url: "/",
						name: "相册"
					},{
						url: "/",
						name: "音乐"
					},{
						url: "/",
						name: "简历"
					}
				]
			}
		} 
	}
</script>

<style>
	.nav{
		display: flex;
		height: 80px;
		line-height: 80px;
	}
	.nav .nav-l,
	.nav .nav-r{
		flex: 1;
	}
	.nav .nav-l .title,
	.nav .nav-l .subtitle{
		float: left;
		margin: 0;
	}
	.nav .nav-l .title{
		font-size: 32px;
		color: #00acee;
	}
	.nav .nav-l .subtitle{
		font-size: 12px;
		color:#bdc3c7;
		padding-left: 16px;
	}
	.nav-list{
		display: flex;
		list-style: none;
		margin: 0;
	}
	.nav-list .nav-item{
		flex: 1;
	}

</style>