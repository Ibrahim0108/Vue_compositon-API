<template>
     // showing reactive using reactive() method 
    <div class="stuff">
  <div>
   
    <h1>Refs</h1>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
<button @click="updateNinjaOne">update ninja 1</button>
</div>
<div>
    <h1>reactive</h1>
     <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
     <button @click="updateNinjaTwo">update ninja 2 </button>
  </div>
</div>
</template>

<script>
import { ref , reactive } from 'vue'
export default {

    setup(){
        const ninjaOne = ref({name : 'mario',age: 20})
        const ninjaTwo = reactive({name : 'luigi',age:30})

        const updateNinjaOne = () => {
            ninjaOne.value.age = 40
        }
        const updateNinjaTwo = () => {
            ninjaTwo.age = 60
        }
        return {ninjaOne , updateNinjaOne , ninjaTwo , updateNinjaTwo}
    }


}
</script>

<style scoped>
.stuff{
    display: flex;
    justify-content: space-evenly;
    margin-top: 90px;
}
</style>