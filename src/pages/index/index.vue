<template>
	<div>
      <index-head></index-head>
      <index-swiper :list="swiperInfo"></index-swiper>
      <index-icon :list="icons"></index-icon>
      <index-sights></index-sights>
	</div>
</template>

<script>
import IndexHead from './head'
import IndexSwiper from './swiper'
import IndexIcon from './icon'
import IndexSights from './sights'

import axios from 'axios'
export default {
  name: 'index',
  components: {
    IndexHead,
    IndexSwiper,
    IndexIcon,
    IndexSights
  },
  data () {
  	return {
  		swiperInfo: [],
  		icons: []

  	}
  },
  methods: {
   getIndexData () {
   	axios.get('api/index.json')
   .then(this.handleGetDataSucc.bind(this))
   .catch(this.handleGetDataError.bind(this))
   },
   handleGetDataSucc (res) {
    const data = res.data.data
    this.swiperInfo = data.swiper
    console.log(this.swiperInfo)
    this.icons = data.icons
   },
   handleGetDataError () {
    console.log('2222')
   }
   
  },
  created () {
    this.getIndexData()
  }
}
</script>

<style>

</style>
