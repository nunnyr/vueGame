<template>
<button class="box" :show="toggle" @click="onClick">{{toggle}}</button>
</template>

<script setup>
import {ref, defineProps, defineEmits, toRefs} from 'vue'

//define props
const props = defineProps({
    place: {
      type: Number,
      required: true
    }
})

// const { place } = toRefs(props)
const emit = defineEmits(["sendBox"])

let toggle = ref("")
//create new variable to hold state to print out ID for box to the console
//will be using props to 

function onClick(){
  // console.log("this is box", place.value)
   //debugger
    console.log("here", toggle.value)
  if(toggle.value === ""){
      toggle.value = "X"
     
  } else if(toggle.value === "X") {
        toggle.value = "O"
  } else if(toggle.value === "O"){
    toggle.value = "X"
  }

  let emitInfo = props.place
  
  emit("sendBox", emitInfo)
}



</script>

<style>
.box {
  width: 100px;
  height: 100px;
}

</style>