<template>
<div class="slide-container">
  <swiper :options="swiperOption" v-if="hasSwiper">
    <swiper-slide v-for="item of list" :key="item.id">
     <img class="slide-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
   </swiper>
  </div>
</template>

<script>
export default {
  name: 'index-swiper',
  props: {
   list: Array
  },
  data () {
  	return {
  		swiperList: [],
  		swiperOption: {
  			loop: true,
  			pagination : '.swiper-pagination'
  		}
  	}
  },
  computed: {
    hasSwiper () {
      return !!this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
.slide-container
	overflow: hidden
	height: 0
	padding-bottom: 31.25%
.slide-img
	width: 100%
.swiper-pagination >>> .swiper-pagination-bullet-active
	background: red !important

</style>
