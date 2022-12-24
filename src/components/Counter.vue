

<script>
export default {
    name:'Patito feo',
  data() {
    return {
      count: 0
    }
  }
}
</script>

<template>
 <h1>Contador</h1>
    <p>{{count}}</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style>

</style>
