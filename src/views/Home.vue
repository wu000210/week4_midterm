<template>
  <div class="home container">
    <h1>{{ welcome }}</h1>
    <el-row>
  <el-col :span="12"><div class="grid-content bg-purple">
    <img src="../assets/images/1.jpeg" alt="">   </div></el-col>
  <el-col :span="12"><div class="grid-content bg-purple-light">
    <p>{{ prograph}} </p>
    <p>{{ prograph}}</p>
      </div></el-col>
</el-row>
</div>
</template>

<script>
export default {
 
    data() {
      return {
        welcome:"Welcome to My Vue App",
        prograph: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec sodales, urna at vulputate feugiat, nulla ex gravida augue, sit amet vestibulum lectus metus eu est. Phasellus id elit id est euismod cursus vel eget neque. Ut scelerisque mi quis elementum aliquam. Donec rhoncus nec diam vel suscipit. Nulla feugiat auctor orci nec vehicula. Cras dignissim justo diam, vitae sodales purus imperdiet eu."

      };
    }
};

</script>

<style>
  .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  p {
    text-align: left
  }
   h1 {
    text-align: left
  }
  
</style>
