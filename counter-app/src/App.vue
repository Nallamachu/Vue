<template>
  <div class="app-container">
    <counter-app></counter-app>
  </div>
</template>

<script>
  import CounterApp from './CounterApp';
  export default {
    components:{
      CounterApp  
    }
  }
</script>

<style>
  .app-container {
    color: blue;
    padding: 200px;
  }
</style>