<template>
  <div class="contact">
    <h1>{{ title }}</h1>
  <el-row>
  <el-col :span="12"><div class="grid-content bg-purple">
      <h2>{{ address }}</h2>
      <p>{{ ad }}

       <p>{{ phone }}</p>
      
      </div></el-col>
  <el-col :span="12"><div class="grid-content bg-purple-light">
      <h2>{{ hours }}</h2>
    
          <ul>
              <li v-for="obj of operation">{{ obj.key }} : {{ obj.value }}</li>
              </ul>
     
      </div></el-col>
</el-row>
</div>
</template>
<script>

export default {
    data() {
      return {
        title: "Contact",
        ad: "1435 Woodroffe Avenue,Ottawa, Ontario, K2G1V8",
        hours: "Hours of Operation",
        address: "Address",
        phone: "613-7274723", 
        operation: [
          {
              key: "Monday",
              value: "8AM-6PM"
          },
          {
              key: "Tuesday",
              value: "8AM-6PM"
          },
          {
              key: "Wednesday",
              value: "8AM-6PM"
          },
          {
              key: "Thursday",
              value: "8AM-6PM"
          },
          {
              key: "Firday",
              value: "8AM-5PM"
          },
          {
              key: "Saturday",
              value: "10AM-4PM"
          },
          {
              key: "Sunday",
              value: "10AM-2PM"
          }
      
        ]
    };
}
};
</script>
<style>
.contact {
    width: 60%;
    margin: 0 auto;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}
 
  li {
     text-align: left;
     list-style: none;

  }
  
p {
    text-align: left;
}
  
</style>
