<template>
  <div class="header">
  	<div class="back iconfont">&#xe660;</div>
  	<div class="seach">
  		<span class="iconfont serch-icon">&#xe672;</span>
  	请输入搜索内容
    </div>
  	<div class="city">binghkhk</div>
  </div>
</template>

<script>
export default {
  name: 'index-head'
}
</script>

<style lang="stylus" scoped>
// @import "../../assets/css/stylus/varibles.styl"
.header
	display: flex
	height: .88rem
	background: red
	line-height: .88rem
	color: #fff
	.back
		width: .58rem
		text-align: center
		font-size: .4rem
		font-weight: bold
	.seach
		flex: 1
		margin: .14rem .2rem
		padding-left: .4rem
		height: .6rem
		background: #fff
		border-radius: .1rem
		color: #919191
		line-height: .6rem
		.serch-icon
			padding-right: .04rem
	.city
		padding-right: .6rem
		position: relative
		&:before
			position: absolute
			top: .34rem
			right: .2rem
			content: "\0020"
			width: 0
			height: 0
			border-left: .14rem solid transparent
			border-right: .14rem solid transparent
			border-top: .14rem solid #fff
</style>
