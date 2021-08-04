<template>
    <div class="body">
        <p class="text-selectprovince">เลือกจังหวัด</p>
        <select v-model="province" class="combobox">
            <option value="" selected disabled>กรุณาเลือกจังหวัด</option>
            <option  v-for="p in provinceArr" :key="p.province_code" >{{p.province_name_th}}</option>
        </select>
        <div class="d-flex justify-content-center">
            <button class="bt ">ตกลง</button>
        </div>
        <div class="box d-flex justify-content-center align-items-center">
            <p class="text-province">{{province}}</p>
        </div>
        
    </div>
    
</template>

<script>

export default {
  async asyncData({ $axios }) {
        const res = await $axios.$get(process.env.API)
        return {
            provinceArr: res.result.data
        }
    },
    data(){
        return{
            provinceArr: null,
            province: '',
        }
    }, 
    methods:{
        show(){

        }
    } 
}
</script>

<style scoped>
.body{
    margin: 50px 123px 0px 123px;
}
.combobox{
    font-size: 30px;
    width: 100%;
}
.text-selectprovince{
    font-size: 30px;
}
.bt{
  background-color: rgb(63, 63, 63);
  color: white;
  font-size: 45px;
  padding: 5px 5vw;
  border-radius: 15px;
  border: none;
  margin: 46px 0px;
}
.text-province{
    font-size: 45px;
}
.box{
    border: 0.5px solid black;
    min-height: 200px;
}
</style>