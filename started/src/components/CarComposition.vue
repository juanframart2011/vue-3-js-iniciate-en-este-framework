<template>
  <h2>Car</h2>
  <p>
    Marca: {{ brand }}
</p>
<p>color:<br>
    <span v-for="(color, index) in colors" :key="index">{{ color }}<br></span>
</p>
<p>price: {{ price }}</p>
<p>message: {{ message }}</p>

<p>Potencias</p>
<ul>
    <template v-for="(power, index) in powers" :key="index">
        <li v-if="power < 300">Urbana: {{ power }}</li>
        <li v-else-if="power == 320">Hibrido: {{ power }}</li>
        <li v-else>Carrera: {{ power }}</li>
    </template>
</ul>

<p>Potencia {{ powerCurrent }}</p>

<button @click="upPower">Aumentar</button>
<button @click="downPower">Disminuir</button>
</template>

<script>
export default {
    setup(){
        const brand = 'Mercedes';
        const colors =  ['rojo','azul'];
        const powers =  [60,80,100,120,140,160,200,300,320,400,500,600];
        const price =  180;
        const message = {
            title: 'Hola',
            name: 'Leo'
        };
        const powerCurrent = 1;

        const upPower = () => {
            this.powerCurrent++;
        };
        const downPower = () => {
            this.powerCurrent--;
        };

        return {
            brand,
            colors,
            powers,
            powerCurrent,
            price,
            message,
            upPower,
            downPower
        };
    }
}
</script>

<style>

</style>