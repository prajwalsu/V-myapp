<template>
  <h1> Hey, This is my component...</h1>
  <h2> Prajwal</h2>
  <h2>Name i am
    :{{ name }} 
    {{ greeting}}
  </h2>

  <p> 
    UserName is : {{ UserName}} 
    rollNo:{{ rollNo }} 
    College:{{College}}
  </p>
</template>

<script>
export default {
  // without validation
  // props:["greeting", "UserName", "rollNo", "College"],

  // with validation
  props:{
    greeting:{
      type:String,
      required:true
    },
    UserName:{
      type:String,

    },
    rollNo:{
      type: Number,
      default:90
    },
    College:{
      type: String,
    }
  }, 

  data(){
    return{
      name:"Prajwal",
    }
  }

}
</script>

<style>

</style>