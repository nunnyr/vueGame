<template>
 <button class="reset" :reset="toggle" @click="onClick">{{toggle}}>Reset</button>
</template>

<script setup></script>



<style>
.reset {
  color: white;
  font-size: 15px;
  background-color: teal;
  border-radius: 10px;
  width: 100px;
  height: 50px;

}
</style>