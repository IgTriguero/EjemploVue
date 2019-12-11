<template>
  <div>
      <p>{{variable}}</p>
      <p>{{inputText}}</p>
      <p v-if="inputText === 'xd'">Ja, xD</p>
      
      <input type="text" v-model="inputText">

      <p v-for="(item, index) in array" :key="index">{{item}}</p>
      <button @click="funtion1">Exec func 1</button>
      <button @click="funtion2">Exec fucn 2</button>
  </div>

</template>

<script>
export default {
  name: "Ejemplo",
  data(){
    return{
      variable: "Que pasa gente, estoy DORAMION",
      inputText: "",
      array:["hola", "hola1", "this."]
    }
  },
  methods: {
    funtion2(){
      this.variable = "funtion2"
    },
    funtion1(){
      this.variable = "funtion1"
    }
  }
}
</script>

<style>

</style>