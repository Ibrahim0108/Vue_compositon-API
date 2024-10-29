<template>
  <div class="computed">
    <h1>Home</h1>
    <input type="text " v-model="search">
    <p> the search item is - {{ search }}</p>
    <div v-for="name in matchNames" :key="name">

        {{ name }}
    </div>

  </div>
</template>

<script>
import { computed, ref, watch, watchEffect } from 'vue'
export default {

    setup(){
        const search = ref('')
        const names = ref(['mario','luigi','toad','yoshi','koopa','peach'])

        const matchNames = computed(()=> {
            return names.value.filter((name)=> name.includes(search.value))
        })

        watch(search, () =>{
            console.log('the watch is running')
        })
        watchEffect(() => {
            console.log('the watch is running' ,search.value)
        })

        return {names ,search ,matchNames}
    }

}
</script>

<style>
.computed{
    justify-items: center;
    margin-top: 70px;
}
</style>