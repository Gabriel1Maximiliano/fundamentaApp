<template>
    <h1>Contador sin computed properties</h1>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <p>{{count}} <sup>2</sup> = {{ getSquareValue() }}</p>
       <h1>Contador con computed properties</h1>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
       <p>{{count}} <sup>2</sup> = {{ computedSquare }}</p>
     <button @click="count++">Count is: {{ count }}</button>
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
 }
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
