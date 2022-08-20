<script>
import DeviceUtil from './assets/js/DeviceUtil'
export default{
  data() {
	  return {
    	scheme: "niopower://peservice/sourcebook?id=123"
  	}
	},
  methods:{
    submit(){
      if(this.scheme.length == 0){
        alert('please input shceme!')
        return
      }
      window.location.href= this.shceme;
      setTimeout(function(){
                window.location.href= "https://www.baidu.com";
            },3000)
      if(DeviceUtil.android()){
          
      }else if(DeviceUtil.ios()){

      }else if(DeviceUtil.browser()){

      }
    }
  }
}
</script>

<template>
  <header>
    <p>Scheme:</p>
    <input type="text" v-bind:value="scheme" placeholder="scheme://host/path?params"/>
    <button v-on:click="submit" >submit</button>
  </header>

</template>

<style>
header {
  width:100%;
}

input {
  flex: 1;
  margin-left: 10px;
}
button{
  margin-left: 10px;
}
</style>
