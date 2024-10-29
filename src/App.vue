<script setup>


</script>

<template>
<header>

      <nav>
        <RouterLink to="/">Refs</RouterLink>
        <RouterLink to="/about">Reactive</RouterLink>
        <RouterLink to="/new">computed</RouterLink>
      </nav>
   
  </header>

  <RouterView />
</template>

<style scoped>
header{
   justify-items: center;
  
}
nav a{
  text-decoration: none;
  margin-right: 40px;
  font-size: 40px;
  font-weight: bold;
  color: red;
}
</style>
