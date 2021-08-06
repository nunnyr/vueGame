<template>
<!-- <h1>Hola from row</h1> -->
<Box :place="returnPlace"></Box>
<Box :place="2"></Box>
<Box :place="3"></Box>


</template>

<script setup>
import Box from './Box.vue'

function returnPlace(){
  console.log("inside returnPlace")
  return 1
}
</script>

<style></style>