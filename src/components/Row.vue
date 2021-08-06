<template>
<!-- <h1>Hola from row</h1> -->
<Box :place="1"></Box>
<Box :place="2"></Box>
<Box :place="3"></Box>


</template>

<script setup>
import Box from './Box.vue'
import {defineProps} from 'vue'

function returnPlace(){
  console.log("inside returnPlace")
  return 1
}
</script>

<style></style>