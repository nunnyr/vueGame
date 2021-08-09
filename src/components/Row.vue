<template>
<!-- <h1>Hola from row</h1> -->
<Box :place="1" @sendBox="onClick"></Box>
<Box :place="2" @sendBox="onClick"></Box>
<Box :place="3" @sendBox="onClick"></Box>


</template>

<script setup>
import Box from './Box.vue'
import {defineProps, toRefs} from 'vue'

const props = defineProps({
  rowNum:{
    type: Number,
    required: true
  }
})

// const {rowNum} = toRefs(props)

function onClick(info){
  debugger
  let uniqueId = `This is row: ${props.rowNum}, this is place: ${info}`
  console.log("here", uniqueId)
  //console.log("this is rowNum:", rowNum.value)
}

//note for pushing

</script>

<style></style>