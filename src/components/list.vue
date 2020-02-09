<template>
  <div class="list">
   <ul>
       <li v-for="(item,index) in msg" :key="index" v-show="!state">{{item.title}}</li>
   </ul>
  </div>
</template>

<script>



import axios from "axios"
export default {
  name: 'list',
  data() { 
    return {
      msg:'',
      state:false
    }
  },
  props: {

  },
  components:{
  },
  mounted() {
    axios.get("https://cnodejs.org/api/v1/topics").then((res)=>{
        console.log(res)
        this.msg=res.data.data
    })
  },
  methods:{

  },
 }
</script>

<style>
</style>