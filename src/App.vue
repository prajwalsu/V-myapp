<template>
<h1>Heloo world</h1>

<!-- rendering comonent -->
<!-- stati prop no v-mind only for dynmaic -->

<!-- paremt to child -->
<!-- <my-component greeting="good morning" :UserName="UserName" :rollNo="40" :College="College" /> -->

<!-- child to parent -->

<child-component-vue @getDataFromChild="getDataFromChild"/>

<h3>Data from Toy from Child:{{KidsToyData}}</h3>
</template>

<script>
import ChildComponentVue from './components/ChildComponent.vue'
// import MyComponent from './components/MyComponent.vue'

export default {
  name: 'App',

  components: {
    ChildComponentVue
    // MyComponent,
    
  },
  data(){
    return{
      UserName:"Raju Rastogi",  
      KidsToyData:"",

       };
  },
  methods:{
    // chocolate function
    // 1. in parent component creatte function and pass it to child component
    // 2. call that function in child component and pass the data inside that function
     
    getDataFromChild(childData){
      console.log("chocolate function executed",childData);
      this.KidsToyData=childData
    }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
