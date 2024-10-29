<template>
  <div class="Home">
    // showing recative values using refs 
    Home
    <p>The name is {{ name }} and age is {{ age }}</p>
    <button @click = handleClick>Click me </button>
    <button @click = age++>add 1 to age </button>
  </div>
  <input type="text" v-model="name">
</template>


<script >
import { ref } from 'vue'

export default{
  name :'Home',
  setup(){
     const name = ref('mario')
     const age = ref(20)

     const handleClick = () => {
       name.value = 'luigi'
       age.value = 36
     }

     return{name ,age, handleClick}
  }
  
}

</script>


