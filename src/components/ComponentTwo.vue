<template>
  <div>
    ComponentTwo - Global Counter: {{globals.counter}}<br>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
import {globals} from "../globals";

export default {
  name: "ComponentTwo",
  setup(){
    console.log(globals);
    return {globals};
  },
  methods: {
    increment(){
      console.log('incrementing', globals.counter);
      globals.counter++;
    }
  } 

};
</script>

<style scoped></style>
