<template>
<!-- <h1>Hola from row</h1> -->
<Box :place="1" @click="onClick"></Box>
<Box :place="2" @click="onClick"></Box>
<Box :place="3" @click="onClick"></Box>


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

const {rowNum} = toRefs(props)

function onClick(){
  console.log("this is rowNum:", rowNum.value)
}

</script>

<style></style>