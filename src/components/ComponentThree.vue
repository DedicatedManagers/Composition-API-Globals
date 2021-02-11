<template>
  <div>
    This component tries to Destructure the "globals" object for the template.  It loses reactivity.<br>
    ComponentThree - Global Counter: {{counter}}<br>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
import {globals} from "../globals";

export default {
  name: "ComponentThree",
  setup(){
    console.log(globals);
    return {...globals};  // Breaks reactivity
    // return {counter: globals.counter};  // Breaks Reactivity - same as above
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
