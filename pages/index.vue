<template>
  <div class="body">
    <p class="text1">พวกเราพร้อมส่งสินค้า</p>
    <p class="text2">เพื่อคุณตลอดเวลา</p>
    <NuxtLink to="/pop">
      <button class="bt">พบกันเร็วๆ นี้</button>
    </NuxtLink>
    
  </div>
</template>

<script>
export default {
    
     
}

</script>

<style scoped>
.body{
  margin-left: 300px;
 
}
.text1{
  margin-top: 348px;
  margin-right: 936px;
  font-size: 58px;
  font-weight: bold;
}
.text2{
  margin-bottom: 58px;
  font-size: 45px;
}
.bt{
  margin-bottom: 422px;
  background-color: rgb(63, 63, 63);
  color: white;
  font-size: 45px;
  padding: 10px 30px;
  border-radius: 15px;
  border: none

}
</style>