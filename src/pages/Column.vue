<template>
  <div class="Column">
   <Cell
     v-for="item of column"
     :key="item._id"
     :data="item"
     api-name="column"
   />
  </div>
</template>

<script>
  import Cell from '../components/Cell'
  export default {
    name:'Column',
    props:{},
    data(){
      return {
        column:[
			
		]
      }
    },
    components:{
      Cell
    },
    mounted(){
      this.$axios({
        url:'/api/goods/banner',
        params:{_page:1,_limit:1},
      }).then(
        res=>this.column = res.data.data
      )
    },
    updated(){},
    methods:{}
  }
</script>

<style scoped>
  .Column{
    margin-top: .6rem;
    margin-left: 0.4rem;
    margin-right: 0.4rem;
  }
</style>
