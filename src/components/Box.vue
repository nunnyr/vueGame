<template>
<button class="box" :show="toggle" @click="onClick">{{toggle}}</button>
</template>

<script setup>
import {ref, defineProps, toRefs} from 'vue'

//define props
const props = defineProps({
    place: {
      type: Number,
      required: true
    }
})

const { place } = toRefs(props)

let toggle = ref("")
//create new variable to hold state to print out ID for box to the console
//will be using props to 



function onClick(){
  // console.log("this is box", place.value)
  if(toggle.value === ""){
      toggle.value = "X"
      return
  } 
  if(toggle.value === "X") {
        toggle.value = "O"
        console.log("to O")
        return
  }

  if(toggle.value === "O"){
    toggle.value = "X"
    
  }   
}

</script>

<style>
.box {
  width: 100px;
  height: 100px;
}

</style>