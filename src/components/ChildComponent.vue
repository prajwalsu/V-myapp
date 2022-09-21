<template>
  <h1> Hi i am child Component</h1>
  <button @click="handleClick">Send Data to parent</button>
</template>

<script>
export default {
    emits: ["getDataFromChild"],
    data() {
        return{
            toyInfo: "red toy car",
        };
    },
    methods: {
        handleClick(){
            // console.log("handle click execute");
            this.$emit("getDataFromChild", this.toyInfo);
        }
    }

}
</script>

<style>

</style>