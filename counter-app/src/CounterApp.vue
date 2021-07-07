<template>
    <div>
        <!-- :counter is equal to v-bind:counter -->
        <counter-view v-bind:counter="counter"></counter-view>
        <counter-controller @on-increment="handleIncrement($event)" @on-reset="handleReset"></counter-controller>
    </div>
</template>

<script>
import CounterView from './components/CounterView';
import CounterController from './components/CounterController';
export default {
    components:{
    CounterView,CounterController
  },
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    handleIncrement(val){
      this.counter +=val
    },
    handleReset(){
      this.counter = 0
    }
  },
}
</script>