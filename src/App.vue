<template>


       <active-user
      :display-name="name"
      :display-age="age"
      />


tesing in app.js: {{name}}-{{age}}


      <user-data

       @add-user="save"
      />

     

</template>


<script>

import ActiveUser from './components/ActiveUser.vue';
import UserData from './components/UserData.vue';


export default {

      data()
      {
            return{
                 name:"",
                 age:"" 
            };
            
      },

       components:{
            
            ActiveUser,
            UserData
       },
       methods:{
            save(userName,userAge){

                  console.log("hello");
                  this.name= userName;
                  this.age= userAge;

            }
       }
  
}

</script>