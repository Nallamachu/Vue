<template>
  <div class="my-app">
    <!-- :counter is equal to v-bind:counter -->
    <counter-view v-bind:counter="counter"></counter-view>
    <!-- @click is equal to v-on:click -->
    <button @click="increment(1)">Increment</button>
    <button @click="increment(-1)">Decrement</button>
    <button @click="reset">Reset</button>
  </div>
</template>

<script>
import CounterView from './components/CounterView';
export default {
  components:{
    CounterView
  },
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increment(val){
      this.counter +=val
    },
    reset(){
      this.counter=0
    }
  },
}
</script>

<style>
.my-app{
  color: blue;
  padding: 200px;
}
</style>