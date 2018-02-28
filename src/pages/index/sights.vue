<template>
	<div class="sights">
	  <ul>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
  	     <li>1</li>
     </ul>
	</div>	
  
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'index-sights',
  props: {
  	list: Array,
  	default: []
  },
  mounted () {
  	const scroll = new BScroll(".sights")
  }
}
</script>

<style lang="stylus" scoped>
.sights
	overflow: hidden 
	height: 1rem
	background: green
</style>
