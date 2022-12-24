<template>
    <!-- <h1>Contador sin computed properties</h1>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <h1>Contador con computed properties</h1>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
     <button @click="count++">Count is: {{ count }}</button> -->
     <div>
        <p>{{count}} <sup>2</sup> = {{ increaseBy1(1) }}</p>
       <p>{{count}} <sup>2</sup> = {{ decreaseBy1() }}</p>
        <button v-on:click="increaseBy1()" >+1</button>
        <p>{{count}}</p>
        <button v-on:click="decreaseBy1()" >-1</button>
        <p>{{count}}</p>
        <button>-1</button>
     </div>

   </template>

<script>
export default {
    name:'Patito feo',
  data() {
    return {
      count: 0
    }
},
methods:{
 getSquareValue() {// esta se dipara cada evez que se llama a la fncion 
    console.log('me dipare soy getSquareValue ')
    return this.count*this.count
 },
 increaseBy1(){console.log('soy invrease')
   this.count = this.count +1
},decreaseBy1(){
 this.count = this.count -1;
},

},
computed:{// las propiedades computadas se guardan en cache por eso se dispara solo una vez
    // esta caracteristica ayuda con los procesos pesados de la app
    computedSquare(){
        console.log('me dispare soy computedSquare')
        return this.count*this.count
    }
}
}
</script>



<style>

</style>
