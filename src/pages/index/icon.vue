<template>
	<div class="icon">
	 <swiper :options="swiperOption">
      <swiper-slide  v-for="(page, index) of pageList" :key="index">
       <div class="area-con">
	       	<div class="area-item" v-for="item in page" :key="item.id">
	       		<img  class="area-img" :src="item.imgUrl"/>
	       		<p class="area-desc">{{item.description}}</p>
	       	</div>
       </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
     </swiper>
	</div>
  
</template>

<script>
export default {
  name: 'index-icon',
  props: {
  	list: Array
  },
   data () {
  	return {
  		swiperList: [],
  		swiperOption: {
  			pagination : '.swiper-pagination'
  		}
  	}
  },
  computed: {
  	pageList () {
  		const pages = []
  		this.list.forEach((value, index) => {
        const page = Math.floor(index / 8)
        if(!pages[page]) {
        	pages[page] = []
        }
        pages[page].push(value)
  		})
  		return pages
  	}
  }
}
</script>

<style lang="stylus" scoped>
.icon
	height: 3.8rem
	overflow: hidden
	.area-con
		display: flex
		flex-wrap: wrap
		.area-item
			width: 25%
			height: 1.9rem
			.area-img
				display: block
				margin: .3rem auto .2rem auto
				width: .9rem
				height: .9rem
			.area-desc
				overflow: hidden
				white-space: nowrap
				text-overflow: ellipsis
				line-height: .4rem
				text-align: center
				
		
</style>
