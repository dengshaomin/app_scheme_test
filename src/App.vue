<script>
import DeviceUtil from './assets/js/DeviceUtil'
export default{
  data() {
	  return {
    	scheme: "niopower://peservice/sourcebook?id=PS-NIO-MAN00021-00000003"
  	}
	},
  methods:{
    submit(){
      if(this.scheme.length == 0){
        alert('please input shceme!')
        return
      }
      setTimeout(function(){
                    window.location.href= "https://www.baidu.com";
                },3000)
      window.location.href = this.shceme;

      if(DeviceUtil.android()){
          
      }else if(DeviceUtil.ios()){
          
      }else if(DeviceUtil.browser()){

      }
    }
  }
}
</script>

<template>
  <div>
    <p>Scheme:</p>
    <input type="text" v-model="scheme" placeholder="scheme://host/path?params"/>
    <a :href="scheme">open app</a>
  </div>

</template>

<style>
p{
  display: inline;
}
a{
  margin-left: 10px;
  border: 2px solid rgb(0, 255, 72);
  border-radius: 5px;
}
header {
  display: flex;
  margin-left: 0px;
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
