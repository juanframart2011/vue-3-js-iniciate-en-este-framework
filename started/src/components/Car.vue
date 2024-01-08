<template>
    <h2>Car Props</h2>
    <p>
      Marca: {{ brand }}
    </p>
    <p>
      Modelo: {{ model }}
    </p>
    <p>
      Potencia: {{ power }}
    </p>
    <button>- Disminuir</button>
  </template>
  
  <script>
  export default {
    props:{
        power:Number,
        upPower:Function,
    },
    emits:[
        "downPower"
    ],
      setup(props, context){
          const brand = 'Audi';
          const model = 'A4';

          const testPower = () => {
            props.upPower();
          }

          const downPowerFn = () => {
            context.emit("downPower");
          }
  
          return {
            brand,
            model,
          };
      }
  }
  </script>
  
  <style>
  
  </style>