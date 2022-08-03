
<template>
<div class="data">
      <h2>name : {{displayName}}</h2>

      <h3 id="h3">Age : {{displayAge}}</h3>
</div>
</template>


<script>
export default {
  
  props:[
      "displayName",
      "displayAge"
  ]
};
</script>


<style>

.data{
      margin-top:30px;
      margin-left:20%;
      display:flex;
}
#h3{
margin-left:20px;
padding-top:4px;

}
</style>