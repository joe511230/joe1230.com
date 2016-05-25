<template>
	<header id="header" class="header">
		<div class="container nav-container">
			<nav class="nav center">
				<div class="nav-l clearfix">
					<h1 class="title">JoE</h1>
					<h2 class="subtitle">FED,OCD,Learning &amp; Coding</h2>
				</div>
				<div class="nav-r">
					<ul class="nav-list">
						<li v-for="link in links" class="nav-item">
							<a v-on:click="toggleClass(link)" v-bind:class="['nav-link',link.active ? 'active' : '']" >{{link.name}}</a>
						</li>
					</ul>
				</div>
			</nav>
		</div>
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
						'url' : "/",
						'name': "主页",
						'active': true
					},{
						'url' : "/video",
						'name': "视频",
						'active': false
					},{
						'url': "/",
						'name': "相册",
						'active': false
					},{
						'url': "/",
						'name': "音乐",
						'active': false
					},{
						'url': "/",
						'name': "简历",
						'active': false
					}
				]
			}
		},
		methods :  {
			toggleClass : function (link) {
				if(link.active) return false;
				else{

				}
			}
		} 
	}
</script>

<style>
	.header{
		border-top: 5px solid #00acee;
	}
	.nav-container{
		border-bottom:1px solid #f2f2f2; 
	}
	.nav{
		display: flex;
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
		line-height: 80px;
	}
	.nav .nav-l .subtitle{
		font-size: 12px;
		color:#bdc3c7;
		padding-left: 16px;
		padding-top: 38px;
	}
	.nav-list{
		display: flex;
		list-style: none;
		margin: 0;
	}
	.nav-list .nav-item{
		flex: 1;
		height: 80px;
		line-height: 80px;
		text-align: center;
	}
	.nav-list .nav-item .nav-link{
		display: inline-block;
		width: 70px;
		height: 35px;
		line-height: 35px;
		font-size: 13px;
		font-weight: bold;
		color: #bdc3c7;
		vertical-align: middle;
		border-radius: 4px;
	}
	.nav-list .nav-item .nav-link.active{
		background-color: #00acee;
		color:#fff;
	}

</style>