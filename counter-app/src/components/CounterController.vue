<template>
    <div>
        <!-- @click is equal to v-on:click -->
        <button @click="$emit('on-increment',1)">Increment</button>
        <button @click="$emit('on-increment',-1)">Decrement</button>
        <!-- Here is an example of method calling on click event -->
        <button @click="reset">Reset</button>
    </div>
</template>

<script>
export default {
    emits: ['on-increment','on-reset'],
    methods: {
        increment(val){
            this.$emit('on-increment',val)
        },
        reset(){
            //this.counter=0
            this.$emit('on-reset',0)
        }
    }
}
</script>