<template>
      <div class=form-style>
            <b-form @submit.prevent="saveUserData">
                  <b-form-input v-model="userName" placeholder="Enter your name"></b-form-input>
                  <b-form-input id="second-form" v-model="userAge" placeholder="Enter your Age"></b-form-input>
                  <b-button style="margin-left:20px;" variant="danger">Submit</b-button>
            </b-form >
                  
      </div>
</template>

<script>
export default {

      emits:[
            "add-user"
      ],
      data(){
            return{
                  userName:"",
                  userAge:""
            };
            
      },
      method:{
            saveUserData(){
                  this.$emit("add-user",this.userName,this.userAge);

                  //this.$emit('delete-event',this.friendId)
            }
      }
}
</script>


<style>
.form-style{
      margin:100px 0px 0px 100px;
      width:50%;
      display:flex;
}

.form-style #second-form {
     margin-left:20px;
}
</style>