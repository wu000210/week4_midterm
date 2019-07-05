<template>
  <div id="app">
    <div id="nav">
      <div class="container">
        <el-row>
 
  <el-col :span="8"><div class="grid-content bg-purple-light"><h2>My Vue App</h2></div></el-col>
  <el-col :span="4"><div class="grid-content bg-purple"><router-link to="/"><h4>Home</h4></router-link> </div></el-col>
  <el-col :span="4"><div class="grid-content bg-purple-light"><router-link to="/about"><h4>About</h4></router-link> </div></el-col>
  <el-col :span="4"><div class="grid-content bg-purple"> <router-link to="/contact"><h4>Contact</h4></router-link> </div></el-col>
  <el-col :span="4"><div class="grid-content bg-purple-light"> <router-link to="/testimonials"><h4>User Testimonials</h4></router-link> </div></el-col>
</el-row>
      </div>
    </div>
 
  </div>
</template>

<style>
#nav {
  background-color: dimgrey;
}

  .container{
    max-width:1170px;
    height: 80px;
    margin:auto;  
    font-size: 22px;
    
  }
</style>
