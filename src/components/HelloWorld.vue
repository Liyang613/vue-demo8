<template>
  <div class="hello">
    <ul>
      <li>
        <router-link to="/list">首页</router-link>
      </li>
      <li>招聘</li>
      <router-veiw></router-veiw>
    
    </ul>
   
   父组件
   <List></List>
  </div>
</template>

<script>
import List from "../components/list"
import axios from "axios"
export default {
  name: 'HelloWorld',
  data () {
    return {
      // msg: ''
    }
  },
  components:{
     List
  },
  
  mounted() {
  //  axios.get("https://cnodejs.org/api/v1/topics").then((res)=>{
  //    console.log(res)
      // this.msg=res.data.data
  //  })
  },
  methods:{

  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
  list-style-type: none;
  padding: 0;
  background: yellowgreen;
  height:40px;
  line-height:40px;
  text-align:left;
}
li {
  display: inline-block;
  margin: 0 10px;

}

</style>
