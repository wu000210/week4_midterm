<template>
  <div class="about container">
    <h1>{{ about }} </h1>
    <el-row>
  <el-col :span="12"><div class="grid-content bg-purple">
    <img src="../assets/images/2.jpeg" alt="">   </div></el-col>
  <el-col :span="12"><div class="grid-content bg-purple-light">
    <p>{{ Lorem }}</p>
      </div></el-col>
</el-row>
<el-row>
  <el-col :span="12"><div class="grid-content bg-purple">
  <p>{{ Lorem }}
    </p> </div></el-col>
  <el-col :span="12"><div class="grid-content bg-purple-light">
  <img src="../assets/images/3.jpeg" alt="">   </div></el-col>
</el-row>
</div>
</template>

<script>
export default {
    data() {
      return {
        about:"About The Vue App",
        Lorem:"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec sodales, urna at vulputate feugiat, nulla ex gravida augue, sit amet vestibulum lectus metus eu est. Phasellus id elit id est euismod cursus vel eget neque. Ut scelerisque mi quis elementum aliquam. Donec rhoncus nec diam vel suscipit. Nulla feugiat auctor orci nec vehicula. Cras dignissim justo diam, vitae sodales purus imperdiet eu. Nam a mattis metus. Sed hendrerit tellus eu erat luctus cursus."
      };
      }
    };
</script>

<style>

  
  p {
    text-align: left
  }
  h1 {
    text-align: left
  }
</style>