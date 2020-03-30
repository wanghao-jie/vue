<template>
	<div class="Follow">
   <Cell
       v-for="(item,index) of list"
       :key="item._id"
       :data="item"
       :index="index"
       api-name="column"
     />
   
	  </div>
	
</template>

<script>
	import Cell from '../components/Cell.vue';
	import axios from 'axios'
	export default{
		name:'Follow',
		props:{},
		data(){
			return{
				list:[
					{_id:1,title:'alax1',des:'ooo1'},
					{_id:2,title:'alax2',des:'ooo2'},
					{_id:3,title:'alax3',des:'ooo3'},
					]
			}
		},
		components:{
			Cell
		},
		mounted(){
			// axios({
			//     url:'/api/goods/follow',
			//     params:{_page:1,_limit:8},
			//   }).then(
			//     res=>this.follow = res.data.data
			//   )
			
		},
		updated(){
		},
		methods:{},
	}
</script>

<style scoped>
	.Follow{
	    margin-top: .6rem;
	    margin-left: 0.4rem;
	    margin-right: 0.4rem;
	  }
	
</style>
