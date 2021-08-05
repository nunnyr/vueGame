<template>
<button class="box" :show="toggle" @click="onClick">{{toggle}}</button>
</template>

<script setup>
import {ref} from 'vue'

let toggle = ref("")


function onClick(){
  console.log("clicked")
  
  if(toggle.value === ""){
      toggle.value = "X"
      return
  } 
  console.log("clickTwo")
  if(toggle.value === "X") {
        toggle.value = "O"
        console.log("to O")
        return
  }
  console.log("clickThree")
  if(toggle.value === "O"){
    toggle.value = "X"
    console.log("lol back to X")
  }
      console.log("clickFour")
      
}

</script>

<style>
.box {
  width: 100px;
  height: 100px;
}

</style>