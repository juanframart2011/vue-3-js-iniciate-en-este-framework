<template>
  <h2>Car</h2>
  <p>
    Marca: {{ brand }}
</p>
<p>price: {{ price }}</p>
<p>message: {{ message }}</p>
<p>Power: {{ power }}</p>
<button @click="upPower">Aumentar</button>
<button @click="downPower">Disminuir</button>
</template>

<script>
export default {
    data(){
        return {
            brand : 'Mercedes',
            colors :  ['rojo','azul'],
            power :  1,
            price :  180,
            message : {
                title: 'Hola',
                name: 'Leo'
            },
        }
    },
    methods:{
        upPower(){
            this.power++;
        },
        downPower(){
            this.power--;
        }
    }
}
</script>

<style>

</style>