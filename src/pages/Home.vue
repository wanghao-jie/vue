<template>
  <div class="Home">
    
   <swiper
      :data="list"
      apiName="banner"
    />
    
    <div class="home-m-l-r">
      <Cell
        v-for="(item,index) of banner"
		:key="item.id"
        :data="item"
        :index="index"
        api-name="home"
      />
    </div>
    
    
  </div>
</template>

<script>
  import swiper from '../components/swiper.vue'
  import Cell from '../components/Cell.vue'
  export default {
    name:'Home',
    props:{},
    data(){
      return {
        list:[],
        banner:[]
      }
    },
    components:{
      swiper,Cell
    },
    mounted(){
	
      axios({ 
		url:'/api/goods/banner',
        params:{_page:1,_limit:3},
      }).then(
        res=>{
			this.list = res.data.data;
			console.log(this.list)
		}
      )
      
      axios({
        url:'/api/goods/home',
        params:{_page:1,_limit:5},
      }).then(
        res=>{this.banner = res.data.data;
		console.log('banner', res.data.data)
		}
      )
      
    },
    updated(){},
    methods:{
		
	}
  }
</script>

<style scoped>
  .Home{
    /* background: #999999; */
  }
  .home-m-l-r{
    margin: 0 0.4rem;
  }
</style>

{ "_id" : { "oid" : "5c8a308be850280074ed5be4" }, "title" : "1", "sub_title" : "", "banner" : "/upload/noimage.jpg", "time" : 1552560266841, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : "b", "content" : "<p><br></p>" } }
{ "_id" : { "oid" : "5c8a309ae850280074ed5be5" }, "title" : "2", "sub_title" : "", "banner" : "/upload/noimage.jpg", "time" : 1552560281691, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : "a", "content" : "<p><br></p>" } }
{ "_id" : { "oid" : "5c8a30aee850280074ed5be6" }, "title" : "3", "sub_title" : "", "banner" : "/upload/banner/8534e87286554c5d28255d6fa9081ef3.jpg", "time" : 1552560301002, "detail" : { "icon" : "/upload/banner/51a5a85d371fe9b41cbab6dcb0430451.jpg", "auth" : "c", "content" : "<p><br></p>" } }
{ "_id" : { "oid" : "5cb985a05e768425303efd3d" }, "title" : "大标题大标题大标题", "sub_title" : "小标题小标题小标题", "banner" : "/upload/banner/4aa51a26d59a544c9c800e931f77f991.jpg", "time" : 1555662239735, "detail" : { "icon" : "/upload/user/3244a3c5ccc97f0851cf850d7a4260e8.jpg", "auth" : "uncle9", "content" : "<p>段落</p>" } }
{ "_id" : { "oid" : "5cc0116a2577c007943ebc50" }, "title" : null, "sub_title" : null, "banner" : "/upload/noimage.jpg", "time" : 1556091241912, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : "uncle9", "content" : "<p>段落</p>" } }
{ "_id" : { "oid" : "5cc01327d2bf080850710d3e" }, "title" : "123321", "sub_title" : "小标题小标题小标题", "time" : 1556091686755, "detail" : { "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc01424ff3d4327581df3e3" }, "title" : "123321", "sub_title" : "小标题小标题小标题", "banner" : "/upload/noimage.jpg", "time" : 1556091938932, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc01439ff3d4327581df3e4" }, "title" : "大标题大标题大标题789", "sub_title" : "小标题小标题小标题", "banner" : "/upload/banner/9b861f466bf1bfd5be647f1c25cc18e3.jpg", "time" : 1556091960458, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : "uncle9", "content" : "<p>段落</p>" } }
{ "_id" : { "oid" : "5cc01440ff3d4327581df3e5" }, "title" : "大标题大标题大标题789", "sub_title" : "小标题小标题小标题", "banner" : "/upload/noimage.jpg", "time" : 1556091967512, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : "uncle9", "content" : "<p>段落</p>" } }
{ "_id" : { "oid" : "5cc014d3ff3d4327581df3e6" }, "title" : "123321", "sub_title" : "小标题小标题小标题", "banner" : "/upload/noimage.jpg", "time" : 1556092114070, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc01527ff3d4327581df3e7" }, "title" : "123321labula", "sub_title" : null, "banner" : "/upload/noimage.jpg", "time" : 1556092198180, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc0155cff3d4327581df3e8" }, "title" : "aa123321labula", "sub_title" : null, "banner" : "/upload/noimage.jpg", "time" : 1556092251613, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc019deb914c1085057abbf" }, "title" : "aa123321labula", "sub_title" : null, "banner" : "/upload/noimage.jpg", "time" : 1556093405723, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cc125e18b51e80450dc82bb" }, "title" : "aa123321labula", "sub_title" : "11", "banner" : "/upload/banner/d00898aad853bb6018b0a86fe81cb7df.jpg", "time" : 1556162016463, "detail" : { "icon" : "/upload/banner/400c12d99f845a9f3969dd989dfbfb89.jpg", "auth" : "333", "content" : "22<b>2</b>22" } }
{ "_id" : { "oid" : "5cdbb0a873ce30208080e360" }, "title" : "123", "sub_title" : "adfadf", "banner" : "/upload/noimage.jpg", "time" : 1557901479226, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cf8798751b5140fa8d14394" }, "title" : "2019-6-7", "sub_title" : "adfadf123", "banner" : "/upload/noimage.jpg", "time" : 1559788009391, "detail" : { "icon" : null, "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cf87af7fc4ed92368d396f9" }, "title" : "2019-6-77", "sub_title" : "adfadf12333", "banner" : "/upload/banner/60808848d4768d2f0eecc55b1a02bd74.jpg", "time" : 1560511236613, "detail" : { "icon" : "/upload/noimage.jpg", "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cf87b57fc4ed92368d396fa" }, "title" : "cc", "sub_title" : "cc", "banner" : "/upload/banner/4abc406e51159dceef6f1cefd1d22c50.jpg", "time" : 1560510880316, "detail" : { "icon" : null, "auth" : "uncle9", "content" : "xxx" } }
{ "_id" : { "oid" : "5cf891bd65dff127ec8f83f9" }, "title" : "123cc", "sub_title" : "cc123", "banner" : "/upload/banner/a1a68a7e062fa21cd158332de28d0d24.jpg", "time" : 1560510747910, "detail" : { "icon" : null, "auth" : null, "content" : null } }
{ "_id" : { "oid" : "5cf891cc65dff127ec8f83fa" }, "title" : "1234cc", "sub_title" : "cc1234", "banner" : "/upload/banner/1f3fec4832ab2eabddf9c9bdd96ad246.jpg", "time" : 1560510686465, "detail" : { "icon" : null, "auth" : null, "content" : null } }
Type "it" for more