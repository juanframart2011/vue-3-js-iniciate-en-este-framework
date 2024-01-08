<template>
  <h1>Vue Js</h1>
  <Car :power="power" :upPower="upPower" @downPower="downPower" />
  <hr />
  <CarOptions />
  <hr />
  <CarComposition />
</template>

<script>
import Car from './components/Car.vue';
import CarComposition from './components/CarComposition.vue';
import CarOptions from './components/CarOptions.vue';
export default {
  components:{
    Car,
    CarComposition,
    CarOptions
  },
  setup(){
    let power = 30;

    const upPower = () => {

    };

    const downPower = () => {

    };

    return {
      downPower,
      power,
      upPower,
    }
  }
}
</script>

<style>

</style>