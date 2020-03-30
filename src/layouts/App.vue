<template>
  <div id="app">
	  <loading v-if="$root.bLoading"/>
	  <Header v-if="$root.bNav"/>
	<router-view></router-view>
    <Footer v-show="$root.bFoot"/>
	
  </div>
</template>

<script>
  
   // 首页	 的引入 
import Header from './Header.vue';
import Footer from './Footer.vue';
import Loading from '../components/loading.vue'

export default {
  name: 'App',
  components: {
    Header,Loading,Footer
  },

watch:{
	$route:{ // 路由监听，属性检测
	handler(nextValue,PrevValue){
		console.log('路由变化了',nextValue);
		
		let path = nextValue.path;
		
		
		if(/home|follow|column/.test(path)){
			this.$root.bNav = this.$root.bFoot = true;
		}
		if(/Detail|login|reg/.test(path)){
			this.$root.bNav = this.$root.bFoot=false;
		}
		if(path.includes('/user')){//user
		  this.$root.bNav=false;
		  this.$root.bFoot=true;
		}
		},
		immediate:true	
	 }	
	}
}



</script>

<style scoped>

</style>
