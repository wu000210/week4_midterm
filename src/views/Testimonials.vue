<template>
  <div class="testimonials">
  <h1>{{ testimonials }}</h1>
    
  
<el-row>
    
        <el-col v-for="(allcomment, index) of allcomments" :key="index" :span="8">
          <div class="feedback">
          <p>{{ allcomment.Name }} - {{ allcomment.jobTitle }}</p>
          <p>{{ allcomment.comment }}</p>
        </div>
    </el-col>
    </el-row>
 
  <el-form
     v-show="!dialogVisible"
     :model="ruleForm" :rules="rules" ref="ruleForm" label-width="120px" class="demo-ruleForm">
  <el-form-item label="name" prop="Name">
    <el-input v-model="ruleForm.Name"></el-input>
  </el-form-item>

  <el-form-item label="Positin" prop="jobTitle">
    <el-input v-model="ruleForm.jobTitle"></el-input>
  </el-form-item>

  <el-form-item label="Comments" prop="comment">
    <el-input type="textarea" v-model="ruleForm.comment"></el-input>
  </el-form-item>

  <el-form-item>
    <el-button type="primary" @click="submitForm('ruleForm')">Submit</el-button>
  </el-form-item>
</el-form>
  </div>
</template>
<script>
import Todo from "@/components/Todo.vue";
import TodoForm from "@/components/TodoForm.vue";
import axios from "axios";
  export default {
    data() {
      return {
        testimonials:"Testimonials",
        // dialogVisible: false,
        Name:"",
        jobTitle:"",
        comment:"",
        allcomments: [],

        ruleForm: {
          Name:"",
          jobTitle: "",
          comment: ""
        },
        rules: {
          Name: [
            { required: true, message: "Please input  name", trigger: 'blur' },
            {min: 3, max: 50, message: "Length should be 3 to 50", trigger:"blur"}
          ],
          jobTitle: [
            { required: true, message: 'Please input job title', trigger: 'blur' },
            {min: 3, max: 50, message: "Length xhould be 3 to 50", trigger:"blur"}
          ],
          comment: [
            { required: true, message: 'Please input comment', trigger: 'blur' },
            { min: 3, max: 120, message: 'Length should be 3 to 120', trigger: 'blur' }
          ]
        
        },
      };
    },
    
    methods: {
      submitForm(formName) {
        this.$refs[formName].validate((valid) => {
          if (valid) {
           this.allcomments.push(this.ruleForm);
            console.log(this.allcomments);
            axios
              .put(
                "https://midterm-99a2b.firebaseio.com/data.json",
                this.allcomments
              )
              .then(response =>{
                console.log(response);
                console.log("Your data was saved status: " + response.status);
              })
              .catch(error => {
                console.log(error);
              });
              
          } else {
            console.log("error submit!!");
            return false;
          }
        });
      }
    },
    created() {
    axios.get("https://midterm-99a2b.firebaseio.com/data.json")
    .then(response => {
        console.log(response.data);
        if(response.data) {
          this.allcomments = response.data; 
        }     
    })
    .catch(error => {
        console.log(" there are and error in getting data: "  + error.response);
    });
  }
  };
</script>
<style>
.testimonials {
    width: 60%;
    margin: 0 auto;    
}
 
  li {
     text-align: left;
  }
  
p {
    text-align: left;
    
}
.feedback {
  background-color:darkgray;
}  
</style>

