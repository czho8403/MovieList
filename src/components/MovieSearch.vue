<script setup>
import { ref } from "vue"
import axios from "axios"

const searchQuery = ref('')
const result = ref('')
const searchMovies = ()=>{
axios.post(`https://www.omdbapi.com/?apikey=82c8d948&s='${searchQuery.value}'`).then(res=>{
  console.log(res)
  result.value=res.data
})
}
</script>

<template>
  <div style='display:flex'><input v-model="searchQuery"/><button @click=searchMovies>搜尋</button></div>

  
<div>{{result}}</div>
</template>